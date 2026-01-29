# Fluent UI/UX Design Skill for Claude

This document provides Claude with comprehensive knowledge of Microsoft's Fluent 2 Design System to assist users with UI/UX design decisions, component usage, accessibility guidance, and creating visually consistent Microsoft-style interfaces.

---

## Table of Contents

1. [Core Design Principles](#core-design-principles)
2. [Color System](#color-system)
3. [Typography](#typography)
4. [Spacing System](#spacing-system)
5. [Iconography](#iconography)
6. [Elevation & Shadows](#elevation--shadows)
7. [Motion & Animation](#motion--animation)
8. [Accessibility Guidelines](#accessibility-guidelines)
9. [Component Patterns](#component-patterns)
10. [Layout Guidelines](#layout-guidelines)
11. [Theming](#theming)
12. [Platform Considerations](#platform-considerations)
13. [Design Tokens Reference](#design-tokens-reference)

---

## Core Design Principles

Fluent 2 is built on four foundational design principles:

### 1. Natural on Every Platform
- **Functional**: Layouts adapt to different screen sizes and platforms, enabling reuse of native components approximately 80% of the time
- **Emotional**: Experiences feel intuitive and expected, creating reliability and trust
- **Implementation**: Use platform-native components where possible; adapt to platform conventions

### 2. Built for Focus
- **Functional**: Technology should communicate and perform without hindering user action
- **Emotional**: Minimizing visual clutter maintains user centeredness, calm, and confidence
- **Implementation**: Remove unnecessary elements; prioritize content over chrome; use progressive disclosure

### 3. One for All, All for One
- **Functional**: Including diverse perspectives and abilities early in design creates better solutions
- **Emotional**: Inclusive design fosters belonging among users
- **Implementation**: Design for accessibility from the start; test with diverse users; support multiple input methods

### 4. Unmistakably Microsoft
- **Functional**: Create signature experiences connecting products through distinctive aesthetics
- **Emotional**: A little personality goes a long way in brand recognition
- **Implementation**: Use Fluent design tokens consistently; apply brand colors appropriately; maintain visual coherence

---

## Color System

### Color Palettes

Fluent uses three primary color palettes:

#### 1. Neutral Colors
- Blacks, whites, and grays that ground interfaces
- Used for surfaces, text, and layout elements
- Lighter neutrals highlight primary focus areas
- Establish visual hierarchy through shade variation

```
Neutral Tokens:
├── colorNeutralBackground1: #FFFFFF (primary background)
├── colorNeutralBackground2: #FAFAFA (secondary background)
├── colorNeutralBackground3: #F5F5F5 (tertiary background)
├── colorNeutralForeground1: #242424 (primary text)
├── colorNeutralForeground2: #424242 (secondary text)
├── colorNeutralForeground3: #616161 (tertiary text)
├── colorNeutralStroke1: #D1D1D1 (borders)
└── colorNeutralStrokeAccessible: #616161 (accessible borders)
```

#### 2. Shared Colors
- Aligned across Microsoft 365 applications
- Used for high-value components: avatars, calendars, badges
- Enable quick recognition across products
- Use sparingly for accenting important areas

```
Shared Color Palette:
├── Red: Danger, errors, destructive actions
├── Orange: Warnings, attention
├── Yellow: Caution, pending states
├── Green: Success, positive feedback, available
├── Blue: Information, links, primary actions
├── Purple: Special features, premium
├── Pink: Highlights, decorative
└── Teal: Secondary information
```

#### 3. Brand Colors
- Product-specific colors for immediate recognition
- Examples:
  - Communication Blue (Outlook)
  - Teams Purple
  - Word Blue
  - Excel Green
  - PowerPoint Orange
- Avoid overuse to maintain hierarchy

```
Brand Color Ramp (example):
├── colorBrandBackground: #0078D4 (primary brand)
├── colorBrandBackgroundHover: #106EBE
├── colorBrandBackgroundPressed: #005A9E
├── colorBrandForeground1: #0078D4
└── colorBrandStroke1: #0078D4
```

### Semantic Colors

Use consistently across the interface:

| Color | Meaning | Usage |
|-------|---------|-------|
| Red | Danger | Errors, destructive actions, critical alerts |
| Yellow/Orange | Caution | Warnings, pending states, attention needed |
| Green | Success | Confirmation, positive feedback, available status |
| Blue | Information | Links, informational messages, primary actions |

**Important**: Never use color as the sole indicator. Always pair with text, icons, or other visual indicators.

### Interaction States

Components progress through states:

**Light Mode**:
- Rest → Hover → Pressed (progressively darker)
- Focus uses thicker strokes, not color changes

**Dark Mode**:
- Rest → Hover → Pressed (progressively lighter)
- Focus uses thicker strokes

**Windows Exception**: Controls become lighter rather than darker in hover/pressed states.

### Color Accessibility

1. **Standard text**: Minimum 4.5:1 contrast ratio
2. **Large text** (18.5px bold or 24px regular): Minimum 3:1 contrast ratio
3. **Interactive elements**: Minimum 3:1 against adjacent colors
4. **Non-textual elements**: Minimum 3:1 against background

---

## Typography

### Font Families

| Platform | Primary Font | Fallback |
|----------|-------------|----------|
| Web | Segoe UI | -apple-system, system-ui, sans-serif |
| Windows | Segoe UI Variable | Segoe UI |
| macOS | San Francisco Pro | -apple-system |
| iOS | San Francisco Pro | -apple-system |
| Android | Roboto | sans-serif |

### Type Scale (Web)

| Style | Weight | Size | Line Height | Usage |
|-------|--------|------|-------------|-------|
| Display | Semibold | 68px | 92px | Hero sections, landing pages |
| Title 1 | Semibold | 32px | 40px | Page titles |
| Title 2 | Semibold | 28px | 36px | Section headings |
| Title 3 | Semibold | 24px | 32px | Card titles, modal headers |
| Subtitle 1 | Semibold | 20px | 26px | Subheadings |
| Subtitle 2 | Semibold | 16px | 22px | Small subheadings |
| Body 1 | Regular | 14px | 20px | Primary body text |
| Body 2 | Regular | 12px | 16px | Secondary body text |
| Caption 1 | Regular | 12px | 16px | Captions, metadata |
| Caption 2 | Regular | 10px | 14px | Small labels, timestamps |

### Font Weights

- **Regular (400)**: Body text, captions
- **Semibold (600)**: Headings, emphasis, buttons
- **Bold (700)**: Strong emphasis only

### Typography Guidelines

1. **Case**: Use sentence case; avoid ALL CAPS for readability
2. **Alignment**: Left-align for LTR languages; right-align for RTL
3. **Color hierarchy**:
   - Primary text: colorNeutralForeground1
   - Secondary text: colorNeutralForeground2
   - Tertiary/disabled: colorNeutralForeground3
4. **Line length**: Optimal 50-75 characters for readability
5. **Hierarchy**: Create clear distinction between heading levels

---

## Spacing System

### Base Unit

Fluent uses a **4px base unit** for all spacing calculations.

### Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| spacingHorizontalNone | 0px | No spacing |
| spacingHorizontalXXS | 2px | Minimal spacing |
| spacingHorizontalXS | 4px | Tight spacing |
| spacingHorizontalSNudge | 6px | Slight adjustment |
| spacingHorizontalS | 8px | Small spacing |
| spacingHorizontalMNudge | 10px | Medium adjustment |
| spacingHorizontalM | 12px | Medium spacing |
| spacingHorizontalL | 16px | Large spacing |
| spacingHorizontalXL | 20px | Extra large spacing |
| spacingHorizontalXXL | 24px | Section spacing |
| spacingHorizontalXXXL | 32px | Major section spacing |

### Spacing Guidelines

1. **Component internal padding**: 8-16px
2. **Between related elements**: 4-8px
3. **Between groups**: 16-24px
4. **Section margins**: 24-32px
5. **Page margins**: 16-48px (responsive)

### Layout Spacing

```
Page Structure:
├── Page margin: 24-48px (responsive)
├── Section spacing: 32px
├── Card padding: 16px
├── Form field spacing: 16px vertical
└── Button group spacing: 8px
```

---

## Iconography

### Icon Collections

1. **System Icons**: UI controls, actions, navigation (MIT licensed)
2. **Product Launch Icons**: App launchers, product representation
3. **File Type Icons**: Document types, file formats

### Icon Sizes

| Size | Usage | Touch Target |
|------|-------|--------------|
| 12px | Informational only, not interactive | N/A |
| 16px | Inline with text, small UI | 24px minimum |
| 20px | Standard buttons, menus | 32px minimum |
| 24px | Primary actions, navigation | 40px minimum |
| 28px | Emphasis, large buttons | 44px minimum |
| 32px+ | Headers, features | 48px minimum |

### Icon Styles

1. **Regular (Outline)**: Primary style for available actions and navigation
2. **Filled**: Selected states, active items, emphasis for small sizes

### Icon Usage Guidelines

1. **Naming**: Use literal metaphors based on shape (e.g., "shield" not "security")
2. **Modifiers**: Add in bottom-right corner for specificity
3. **Color**: Apply solid colors sparingly; maintain visual balance
4. **Localization**: Consider cultural symbol meanings across regions
5. **Pairing**: Always pair icons with text labels when possible
6. **Consistency**: Use same style throughout an interface section

### Icon Resources

- Fluent UI Icons: https://github.com/microsoft/fluentui-system-icons
- Icon search: https://react.fluentui.dev/?path=/docs/icons-catalog--page

---

## Elevation & Shadows

### Shadow System

Fluent uses a two-shadow system combining:
1. **Key Shadow**: Sharp, directional shadow defining element edges
2. **Ambient Shadow**: Soft, diffused shadow implying distance from surface

### Elevation Levels

#### Low Elevation Ramp

| Token | Blur | Y-Offset | Use Case |
|-------|------|----------|----------|
| Shadow 2 | 2px | 1px | Cards without edge, pressed FABs |
| Shadow 4 | 4px | 2px | Cards, grid items, list items |
| Shadow 8 | 8px | 4px | Command bars, tooltips, dropdowns |
| Shadow 16 | 16px | 8px | Callouts, hover cards |

#### High Elevation Ramp

| Token | Blur | Y-Offset | Use Case |
|-------|------|----------|----------|
| Shadow 28 | 28px | 14px | Navigation bars, tab bars |
| Shadow 64 | 64px | 32px | Dialogs, panels, sheets |

### Shadow Values (Light Mode)

```css
/* Shadow 4 - Standard card */
box-shadow:
  0 2px 4px rgba(0, 0, 0, 0.14),  /* Key shadow */
  0 0 2px rgba(0, 0, 0, 0.12);     /* Ambient shadow */

/* Shadow 8 - Dropdown */
box-shadow:
  0 4px 8px rgba(0, 0, 0, 0.14),
  0 0 2px rgba(0, 0, 0, 0.12);

/* Shadow 16 - Callout */
box-shadow:
  0 8px 16px rgba(0, 0, 0, 0.14),
  0 0 2px rgba(0, 0, 0, 0.12);

/* Shadow 64 - Dialog */
box-shadow:
  0 32px 64px rgba(0, 0, 0, 0.24),
  0 0 8px rgba(0, 0, 0, 0.12);
```

### Shadow Values (Dark Mode)

Dark mode uses increased opacity:
- Key shadow: 28% opacity (vs 14% in light)
- Ambient shadow: Maintain similar values

### Usage Guidelines

1. **Cards**: Shadow 4 for static, Shadow 8 on hover
2. **Dropdowns/Menus**: Shadow 8
3. **Tooltips**: Shadow 8
4. **Dialogs**: Shadow 64
5. **Panels**: Shadow 64
6. **Navigation**: Shadow 28 when elevated

**Note**: Windows uses strokes instead of key shadows for outlines.

---

## Motion & Animation

### Motion Principles

1. **Functional**: Applied with purpose to serve functionality
2. **Natural**: Follow physical laws (inertia, gravity, weight)
3. **Consistent**: Unified motion across experiences
4. **Appealing**: Delightful without being distracting

### Duration Guidelines

| Type | Duration | Usage |
|------|----------|-------|
| Instant | 0ms | State changes without animation |
| Ultra Fast | 50-100ms | Micro-interactions, ripples |
| Fast | 100-200ms | Button feedback, toggles |
| Normal | 200-300ms | Standard transitions |
| Slow | 300-500ms | Complex transitions, modals |
| Very Slow | 500ms+ | Page transitions, onboarding |

### Easing Functions

| Type | CSS Value | Usage |
|------|-----------|-------|
| Linear | `linear` | Rotations, looping animations only |
| Ease-Out | `cubic-bezier(0, 0, 0.58, 1)` | Elements entering (most common) |
| Ease-In | `cubic-bezier(0.42, 0, 1, 1)` | Elements exiting |
| Ease-In-Out | `cubic-bezier(0.42, 0, 0.58, 1)` | Elements moving on screen |

### Transition Types

1. **Enter/Exit**: Fade + scale for appearing/disappearing elements
2. **Elevation**: Shadow changes for depth indication
3. **Top-level**: Fade between pages (avoid slide effects)
4. **Container transform**: Resize/reposition for responsive design

### Choreography

1. **Staggering**: Delay animation starts for groups (16-32ms offsets)
2. **Hierarchy**: Important elements animate with more prominence
3. **Direction**: Animations should flow with reading direction

### Motion Accessibility

1. Respect `prefers-reduced-motion` media query
2. Keep durations short and natural
3. Avoid flashing or strobing effects
4. Provide alternative content communication (ARIA live regions)
5. Never use motion for essential information

```css
/* Respect reduced motion preferences */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## Accessibility Guidelines

### WCAG Compliance

Fluent components meet or surpass **WCAG 2.1 AA standards**.

### Color & Contrast

| Element | Minimum Ratio |
|---------|---------------|
| Normal text | 4.5:1 |
| Large text (18.5px bold / 24px) | 3:1 |
| UI components | 3:1 |
| Graphics/icons | 3:1 |
| Focus indicators | 3:1 |

### Keyboard Navigation

1. **Focus order**: Follow logical "Z" pattern (left-to-right, top-to-bottom)
2. **Focus management**: Focus must not get "lost" after closing dialogs/modals
3. **Focus visibility**: Clear visual indicators for focused elements
4. **Tab stops**: All interactive elements must be focusable
5. **Skip links**: Provide for main content navigation

### Focus Indicators

```css
/* Fluent focus indicator style */
:focus-visible {
  outline: 2px solid #000000;
  outline-offset: 2px;
  border-radius: 4px;
}

/* High contrast mode */
@media (forced-colors: active) {
  :focus-visible {
    outline: 2px solid CanvasText;
  }
}
```

### Screen Reader Support

1. Use semantic HTML elements
2. Provide descriptive alt text for images
3. Use ARIA labels for icon-only buttons
4. Implement ARIA live regions for dynamic content
5. Maintain logical heading hierarchy (h1 → h2 → h3)

### Responsive Design

1. **Reflow**: Content must not require horizontal scrolling at 400% zoom
2. **Minimum width**: Support 320px viewport width
3. **Text scaling**: Support up to 200% text zoom without clipping
4. **Touch targets**: Minimum 44x44px for interactive elements

### Inclusive Design Checklist

- [ ] Color is not the only indicator of meaning
- [ ] All functionality available via keyboard
- [ ] Focus order is logical and predictable
- [ ] Error messages are clear and actionable
- [ ] Forms have visible labels
- [ ] Media has captions/transcripts
- [ ] Animations can be paused/disabled
- [ ] Time limits are adjustable or removable

---

## Component Patterns

### Buttons

| Variant | Usage | Appearance |
|---------|-------|------------|
| Primary | Main actions | Filled, brand color |
| Secondary | Alternative actions | Outlined |
| Subtle | Tertiary actions | No background |
| Transparent | Minimal footprint | No styling until hover |

```
Button Sizes:
├── Small: 24px height, 8px padding
├── Medium: 32px height, 12px padding (default)
└── Large: 40px height, 16px padding
```

### Inputs

- **Text fields**: 32px height default, clear labels, helper text below
- **Checkboxes**: 16x16px, with visible focus rings
- **Radio buttons**: 16x16px, grouped with fieldsets
- **Dropdowns**: Match text field styling, clear affordances

### Cards

```
Card Anatomy:
├── Container (rounded corners: 8px, shadow: 4)
├── Header (optional image, title, subtitle)
├── Content area (body text, media)
└── Actions (buttons aligned to bottom)
```

### Dialogs

- Maximum width: 600px
- Overlay: 40% black (light mode) / 60% black (dark mode)
- Shadow: 64
- Focus trapped within dialog
- Close via Escape key

### Navigation

- **Top navigation**: Primary app navigation
- **Side navigation**: Section/page navigation
- **Breadcrumbs**: Hierarchical location
- **Tabs**: Content within same context

---

## Layout Guidelines

### Grid System

```
Responsive Breakpoints:
├── Small: 320-479px (mobile)
├── Medium: 480-639px (large mobile)
├── Large: 640-1023px (tablet)
├── X-Large: 1024-1365px (desktop)
└── XX-Large: 1366px+ (large desktop)
```

### Content Layouts

1. **Single column**: Mobile, focused reading
2. **Two column**: Navigation + content
3. **Three column**: Navigation + content + details
4. **Grid**: Cards, galleries, dashboards

### Z-Index Hierarchy

| Level | Z-Index | Usage |
|-------|---------|-------|
| Base | 0 | Default content |
| Dropdown | 100 | Menus, popovers |
| Overlay | 200 | Modal backdrops |
| Modal | 300 | Dialogs, sheets |
| Notification | 400 | Toasts, alerts |
| Maximum | 9999 | Critical overlays |

---

## Theming

### Theme Structure

Fluent uses a token-based theming system:

```javascript
const theme = {
  // Color tokens
  colorBrandBackground: '#0078D4',
  colorNeutralBackground1: '#FFFFFF',
  colorNeutralForeground1: '#242424',

  // Typography tokens
  fontFamilyBase: 'Segoe UI, -apple-system, sans-serif',
  fontSizeBase300: '14px',
  fontWeightSemibold: 600,

  // Spacing tokens
  spacingHorizontalM: '12px',
  spacingVerticalL: '16px',

  // Border tokens
  borderRadiusMedium: '4px',
  strokeWidthThin: '1px',

  // Shadow tokens
  shadow4: '0 2px 4px rgba(0, 0, 0, 0.14)',
};
```

### Built-in Themes

1. **Web Light** (default)
2. **Web Dark**
3. **Teams Light**
4. **Teams Dark**
5. **Teams High Contrast**

### Custom Theming

1. Start with base theme
2. Override brand colors (primary ramp)
3. Generate derived color tokens
4. Test accessibility compliance
5. Validate across light/dark modes

---

## Platform Considerations

### Web

- Use Fluent UI React v9 (`@fluentui/react-components`)
- Griffel for styling (atomic CSS-in-JS)
- Built-in keyboard/focus management
- RTL support included

### Windows

- Native Fluent components via WinUI
- Mica/Acrylic materials for backgrounds
- System theme integration
- High contrast mode support

### iOS

- San Francisco Pro typography
- Native gesture integration
- Safe area considerations
- Dynamic Type support

### Android

- Roboto typography
- Material Design interoperability
- Edge-to-edge display support
- Dark theme integration

---

## Design Tokens Reference

### Color Tokens

```
colorNeutralBackground1: Primary surface
colorNeutralBackground2: Secondary surface
colorNeutralBackground3: Tertiary surface
colorNeutralBackground4: Quaternary surface
colorNeutralForeground1: Primary text
colorNeutralForeground2: Secondary text
colorNeutralForeground3: Tertiary text
colorNeutralForegroundDisabled: Disabled text
colorNeutralStroke1: Default borders
colorNeutralStrokeAccessible: Accessible borders
colorBrandBackground: Primary brand
colorBrandBackgroundHover: Brand hover
colorBrandBackgroundPressed: Brand pressed
colorBrandForeground1: Brand text
colorCompoundBrandForeground1: Compound brand
colorStatusDangerBackground: Error background
colorStatusDangerForeground: Error text
colorStatusWarningBackground: Warning background
colorStatusWarningForeground: Warning text
colorStatusSuccessBackground: Success background
colorStatusSuccessForeground: Success text
```

### Typography Tokens

```
fontFamilyBase: 'Segoe UI', 'San Francisco', Roboto, sans-serif
fontFamilyMonospace: Consolas, 'Courier New', monospace
fontSizeBase100: 10px
fontSizeBase200: 12px
fontSizeBase300: 14px
fontSizeBase400: 16px
fontSizeBase500: 20px
fontSizeBase600: 24px
fontWeightRegular: 400
fontWeightMedium: 500
fontWeightSemibold: 600
fontWeightBold: 700
lineHeightBase100: 14px
lineHeightBase200: 16px
lineHeightBase300: 20px
lineHeightBase400: 22px
```

### Spacing Tokens

```
spacingHorizontalXXS: 2px
spacingHorizontalXS: 4px
spacingHorizontalS: 8px
spacingHorizontalM: 12px
spacingHorizontalL: 16px
spacingHorizontalXL: 20px
spacingHorizontalXXL: 24px
spacingVerticalXXS: 2px
spacingVerticalXS: 4px
spacingVerticalS: 8px
spacingVerticalM: 12px
spacingVerticalL: 16px
spacingVerticalXL: 20px
spacingVerticalXXL: 24px
```

### Border Tokens

```
borderRadiusNone: 0px
borderRadiusSmall: 2px
borderRadiusMedium: 4px
borderRadiusLarge: 6px
borderRadiusXLarge: 8px
borderRadiusCircular: 9999px
strokeWidthThin: 1px
strokeWidthThick: 2px
strokeWidthThicker: 3px
strokeWidthThickest: 4px
```

---

## Quick Reference Card

### Design Decisions Checklist

When designing with Fluent:

1. **Layout**
   - [ ] Follows 4px grid
   - [ ] Appropriate breakpoints
   - [ ] Clear visual hierarchy
   - [ ] Adequate white space

2. **Color**
   - [ ] Using semantic colors correctly
   - [ ] Meets contrast requirements
   - [ ] Works in light and dark modes
   - [ ] Color not sole indicator

3. **Typography**
   - [ ] Using type scale correctly
   - [ ] Sentence case (not ALL CAPS)
   - [ ] Clear heading hierarchy
   - [ ] Appropriate line lengths

4. **Components**
   - [ ] Using standard Fluent components
   - [ ] Consistent sizing
   - [ ] Proper state handling
   - [ ] Touch targets meet minimums

5. **Accessibility**
   - [ ] Keyboard navigable
   - [ ] Screen reader friendly
   - [ ] Motion respectful
   - [ ] Focus indicators visible

6. **Motion**
   - [ ] Purpose-driven animations
   - [ ] Appropriate durations
   - [ ] Respects reduced motion
   - [ ] Natural easing

---

## Resources

- **Fluent 2 Design System**: https://fluent2.microsoft.design/
- **Fluent UI React**: https://react.fluentui.dev/
- **GitHub Repository**: https://github.com/microsoft/fluentui
- **Fluent UI Icons**: https://github.com/microsoft/fluentui-system-icons
- **Figma UI Kits**: Available on Figma Community

---

*This skill enables Claude to provide expert-level guidance on Microsoft Fluent Design System principles, helping users create consistent, accessible, and beautiful interfaces that align with Microsoft's design language.*
