# Knowledge Updates Log

Timestamped log of time-sensitive changes discovered by the daily monitoring cron. Newest entries first.

## Format

Each entry follows this structure:

```
### [DATE] — [CATEGORY]
**Relevance**: [Which part of the student's profile this affects]
**Source**: [URL or description]
**Summary**: [What changed]
**Action needed**: [Yes/No — and what to do if yes]
**Notified**: [Yes/No]
```

## Categories

- `DEADLINE_CHANGE` — Application, test, or scholarship deadline moved
- `POLICY_CHANGE` — Test-optional, admissions policy, financial aid rule change
- `FAFSA_UPDATE` — FAFSA/CSS Profile changes, opening dates, bugs, extensions
- `TEST_UPDATE` — SAT/ACT registration deadlines, format changes, new test dates
- `SCHOLARSHIP` — New scholarship opportunities or approaching deadlines
- `SUMMER_PROGRAM` — Application windows opening/closing for summer programs
- `SCHOOL_SPECIFIC` — Changes at a specific school on the student's list
- `GENERAL_ADMISSIONS` — Broad admissions trends or news worth knowing

---

<!-- Entries will be added below by the daily cron job -->
