# Beacon (OpenClaw Edition)

🎓 An OpenClaw skill that turns your AI assistant into a college counselor. Guides high school students from freshman-year interest discovery through senior-year decisions — covering academic planning, extracurricular strategy, essay coaching, college list building, and financial aid. Chat with it on Telegram, Discord, or any OpenClaw channel.

Adapted from [Beacon](https://github.com/00derek/Beacon) by [@00derek](https://github.com/00derek).

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
cp -r Beacon ~/.openclaw/skills/beacon

# Or symlink it
ln -s /path/to/Beacon ~/.openclaw/skills/beacon
```

### Option 2: Clone directly into skills

```bash
cd ~/.openclaw/skills
git clone https://github.com/curiowls/Beacon.git beacon
```

Once installed, the skill auto-triggers when college prep topics come up. Or just type **kickoff** to start.

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

## Differences from Original Beacon

- Adapted for OpenClaw's skill system (runs via chat channels, not Claude Code terminal)
- Chat-friendly formatting (shorter responses, no wide tables, mobile-optimized)
- Uses OpenClaw tools (read/write/web_search/web_fetch) for file operations and research
- Same counseling logic, frameworks, and reference materials

## Credits

Original project: [Beacon](https://github.com/00derek/Beacon) by [@00derek](https://github.com/00derek)

## License

[MIT License](LICENSE) — same as original
