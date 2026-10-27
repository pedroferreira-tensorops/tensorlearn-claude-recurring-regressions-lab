# Diagnosis

## Observed cause

CLAUDE.md listed three "previously agreed conventions" that contradict the current docs. Claude loads that file in every session, so each new session reintroduced the old code format and removed the cache.

## Evidence

docs/current-schema.md requires CUS- plus six digits; docs/status-design.md requires a 30-second per-customer cache; docs/testing.md names the full suite. The contract tests agree with the docs, not with CLAUDE.md.

## Targeted correction

Replaced only the three false conventions in CLAUDE.md with the current rules and kept the rest of the working agreement. Added a student regression test for the code format and the cache boundary.

## Fresh-session verification

Started a new Claude Code process, asked it to add a status helper, and checked it kept CUS- six-digit codes and the cache; the full suite passed.
