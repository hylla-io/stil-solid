# stil-solid

Astro-first components with Solid for interactive islands. Apache 2.0. Consumed by Hylla websites, Tillsyn Electron, Hylla Electron, and the Hylla hosted web surfaces. Formerly Sjal.

## Status

Skeleton. To be refactored from `sjal/` once `stil`'s visual language and binding vocabulary are settled.

## Scope

- **Astro components** for static-first surfaces (marketing pages, docs, blog).
- **Solid islands** for interactive bits (token editor, command palette, AI chat) — chosen because Solid's reactivity model is closer to SwiftUI's `@State` than React's, which means stil's component contracts feel parallel across `stil-solid` and `stil-swift`.
- **Token consumption** via `stil/dist/tokens.json` at build time.
- **Bindings consumption** from `stil/bindings/baseline.json` for keyboard nav.

## Why Solid not React

- Smaller runtime (~7KB).
- Fine-grained reactivity matches SwiftUI's mental model — same component shape, different render pipeline.
- Plays well with Astro islands (lazy hydration).

## Out of scope

- Native iOS / macOS — that's `stil-swift`.
- Terminal — that's `lykta`.
