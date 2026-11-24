# Taxi — Vice City visual redesign

This repository is being prepared for an APK-based recovery and visual redesign.

## Source status

- The currently available input is `base.apk`; the original Android Studio project has not been provided.
- APK inspection confirms Android resources and multiple DEX files.
- The APK contains XML layouts/resources for authentication, the main map, orders, order history, profile, payment, and taximeter screens.
- The package also includes Jetpack Compose libraries, but their presence alone does not establish that the app UI is implemented in Compose.
- The original source tree, build configuration, and signing configuration cannot be assumed to be recoverable from the APK.

## Visual direction: Vice City / GTA VI-inspired

Create an original neon-Miami-inspired visual language without copying GTA logos or artwork:

- Deep midnight navy / charcoal surfaces
- Neon magenta and sunset coral accents
- Turquoise secondary accents
- Dark translucent cards with restrained glow
- High-contrast typography and clear touch targets
- Subtle transitions and feedback animations

## Non-negotiable behavior constraints

Preserve existing app behavior wherever recovery permits:

- Authentication and account flows
- Map, location, and route behavior
- Order discovery, acceptance, and lifecycle
- Taximeter and fare calculations
- Payment flows
- Driver profile and history

Visual changes must not alter business rules, API contracts, navigation semantics, or calculations.

## Recovery and validation plan

1. Decode the APK manifest, resources, layouts, and DEX files.
2. Identify app-owned screens and distinguish them from third-party library resources.
3. Recover a buildable Android project where feasible; document any unrecoverable pieces.
4. Apply the visual theme incrementally, starting with shared colors, typography, shapes, and reusable controls.
5. Verify key driver workflows and build/install the resulting APK.

A recovered project is not equivalent to the original source project. Functional equivalence must be tested before claiming that behavior is preserved.
