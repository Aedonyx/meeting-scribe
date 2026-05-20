# meeting-scribe
A Claude Skill that turns meeting transcripts and notes into polished documentation — formatted to match your team's existing Word template.

## What it does

Upload your team's meeting minutes template once. The skill inspects it, learns the structure (sections, fields, styles, branding), and from then on produces meeting documentation that looks like your team made it — because the formatting, headers, logos, and conventions are all preserved from your actual template.

Works with any format:
- Formal memos (To / From / Date / Re)
- Bulleted notes under date headers
- Action-item tracking tables
- Agenda-driven layouts (numbered items with discussion under each)
- Decision logs
- Custom layouts your team has designed

## Why it's different

Most AI meeting summarizers produce generic output that doesn't match your team's existing format. This skill preserves your template exactly — logos, fonts, headers, footers, custom paragraph styles — and only updates the content sections.

No API keys. No external services. Runs entirely inside Claude.

Validated against three common template patterns: formal memo (To/From/Date/Re fields, ALL CAPS sections), casual bulleted notes (informal section labels, simple structure), and PM-style action-item tables (inline metadata, navy branding, styled tables with Action/Owner/Due Date/Status columns). All three render correctly with formatting preserved end-to-end.

## Installation

### Option 1: Claude.ai (web/desktop/mobile)
1. Go to **Settings → Capabilities → Skills**
2. Click **Add Skill**
3. Upload the `meeting-scribe/` folder from this repo
4. Toggle the skill on

### Option 2: Claude Code (terminal)
```bash
git clone https://github.com/Aedonyx/meeting-scribe.git
cp -r meeting-scribe/meeting-scribe ~/.claude/skills/
```

Restart Claude Code to discover the new skill.

## Usage

Attach your team's meeting minutes template (any .docx) and provide meeting content via:
- A transcript (paste or upload)
- Typed notes
- A bulleted summary

Example prompt:
> "Create meeting minutes from yesterday's design review. Here's our template [attached] and the transcript [pasted below]."

The skill will:
1. Inspect your template's structure
2. Confirm the section mapping with you
3. Edit the template's underlying XML, preserving all formatting
4. Output a finished `.docx` you can download

## Requirements

- A meeting minutes template in `.docx` format (any layout)
- Meeting content in any form: transcript, typed notes, or a bulleted summary

## License

MIT — use freely, modify freely, ship freely.

## Maintained by

[Aedonyx](https://aedonyx.io) — AI literacy and automation for knowledge workers.

If you're a firm looking to build custom skills for your internal workflows, or want to learn how to build your own AI tooling, reach out.
