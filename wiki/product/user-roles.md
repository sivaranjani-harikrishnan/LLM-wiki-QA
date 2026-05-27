# Product: User Roles

**Summary**: HeySales has five user roles with different levels of access to creation, management, and reporting features.

**Sources**: Multiple ACs and test case CSVs from `raw/`

**Last updated**: 2026-05-25

---

## Roles and access levels

| Role | HeySales access | Create/Publish content | Settings / Scorecards | Reports |
|---|---|---|---|---|
| Admin | Full | Yes | Yes | Yes |
| Content Publisher | Full | Yes | Yes (Scorecards only) | Yes |
| Normal User (Learner) | My Space + Explore | No | No | Own only |
| BI Analyst | No creation | No | No | Yes (read-only) |
| Deactivated users | None | No | No | No |

## Role-specific behaviours

### Admin
- Can access all Settings options including the Scorecard settings page
- Can create, edit, publish, and delete Courses, Podcasts, and Simulations
- Can assign learners to content
- Can view all learner reports
- Can manage integrations (Zoom, HubSpot, MS Dynamics) at their user level (HubSpot) or as account-level admin (MS Dynamics)

### Content Publisher
- Same creation and management access as Admin
- Has access to the Scorecard settings page
- Cannot access Viewer settings or account-level configuration

### Normal User (Learner)
- Sees assigned content in "My Space"
- Can self-enrol in published content via "Explore"
- Can complete and retake simulations, courses, and podcasts
- Has access to Let's Learn (Microlearning) module
- Reports from their own calls are private

### BI Analyst
- Cannot create content
- Cannot see the Scorecard settings option
- Has read-only access to reports

## Scorecard settings access

Only **Admin** and **Content Publisher** roles see the Scorecard option in Settings.
Normal Users and BI Analysts do not see this option even when HeySales is enabled. (source: `Custom Scorecards - Simulation creation (1).csv` TC0001–TC0003)

## HeySales enablement guard

If HeySales is **not enabled** on the account, no user of any role sees the Scorecard option or any HeySales-specific UI. (source: `Custom Scorecards - Simulation creation (1).csv` TC0003)

## Deactivated users

Deactivated users are automatically excluded from due-date reminder emails. (source: `Due date and reminder notifications - Sheet1.csv`)

## Related pages

- [[heysales-overview]]
- [[custom-scorecards]]
- [[due-date-notifications]]
