# Loyalty Lane Apparel — Studio Stack Contract

## One-page product rule
One cohesive application shell. Use routed states, drawers, modals, panels, overlays, and game-like surfaces inside the primary experience rather than unnecessary disconnected pages.

## Stack
`GITHUB → FLUTTER → FIREBASE → CLOUDFLARE → APPDEPLOY`

## Runtime pipeline
`WEB/UI → APP SHELL → LINGO ID → CATALOG → TAP STITCH → CART → CHECKOUT HANDOFF → REWARDS/XP → ASK LINGO → ANALYTICS → QA → DEPLOY`

## Touch pipeline
`TOUCH → HIT TARGET → UI STATE → FEEDBACK → API ACTION → PERSIST → ANALYTICS → VISUAL CONFIRMATION`

## Asset pipeline
`SOURCE ART → CANONICAL ASSET → RESPONSIVE VARIANTS → ICON/LOADER VARIANTS → OPTIMIZATION → RESOURCE REGISTRY → RUNTIME → QA`

## Media requirements
- Shadow Noir visual world
- Product and campaign imagery
- Canonical app icon
- Favicon
- Phone/home-screen icon
- Loading mark and animated loader
- Motion/transition assets
- Sound identity and interaction feedback
- Reduced-motion alternative

## Infrastructure responsibilities
- GitHub: source control, CI/CD definitions, tests, release records, rollback references.
- Flutter: mobile app shell, shared design tokens, navigation state, touch behavior, canonical icon assets, identity and commerce integration surfaces.
- Firebase: identity/data/state/analytics/notifications where configured; secrets stay out of source control.
- Cloudflare: edge delivery, Workers/API, D1/KV/R2, domains, caching, routing and security where configured.
- AppDeploy: deployment orchestration, asset/resource validation, previews and production promotion where configured.

## Release gate
No release is considered production-ready until build, tests, asset validation, responsive QA, accessibility smoke testing, integration checks, routing/domain checks, analytics checks, and rollback evidence are reconciled.

## Rule
Never bypass a platform security or asset-validation boundary. Fix the asset/resource contract and preserve canonical artwork instead.
