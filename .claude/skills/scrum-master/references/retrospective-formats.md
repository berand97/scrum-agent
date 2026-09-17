# Retrospective Formats

Every format follows: set the stage (5 min) → gather data (10–15 min) → group and vote (10 min) → decide actions (10–15 min) → close (5 min).
Always end with at most 3 actions, each with an owner and a due date, and review the previous retro's actions at the start.

When Azure DevOps data is available, open the retro with sprint facts: committed vs. delivered, carried-over items, scope added mid-sprint, open bugs, and cycle time.

## Start / Stop / Continue
- **When:** new teams or short retros.
- **Script:** "What should we start doing? Stop doing? Keep doing?" Silent writing, 3 notes per column, then a reading round.

## 4Ls (Liked / Learned / Lacked / Longed For)
- **When:** exploring team sentiment after an intense sprint.
- **Script:** "What I liked, learned, lacked, longed for." Group themes and vote on the 2 highest-impact "Lacked" / "Longed For" items.

## Sailboat
- **When:** discussing direction and risks.
- **Script:** draw the boat: **wind** (what drives us), **anchors** (what holds us back), **rocks** (risks ahead), **island** (the goal). Prioritize anchors and rocks.

## Timeline
- **When:** long sprints or sprints with many events.
- **Script:** a line with the sprint days; each person marks highs and lows with an emotion. Look for patterns (do lows match deployments, scope changes, blockers?).

## Fishbone / 5 Whys
- **When:** investigating a specific problem (incident, failed sprint).
- **Script:** write the problem; ask "why?" five times, or sort causes into People / Process / Tools / Environment / Requirements. Actions target the root cause, not the symptom.

## Output Template

```
Sprint <n> Retro — <format>

Sprint facts: <committed vs delivered, carry-over, bugs>
Previous actions: <done / pending>

Main themes:
- ...

Actions:
| Action | Owner | Due |
|---|---|---|
```
