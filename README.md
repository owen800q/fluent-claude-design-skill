# Fluent UI/UX Design Skill for Claude

A comprehensive design skill based on Microsoft's [Fluent 2 Design System](https://fluent2.microsoft.design/) that enables Claude to provide expert UI/UX design guidance.

## Files

| File | Purpose |
|------|---------|
| `skill.md` | Main skill file for Claude Code |
| `reference.md` | Comprehensive reference documentation |

## Usage

### Claude Code (CLI)

**Option 1: Add to CLAUDE.md (Recommended)**

Create or edit `CLAUDE.md` in your project root and include the skill:

```markdown
# Project Instructions

## Design System
This project uses Microsoft Fluent 2 Design System.
See: https://github.com/anthropics/fluent-claude-design-skill/blob/main/skill.md

<!-- Or copy the full content of skill.md here -->
```

**Option 2: Clone and reference locally**

```bash
# Clone this repo
git clone https://github.com/anthropics/fluent-claude-design-skill.git

# In your project, reference it in CLAUDE.md
echo "See ../fluent-claude-design-skill/skill.md for Fluent design guidelines" >> CLAUDE.md
```

**Option 3: Use /add-context command**

During a Claude Code session:
```
/add-context /path/to/skill.md
```

### Claude.ai (Web)

**Option 1: Create a Project (Recommended)**

1. Go to [claude.ai](https://claude.ai) → Projects
2. Create new project (e.g., "Fluent UI Design")
3. Add `skill.md` content to Project Knowledge
4. Start conversations within that project

**Option 2: Paste at conversation start**

1. Copy contents of `skill.md`
2. Start new conversation
3. Paste as first message: "Use these Fluent design guidelines for our conversation: [paste content]"

**Option 3: Custom Instructions**

1. Go to Settings → Custom Instructions
2. Paste key sections from `skill.md`
3. Available in all future conversations

## What Claude Can Help With

| Task | Example Prompt |
|------|---------------|
| Design Review | "Review this button design for Fluent compliance" |
| Typography | "What's the correct type scale for a card header?" |
| Accessibility | "Check if this color meets WCAG contrast requirements" |
| Components | "What elevation/shadow should I use for a dropdown?" |
| CSS Generation | "Generate Fluent-style CSS for a primary button" |
| Layout | "How should I space these form fields?" |

## Example Session

```
User: I'm building a settings page. What typography should I use?

Claude: For a settings page following Fluent guidelines:

- **Page title**: Title 1 (Semibold, 32px/40px)
- **Section headers**: Subtitle 1 (Semibold, 20px/26px)
- **Setting labels**: Body 1 (Regular, 14px/20px)
- **Helper text**: Caption 1 (Regular, 12px/16px)

Use Segoe UI on Windows, San Francisco on Mac/iOS, or Roboto on Android.
```

## Quick Reference

### Spacing (4px base)
| Token | Value |
|-------|-------|
| XS | 4px |
| S | 8px |
| M | 12px |
| L | 16px |
| XL | 20px |

### Shadows
| Level | Use |
|-------|-----|
| Shadow 4 | Cards |
| Shadow 8 | Dropdowns |
| Shadow 16 | Popovers |
| Shadow 64 | Dialogs |

### Contrast (WCAG)
- Text: 4.5:1 minimum
- Large text: 3:1 minimum
- UI elements: 3:1 minimum

## Resources

- [Fluent 2 Design System](https://fluent2.microsoft.design/)
- [Fluent UI React](https://react.fluentui.dev/)
- [Fluent UI GitHub](https://github.com/microsoft/fluentui)
- [Fluent System Icons](https://github.com/microsoft/fluentui-system-icons)

## License

This skill documentation is provided for educational purposes. Microsoft Fluent Design System and related assets are trademarks of Microsoft Corporation.
