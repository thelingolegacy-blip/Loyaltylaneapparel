# Loyalty Lane — Icon, Media & Touch System

## Canonical identity surfaces

| Surface | Role | Rule |
|---|---|---|
| Master mark | Loyalty Lane brand identity | Shadow Noir + Stay Loyal |
| App icon | Phone/app launcher | Simplified silhouette; legible at small size |
| Favicon | Browser identity | Minimal mark; no fine detail |
| Loader | Route/asset initialization | Animated master mark; never a generic spinner |
| Product mark | Tap Stitch/product identity | Consistent across product, cart and checkout states |
| Touch affordance | Mobile interaction | 44px+ hit targets; visible pressed/focus state |

## Media pipeline

`CANONICAL ART → RESOURCE REGISTRY → RESPONSIVE CROP → OPTIMIZE → PRELOAD CRITICAL → LAZY-LOAD SECONDARY → RUNTIME → QA`

Critical above-the-fold artwork should have a deliberate fallback so a missing remote image never breaks layout or navigation.

## Touch pipeline

`TOUCH START → PRESSED STATE → ACTION → PERSISTENCE → FEEDBACK → ANALYTICS`

Required states: default, hover/desktop, focus-visible, pressed, disabled, loading, success and error.

## One-page app experience

The primary storefront remains one cohesive application surface. Catalog filters, product details, bag, identity, rewards, checkout handoff and confirmations are stateful overlays/panels or route states that preserve context.

## Motion

Motion should communicate hierarchy and state, not decorate every interaction. Respect `prefers-reduced-motion`; keep critical actions understandable without animation.

## Sound

Optional sound is event-driven and user-controlled. Never autoplay disruptive audio. Interaction feedback must remain available visually and through accessible state messaging.

## Asset validation

Canonical supplied artwork is preserved. If a platform validator rejects an asset, route the asset through the platform's approved resource mechanism rather than bypassing the security boundary.
