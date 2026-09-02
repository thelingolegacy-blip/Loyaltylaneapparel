# Stage 03 — One-Page App Shell Navigation

## Shell

The application uses one persistent shell. Navigation changes the active view/state without recreating the global shell.

- App bar
- Primary navigation
- Primary viewport
- Overlay manager
- Toast region
- Modal region

## Routes

| Route | Surface | Lazy boundary |
|---|---|---|
| `/` | Home | No |
| `/shop` | Collection | Yes |
| `/product/:productId` | Product detail | Yes |
| `/tap-stitch` | Tap Stitch | Yes |
| `/bag` | Shopping bag | Yes |
| `/account` | Account / Lingo ID | Yes |

## State requirements

- Preserve cart/bag state across navigation.
- Preserve authenticated session state without putting secrets in URLs.
- Preserve UI preferences where appropriate.
- Show loading, empty, error, success, pressed, focus, and disabled states.
- Maintain keyboard focus and screen-reader context during route changes.
- Respect reduced-motion preferences.

## Touch requirements

Interactive controls must provide a minimum 44px touch target, visible pressed feedback, and non-touch keyboard equivalents.

## World boundary

Stage 03 provides the structural shell only. Shadow Noir visual treatment belongs to Stage 04 while shared tokens and icon primitives originate in Stage 02.

## Integration boundary

The shell exposes adapter boundaries for Lingo ID, commerce/checkout, XP/rewards, Firebase, Cloudflare, and analytics. No credentials or secrets belong in route parameters or client source.
