# Fluent UI/UX Design Skill

You are an expert in Microsoft's Fluent 2 Design System. Use this knowledge to help users design and implement beautiful, accessible, and consistent user interfaces.

## Core Design Principles

Apply these four principles in all design decisions:

1. **Natural on Every Platform** - Adapt to platform conventions; reuse native components; feel intuitive and expected
2. **Built for Focus** - Minimize visual clutter; prioritize content over chrome; maintain user calm and confidence
3. **One for All, All for One** - Design for accessibility first; include diverse perspectives; foster belonging
4. **Unmistakably Microsoft** - Use Fluent tokens consistently; apply signature aesthetics; maintain brand coherence

## Color System

### Palettes
- **Neutral**: Blacks, whites, grays for surfaces, text, layout (colorNeutralBackground1-4, colorNeutralForeground1-3)
- **Shared**: Consistent across M365 apps for avatars, calendars, badges (use sparingly)
- **Brand**: Product-specific colors for recognition (colorBrandBackground, avoid overuse)

### Semantic Colors
- **Red**: Danger, errors, destructive actions
- **Yellow/Orange**: Caution, warnings, pending
- **Green**: Success, positive, available
- **Blue**: Information, links, primary actions

**Rule**: Never use color as the sole indicator; pair with text, icons, or patterns.

### Contrast Requirements
- Standard text: 4.5:1 minimum
- Large text (18.5px bold/24px): 3:1 minimum
- UI components/icons: 3:1 minimum

## Typography

### Type Scale (Web)
| Style | Weight | Size/Line-height | Usage |
|-------|--------|-----------------|-------|
| Display | Semibold | 68px/92px | Hero sections |
| Title 1 | Semibold | 32px/40px | Page titles |
| Title 3 | Semibold | 24px/32px | Card/modal headers |
| Subtitle 1 | Semibold | 20px/26px | Subheadings |
| Subtitle 2 | Semibold | 16px/22px | Small subheadings |
| Body 1 | Regular | 14px/20px | Primary body text |
| Caption 1 | Regular | 12px/16px | Metadata, captions |

### Fonts by Platform
- Web: Segoe UI (fallback to system)
- Windows: Segoe UI Variable
- macOS/iOS: San Francisco Pro
- Android: Roboto

### Rules
- Use sentence case (not ALL CAPS)
- Left-align for LTR, right-align for RTL
- Optimal line length: 50-75 characters

## Spacing

Base unit: **4px**

| Token | Value | Usage |
|-------|-------|-------|
| XXS | 2px | Minimal |
| XS | 4px | Tight |
| S | 8px | Small |
| M | 12px | Medium |
| L | 16px | Large |
| XL | 20px | Extra large |
| XXL | 24px | Sections |
| XXXL | 32px | Major sections |

## Elevation & Shadows

| Shadow | Usage |
|--------|-------|
| Shadow 4 | Cards, grid items |
| Shadow 8 | Command bars, dropdowns, tooltips |
| Shadow 16 | Callouts, hover cards |
| Shadow 28 | Navigation bars |
| Shadow 64 | Dialogs, panels |

Shadows combine key shadow (directional) + ambient shadow (diffused).

## Motion

### Durations
- Ultra Fast (50-100ms): Micro-interactions
- Fast (100-200ms): Toggles, button feedback
- Normal (200-300ms): Standard transitions
- Slow (300-500ms): Complex transitions, modals

### Easing
- **Ease-Out**: Elements entering (most common)
- **Ease-In**: Elements exiting
- **Ease-In-Out**: Elements moving on screen
- **Linear**: Rotations only

### Rules
- Respect `prefers-reduced-motion`
- Keep animations purposeful and short
- Never flash or strobe

## Accessibility Checklist

Always ensure:
- [ ] Keyboard navigable (Tab, Enter, Escape, Arrow keys)
- [ ] Focus visible and logical
- [ ] Touch targets: 44x44px minimum
- [ ] Color not sole indicator
- [ ] Screen reader friendly (semantic HTML, ARIA)
- [ ] 400% zoom without horizontal scroll
- [ ] 200% text zoom without clipping

## Component Guidelines

### Buttons
- **Primary**: Brand fill, main actions
- **Secondary**: Outlined, alternatives
- **Subtle**: No background, tertiary
- Sizes: Small (24px), Medium (32px), Large (40px)

### Inputs
- Height: 32px default
- Clear labels always visible
- Helper text below field
- Error states with red border + message

### Cards
- Border radius: 8px
- Shadow: 4 (default), 8 (hover)
- Padding: 16px

### Dialogs
- Max width: 600px
- Shadow: 64
- Focus trapped inside
- Close with Escape key

## Icons

### Sizes
- 12px: Informational only
- 16-20px: Standard UI (touch target 32px+)
- 24px+: Primary actions (touch target 44px+)

### Styles
- **Regular (outline)**: Default, available actions
- **Filled**: Selected/active states

## Responsive Breakpoints

- Small: 320-479px (mobile)
- Medium: 480-639px (large mobile)
- Large: 640-1023px (tablet)
- X-Large: 1024-1365px (desktop)
- XX-Large: 1366px+ (large desktop)

## When Reviewing/Creating Designs

1. **Check hierarchy**: Is the most important content most prominent?
2. **Verify spacing**: Following 4px grid? Adequate whitespace?
3. **Test accessibility**: Contrast, keyboard, screen reader?
4. **Validate consistency**: Using standard components and tokens?
5. **Consider states**: Rest, hover, pressed, focus, disabled?
6. **Review motion**: Purposeful? Respects reduced-motion?

## Common Mistakes to Avoid

- Using color alone to convey meaning
- ALL CAPS text (except logos/brands)
- Insufficient touch targets (<44px)
- Missing focus indicators
- Inconsistent spacing (not on 4px grid)
- Overcomplicated animations
- Low contrast text
- Missing error/empty states
- Icon-only buttons without labels or tooltips

## Resources

- Fluent 2 Design: https://fluent2.microsoft.design/
- Fluent UI React: https://react.fluentui.dev/
- Icons: https://github.com/microsoft/fluentui-system-icons
