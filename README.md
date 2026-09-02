# Loyalty Lane Apparel — Studio Production

**Shadow Noir streetwear. Stay Loyal.**

Loyalty Lane Apparel is a dynamic, production-oriented commerce experience within The Lingo Legacy ecosystem. The product surface is intentionally cohesive: one primary application experience with routed states, drawers, modals, product views, cart states, account/identity surfaces, and checkout handoff rather than a collection of disconnected static pages.

## Studio standard

Every layer is upgraded together:

- **World:** Shadow Noir, edgy premium streetwear environment
- **Web/App:** responsive application shell and state-driven navigation
- **UI/UX:** typography, spacing, controls, feedback, empty/loading/error states
- **Icons:** canonical brand mark, app icon, favicon, loader, navigation and product icons
- **Media:** responsive product/campaign assets with canonical-source tracking
- **Motion:** page transitions, touch feedback, product interactions and reduced-motion fallback
- **Touch:** mobile-first hit targets and explicit pressed/focus/loading/success/error states
- **Commerce:** catalog → product → cart → checkout handoff
- **Identity:** Lingo ID integration surface
- **Rewards:** XP/rewards integration surface
- **Analytics:** event instrumentation boundary

## Unified production stack

`GITHUB → FLUTTER → FIREBASE → CLOUDFLARE → APPDEPLOY`

### Runtime pipeline

`WEB/UI → APP SHELL → LINGO ID → CATALOG → TAP STITCH → CART → CHECKOUT HANDOFF → REWARDS/XP → ASK LINGO → ANALYTICS → QA → DEPLOY`

### Touch pipeline

`TOUCH → HIT TARGET → UI STATE → FEEDBACK → API ACTION → PERSIST → ANALYTICS → VISUAL CONFIRMATION`

### Asset pipeline

`SOURCE ART → CANONICAL ASSET → RESPONSIVE VARIANTS → ICON/LOADER VARIANTS → OPTIMIZATION → RESOURCE REGISTRY → RUNTIME → QA`

## Infrastructure boundaries

- **GitHub:** source control, CI/CD definitions, tests, release records and rollback references.
- **Flutter:** mobile shell, shared tokens, navigation state, touch behavior and native app assets.
- **Firebase:** identity/data/state/analytics/notifications where configured.
- **Cloudflare:** edge delivery, Workers/API, D1/KV/R2, domains, caching and security where configured.
- **AppDeploy:** deployment orchestration, resource validation, previews and promotion where configured.

Secrets must remain in managed secret stores and never be committed to source.

## Production gate

`BUILD → TEST → ASSET VALIDATION → RESPONSIVE QA → ACCESSIBILITY → INTEGRATION → DOMAIN/ROUTING → ANALYTICS → EVIDENCE → ROLLBACK TARGET → RELEASE`

No security or asset-validation boundary is bypassed. Validation failures are fixed at the source/resource contract while canonical artwork and product identity are preserved.

## Product identity

**LOYALTY LANE APPAREL**  
**TAP STITCH**  
**STAY LOYAL.**

The visual system is deliberately distinct from other Lingo Legacy properties while sharing the underlying production standards.
