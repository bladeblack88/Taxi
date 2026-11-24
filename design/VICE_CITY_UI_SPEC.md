# Vice City UI direction

This repository currently contains the visual foundation only. It is not yet a decompiled or buildable copy of the supplied taxi APK.

## Goals
- Restyle the existing taxi app without changing business logic, API contracts, navigation semantics, or order lifecycle.
- Keep all operational controls legible and accessible in bright daylight and at night.
- Use a Miami-at-night palette inspired by the atmosphere of Vice City / GTA VI, without copying game logos or proprietary artwork.

## Tokens
| Token | Hex | Use |
|---|---|---|
| Background | #090D1A | Main screen background |
| Surface | #141B2B | Cards and sheets |
| Surface raised | #1C263A | Inputs and elevated panels |
| Pink | #FF3D9A | Primary actions and highlights |
| Coral | #FF765E | Warnings and sunset accents |
| Cyan | #35D7E8 | Secondary actions and map accents |
| Text | #F6F7FB | Primary text |
| Muted | #A6B0C3 | Secondary text |
| Divider | #2B3850 | Separators |

## Screen treatment
- Map: preserve map provider, markers, route overlays, location permissions and map gestures. Use dark surrounding chrome; do not recolor map tiles unless the provider supports it.
- Orders: high-contrast order cards; primary accept/reject controls remain visually distinct and easy to tap.
- Trip/taximeter: emphasize fare and elapsed distance/time; never change calculation code or units.
- Profile/history/payment: consistent dark surfaces, clear status colors, readable metadata.
- Authentication: restrained gradient accent, but preserve all fields, validation and auth flows.

## Motion
Use short opacity/translation transitions only for presentation. No animation may delay, intercept or change a business action.

## Integration rule
Apply these resources to the decoded original project after its package structure and existing themes are available. Do not replace the original app with a mock implementation.
