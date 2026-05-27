# Audience Guide: New Hires

**Summary**: Start here if you are new to HeySales. This page gives you the mental model you need before diving into feature details.

**Last updated**: 2026-05-25

---

## Mental model: what HeySales does

HeySales turns the Paperflite platform into a sales training system. Sales managers create learning content; sales reps complete it; HeySales measures what they learned and how they perform on real calls.

**Three ways to learn:**
1. **Courses**: Structured multi-step programs (documents, quizzes, podcasts, simulations)
2. **Podcasts**: AI audio from uploaded documents — rep listens like a podcast
3. **Simulations**: Rep role-plays a call with an AI prospect and gets a scored report

**One way to measure real performance:**
- **Real Call Scoring**: Zoom calls with real prospects are scored automatically using the CRM integration

---

## Start here: read these pages first

1. [[heysales-overview]] — what the product is, how it's accessed, key modules
2. [[user-roles]] — who can do what (Admin, Content Publisher, Learner, BI Analyst)
3. [[learning-types]] — courses vs podcasts vs simulations vs microlearning

---

## Then read by the area you work in

**If you work in QA**: read [[for-testing]]

**If you work in Engineering**: read [[for-engineering]]

**If you work in Support**: read [[for-support]]

**If you work in Product / PM**: read [[for-pm]]

**If you work in Sales / Onboarding**: read [[for-onboarding]]

---

## Things that confuse almost everyone at first

### "What's the difference between Microlearning and Podcasts?"

Regular Podcasts are created by admins, assigned to learners, and visible in admin reports. Microlearning (Let's Learn) is private — every user creates their own articles and audio privately. Admins cannot see Microlearning content.

### "Why are there two types of CRM integration?"

HubSpot uses a USER-level Zoom connection (each rep connects their own Zoom). MS Dynamics uses an ACCOUNT-level Zoom connection (one for the whole company). This reflects how the two CRMs work.

### "What's an Elevator Pitch?"

It's a simulation variant where the rep delivers a timed monologue — no AI prospect responds. The rep speaks to the camera (video mode) or microphone (audio mode) and is scored on delivery.

### "What happens to a simulation if the scorecard is deleted?"

Nothing — existing simulations and their reports are unaffected. The deleted scorecard's data is preserved in historical reports. The account's default reverts to the Paperflite MEDDIC scorecard for future use.

### "Can I see if a Zoom call under 2 minutes was scored?"

For Zoom real calls: yes, a report is generated even for calls under 2 minutes. For simulation calls: no — calls under 2 minutes are marked as NA. This difference is intentional (different contexts).

---

## Related pages

- [[heysales-overview]]
- [[user-roles]]
- [[learning-types]]
