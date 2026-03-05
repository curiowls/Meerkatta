# Watch List

Auto-populated from the student's `counseling_state.md`. Defines what the daily monitoring cron should search for.

## How This File Works

- **Auto-updated** whenever `counseling_state.md` changes (college list, testing plans, timeline milestones)
- **Read by the cron job** to generate targeted searches
- **Do not edit manually** — it's regenerated from student state

## Watch Categories

### Schools
<!-- Populated from College List section of counseling_state.md -->
_No schools on list yet._

### Testing
<!-- Populated from Testing section -->
- SAT registration deadlines
- ACT registration deadlines
- AP exam registration deadlines

### Financial Aid
<!-- Always monitored -->
- FAFSA opening date and deadline changes
- CSS Profile deadline changes
- Federal student aid policy changes

### Scholarships
<!-- Populated from Financial section -->
_No scholarships tracked yet._

### Summer Programs
<!-- Populated from Summer Experiences section -->
_No summer programs tracked yet._

### Timeline Milestones
<!-- Populated from Timeline Status — milestones coming up in next 30 days -->
_No upcoming milestones yet._

## General Monitoring (Always Active)

These are checked regardless of student profile:

- Common App opening date and any platform changes
- Coalition App changes
- UC application system changes
- Major FAFSA/financial aid policy shifts
- SAT/ACT format or policy changes
- Test-optional policy changes at top-100 schools
- National scholarship deadlines (Gates, QuestBridge, Coca-Cola, etc.)
