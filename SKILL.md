---
name: ev-design-system
description: Reusable Electro-Voice brand design system for responsive web, desktop web, iOS, and Android product artifacts.
triggers:
  - "EV design system"
  - "Electro-Voice design system"
  - "EV branded prototype"
  - "Electro-Voice branded web"
  - "EV mobile app"
  - "EV responsive web"
od:
  mode: prototype
  platform: responsive
  scenario: brand-system
  design_system:
    requires: true
    sections: [color, typography, layout, components, voice]
  outputs:
    primary: index.html
    secondary:
      - brand-spec.md
      - references/checklist.md
---

# EV Design System Skill

Create Electro-Voice branded product artifacts and design-system references for marketing, sales, and product teams. Use the EV brand guide as the authoritative source for color, typography, voice, layout posture, and component behavior.

## Brand source

Primary brand reference: `/Users/freddy/VIBE/ev_brand_guide/ev-brand-guidelines.md`.

If the file is available, read it before generating. If the file is not available, use the embedded rules in this skill and `brand-spec.md` as the fallback source of truth.

## When to use

Use this plugin when the user asks for:

- EV or Electro-Voice branded web prototypes, landing pages, dashboards, banners, or product pages.
- EV branded iOS or Android app screens.
- A reusable EV design system, token sheet, component library, or brand-compliant artifact.
- Marketing, sales, or product-manager-facing EV materials that need brand consistency.

Do not use it for Dynacord-only work unless the user explicitly asks for dual-brand EV × Dynacord output.

## Core visual system

### Color

- Foundation: EV Black `#000000`, EV White `#FFFFFF`, and neutral grays.
- Primary accent: EV Red 50 `#ED1C24`; for PPT-style contexts use EV Red 40 `#BE161D` when a darker red is needed.
- Purple 50 `#6706EF` is allowed only as part of the official red-purple gradient, not as a standalone decorative accent.
- Status colors: Yellow 50 `#FAAF3C`, Green 50 `#75B843`, Red 50 `#ED1C24`.
- Avoid warm beige, peach, orange-brown, generic violet gradients, and decorative pastel washes unless the user provides a separate approved EV campaign reference.

### Typography

- General/product display: `Berthold Akzidenz Grotesk Pro`, with `Arial Narrow` / `Arial Black` fallback.
- General body: `Berthold Akzidenz Grotesk Pro`, Arial, sans-serif.
- PPT-specific display/body: `Nunito Sans` with bold headlines.
- All text is left-aligned unless a specific format demands otherwise.
- Headlines should be bold, condensed, concise, and confident; body copy should remain direct and practical.

### Layout posture

- Prefer black or white product canvases with EV Red used sparingly and decisively.
- Use boxes, split vertical layouts, split horizontal layouts, full-picture layouts, and grid-based content blocks.
- Align web/banner components to a 4px grid.
- Use real product imagery, real environments, close-ups, or labelled product render placeholders; avoid generic decorative illustrations.
- Buttons use clear physical sizing: large 48px high, medium 32px high, small 24px high.
- Preserve logo clear space equal to the height of the letter E on each side when logo assets are present.

### Voice

Write concise, confident, conversational copy. Focus on sound quality, engineering, reliability, flexibility, and audience experience. Avoid empty claims, fake metrics, generic feature names, and filler language.

## Platform contracts

### Responsive and desktop web

- Build real end-user product UI, not a design-process dashboard.
- Include desktop, tablet, and mobile states for responsive web.
- Use EV navigation patterns: symbol/logotype area, first-level menu, and global action/button area.
- Include domain-specific product modules such as product comparison, sound coverage, system configuration, lead capture, dealer/contact actions, downloads, or support tools when relevant.

### iOS app

- Use an iPhone frame or native iOS screen structure when showing app screens.
- Respect 44px minimum hit targets, safe areas, bottom navigation/sheets where appropriate, and iOS-native interaction patterns.
- Keep EV brand expression in content, color, type, and modules without forcing desktop web chrome into the phone UI.

### Android app

- Use a Pixel/Android frame or native Android screen structure when showing app screens.
- Respect 48dp hit targets, Material-style navigation where appropriate, and Android-native interaction patterns.
- Do not reuse iOS-only chrome or gestures.

## Output expectations

When creating a design artifact, produce implementation-ready HTML with clear CSS tokens and component classes. For multi-screen or multi-platform work, use `index.html` as an overview/launcher and put each distinct user-facing screen in its own HTML file.

When creating a reusable design system, include:

1. Brand tokens.
2. Typography scale.
3. Component rules for buttons, cards, banners, nav, forms, product modules, and status messages.
4. Platform-specific guidance for responsive web, desktop web, iOS, and Android.
5. A brand-compliance checklist.

## PPT note

If the user asks for EV slides or PPT-style output, default to the black footer variant. Footer copy should use KEENFINITY as text only, not a decorative logo, unless a source template instructs otherwise.

## Self-check

Before finishing, verify:

- EV Red is the primary accent and is not overused.
- Purple appears only in the official EV red-purple gradient.
- Typography is left-aligned and confident.
- The design uses real product/audio context or honest labelled placeholders.
- No fake metrics, lorem ipsum, generic feature cards, or emoji icon rows are present.
- Platform-specific screens respect native hit targets and navigation patterns.
- Multi-screen work uses separate HTML files for distinct user-facing screens.
- EV PPT outputs use the black footer preference unless the user overrides it.
