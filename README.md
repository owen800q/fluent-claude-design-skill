# Fluent UI/UX Design Skill for Claude

A comprehensive design skill based on Microsoft's [Fluent 2 Design System](https://fluent2.microsoft.design/) that enables Claude to provide expert UI/UX design guidance.

## Files

| File | Purpose |
|------|---------|
| `fluent-design-skill.txt` | Concise skill prompt for Claude Code/Chat system prompts |
| `FLUENT_UI_DESIGN_SKILL.md` | Comprehensive reference documentation |

## Usage

### With Claude Code

Add the skill to your Claude Code configuration:

```bash
# Option 1: Include in project instructions
# Add to your .claude/settings.json or use /add-context command

# Option 2: Reference in conversation
/add-context fluent-design-skill.txt
```

### With Claude Chat (claude.ai)

1. Start a new conversation
2. Paste the contents of `fluent-design-skill.txt` as a system prompt or initial context
3. Or use Claude Projects to add it as project knowledge

### As Custom Instructions

Copy the skill content into your custom instructions to have Fluent design expertise available in all conversations.

## What Claude Can Help With

Once equipped with this skill, Claude can:

### Design Review
- Evaluate UI designs against Fluent principles
- Check accessibility compliance
- Identify spacing and typography issues
- Suggest improvements

### Component Guidance
- Recommend appropriate Fluent components
- Explain component usage patterns
- Provide correct token values
- Guide state handling

### Accessibility
- Check contrast ratios
- Verify keyboard navigation
- Ensure screen reader compatibility
- Validate touch targets

### Code Implementation
- Generate Fluent-compliant CSS
- Suggest correct design tokens
- Implement responsive breakpoints
- Create accessible markup

## Example Prompts

```
"Review this button design for Fluent compliance"

"What's the correct typography scale for a card header?"

"Help me create an accessible form following Fluent guidelines"

"What elevation/shadow should I use for a dropdown menu?"

"Generate CSS for a Fluent-style primary button"

"Check if this color combination meets WCAG contrast requirements"

"How should I handle focus states in my navigation?"
```

## Fluent Design Principles

The skill is based on Fluent 2's four core principles:

1. **Natural on Every Platform** - Adapt to platform conventions
2. **Built for Focus** - Minimize clutter, prioritize content
3. **One for All, All for One** - Inclusive, accessible design
4. **Unmistakably Microsoft** - Consistent brand identity

## Key Features

- **Color System**: Neutral, shared, and brand palettes with semantic meanings
- **Typography**: Complete type scale with platform-specific fonts
- **Spacing**: 4px base unit system with standardized tokens
- **Elevation**: Shadow hierarchy from cards to dialogs
- **Motion**: Duration and easing guidelines with accessibility
- **Components**: Button, input, card, dialog patterns
- **Accessibility**: WCAG 2.1 AA compliance guidance

## Resources

- [Fluent 2 Design System](https://fluent2.microsoft.design/)
- [Fluent UI React](https://react.fluentui.dev/)
- [Fluent UI GitHub](https://github.com/microsoft/fluentui)
- [Fluent System Icons](https://github.com/microsoft/fluentui-system-icons)

## License

This skill documentation is provided for educational purposes. Microsoft Fluent Design System and related assets are trademarks of Microsoft Corporation.
