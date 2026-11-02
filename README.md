# Skills

My custom skills for Claude. Each skill is a folder under `skills/` with a `SKILL.md` file: a short set of instructions that Claude loads when a task matches the skill's description.

## Available skills

| Skill | What it does |
|---|---|
| [corporate-email-en-fr](skills/corporate-email-en-fr/SKILL.md) | Writes, replies to, polishes and translates professional emails in English and French |

### corporate-email-en-fr

Helps Claude write business emails that sound natural in both languages:

- **Write**: drafts a new email from a few bullet points
- **Reply**: answers an email you paste in
- **Polish**: improves your draft's grammar, clarity and tone
- **Translate**: EN → FR and FR → EN, adapting greetings, closings and tone instead of translating word for word

Every answer comes with a subject line and placeholders like `[Name]` for anything you didn't provide. It also uses the right conventions for each language: British English by default; France French with *vous*, correct closings and French typography.

**Example prompts**

- "Write an email to a client saying the delivery is delayed by one week"
- "Translate this to French, it's for my manager: …"
- "Make this email more professional: …"
- "Réponds à cet email en anglais : …"

## Installation

### Claude app (claude.ai, desktop, mobile)

1. Download the skill folder, for example `skills/corporate-email-en-fr`, and zip it so that the folder sits at the root of the zip.
2. In Claude, open **Settings → Capabilities → Skills** and upload the zip. (The exact menu names may differ slightly between versions.)
3. Turn the skill on, then just ask Claude to write or translate an email.

### Claude Code

Copy the skill folder into your personal skills directory:

```bash
# macOS / Linux
git clone https://github.com/<your-username>/skills.git
cp -r skills/skills/corporate-email-en-fr ~/.claude/skills/
```

```powershell
# Windows (PowerShell)
git clone https://github.com/<your-username>/skills.git
Copy-Item -Recurse skills\skills\corporate-email-en-fr "$HOME\.claude\skills\"
```

To use it in one project only, copy it to `.claude/skills/` inside that project instead. Claude Code picks up the skill automatically.

## Customizing

Open `SKILL.md` and adjust it to how you write, for example:

- your default register (formal or friendly)
- British or American English; France or Canadian French
- your usual closings and signature
- terms that should never be translated (company or product names)

## License

[MIT](LICENSE)
