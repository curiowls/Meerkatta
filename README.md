# Meerkatta 🦊

🎓 An OpenClaw skill that turns your AI assistant into a college counselor. Guides high school students from freshman-year interest discovery through senior-year decisions — covering academic planning, extracurricular strategy, essay coaching, college list building, and financial aid. Chat with it on Telegram, Discord, or any OpenClaw channel.

Forked from [Beacon](https://github.com/00derek/Beacon) by [@00derek](https://github.com/00derek).

## What It Does

- **Interest discovery** — Holland Code, flow activities, Ikigai, strengths frameworks
- **Academic planning** — 4-year course sequences mapped to 9 academic tracks
- **Spike strategy** — "well-lopsided" extracurricular profiles over well-rounded ones
- **Timeline tracking** — grade-aware milestone engine, proactive deadline surfacing
- **Socratic essay coaching** — questions to find your story, never writes for you
- **College list building** — reach/match/safety with fit analysis
- **Financial aid** — FAFSA, CSS Profile, scholarships, net price guidance
- **Summer planning** — grade-appropriate program recommendations

## Quick Start (OpenClaw)

### Option 1: Install as a skill

```bash
# Copy the skill folder to your OpenClaw skills directory
cp -r Meerkatta ~/.openclaw/skills/meerkatta

# Or symlink it
ln -s /path/to/Meerkatta ~/.openclaw/skills/meerkatta
```

### Option 2: Clone directly into skills

```bash
cd ~/.openclaw/skills
git clone https://github.com/curiowls/Meerkatta.git meerkatta
```

Once installed, the skill auto-triggers when college prep topics come up. Or just type **kickoff** to start.

### Option 3: Multi-student setup (recommended)

Each student gets their own OpenClaw agent with a dedicated channel:

```bash
# Create an agent per student
openclaw agents add meerkatta-alex
openclaw agents add meerkatta-jamie

# Install shared skill to each agent
ln -s ~/.openclaw/skills/meerkatta ~/.openclaw/agents/meerkatta-alex/skills/meerkatta
ln -s ~/.openclaw/skills/meerkatta ~/.openclaw/agents/meerkatta-jamie/skills/meerkatta

# Customize each agent with the templates
cp Meerkatta/templates/SOUL.md.example ~/.openclaw/agents/meerkatta-alex/SOUL.md
cp Meerkatta/templates/USER.md.example ~/.openclaw/agents/meerkatta-alex/USER.md
# Edit SOUL.md and USER.md for each student

# Connect each agent to its own Telegram bot (or other channel)
# Enable per-student monitoring
openclaw cron add --agent meerkatta-alex --schedule "0 8 * * *" --task "meerkatta-daily-monitor"
```

See `templates/` for starter files.

## Commands

| Command | What It Does |
|---------|-------------|
| `kickoff` | Set up student profile — grade, school, interests, goals |
| `discover` | Deep interest exploration using proven frameworks |
| `plan` | Map interests to academic track and 4-year course sequence |
| `activities` | Build extracurricular strategy and identify your "spike" |
| `testing` | SAT/ACT strategy, prep planning, score analysis |
| `schools` | Build college list — reach, match, safety with fit analysis |
| `essays` | Socratic essay coaching — find your voice through questions |
| `apply` | Application strategy — ED/EA/RD, recommendations, deadlines |
| `financial` | FAFSA, CSS Profile, scholarships, aid comparison |
| `summer` | Summer program strategy connected to your spike |
| `review` | Full progress check against timeline |
| `help` | Context-aware command recommendations |

## How It Works

- **Persistent state** — `counseling_state.md` tracks everything across sessions
- **Socratic approach** — never writes content for the student
- **Motivational Interviewing** — open-ended questions, affirmations, reflective listening
- **Timeline engine** — grade-aware milestones from freshman fall through senior spring
- **Chat-native** — designed for mobile-friendly, conversational interaction via Telegram/Discord/etc.
- **Multi-student** — each student gets their own agent, channel, and personalized counseling voice
- **Parent access** — parents can check in via the student's channel with filtered view

## ⚠️ Parent Access Disclaimer

Parent access control is **conversational and trust-based only**. There is no technical authentication, passwords, or encryption. When a parent messages the student's channel and identifies themselves, Meerkatta withholds coaching notes and essay content — but this is a counseling boundary, not a security boundary. The underlying state files are readable by anyone with filesystem access.

## Daily Knowledge Monitor (New!)

Meerkatta includes a daily cron job that automatically checks for time-sensitive updates relevant to your student's situation:

- 📅 **Deadline changes** — application, test registration, scholarships
- 📋 **Policy updates** — test-optional changes, FAFSA updates
- ⏰ **Approaching milestones** — reminders for upcoming deadlines
- 🏫 **School-specific news** — changes at schools on your college list

**Only notifies when something matters.** No daily spam — silent when there's nothing new.

### Enable it:

```bash
openclaw cron add --schedule "0 8 * * *" --task "meerkatta-daily-monitor" --label "Meerkatta Knowledge Monitor"
```

The monitor reads your student's profile (`counseling_state.md`) and runs targeted searches. Updates are logged in `references/knowledge-updates.md`.

## Differences from Original Beacon (upstream)

- Adapted for OpenClaw's skill system (runs via chat channels, not Claude Code terminal)
- Chat-friendly formatting (shorter responses, no wide tables, mobile-optimized)
- Uses OpenClaw tools (read/write/web_search/web_fetch) for file operations and research
- **New: Daily knowledge monitor** — cron-based auto-updates for deadlines, policy changes, and approaching milestones
- **New: Multi-student architecture** — separate agents per student with personalized SOUL.md
- **New: Parent handoff flow** — channel-based identity detection with trust-based access control
- **New: Templates** — starter SOUL.md and USER.md for quick per-student setup
- Same counseling logic, frameworks, and reference materials

## Credits

Original project: [Beacon](https://github.com/00derek/Beacon) by [@00derek](https://github.com/00derek)

## License

[MIT License](LICENSE) — same as original
