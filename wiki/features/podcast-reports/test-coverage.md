# Test Coverage: Podcast Reports

**Summary**: 20 test cases covering podcast completion rate, total listen time, and avg listen time metric cards.

**Sources**: `Podcast Reports - Sheet1.csv`

**Last updated**: 2026-05-25

---

## Key TC groups

### Completion Rate (TC0001–TC0007)
- TC0001: Completion rate card shows completed / assigned
- TC0002: Replay does NOT increment completion count (completion counted once)
- TC0003–TC0007: Various scenarios with different learner counts and states

### Total Listen Time (TC0008–TC0013)
- TC0008: Total listen time card shows cumulative including in-progress and completed
- TC0009: Replay does NOT change total listen time
- TC0010: In-progress learners' time IS included
- TC0011–TC0013: Various replay and in-progress scenarios

### Avg Listen Time (TC0014–TC0020)
- TC0014: Avg listen time = total time / (started + completed learners)
- TC0015: Not-started learners are NOT included in denominator
- TC0016: Replay does NOT change avg listen time
- TC0017: In-progress learners ARE included in denominator
- TC0018–TC0020: Various combinations of started, in-progress, and completed learners

---

## Related pages

- [[overview]]
- [[podcasts]]
