# Missfix — Project Brief

Use together with the *Aquila Digital — Mobile & Web App Build Standards*. This brief is the product source of truth; anything not listed under Confirmed is not decided.

## 1. Project overview
Missfix is an application for Aquila Digital LLC. A practice-session companion for the driving range: log your shots, find the pattern in your misses (for example, the 7-iron misses right), and get one drill to work on.

- **Platform scope:** iOS (assumed: see below).
- **Primary users:** Golfers who hit balls at the range without a clear idea of what to fix.
- **Primary user outcome:** Leave the range knowing your main miss and the one drill to work on next.

## 2. Confirmed requirements
- Standalone app. Selected from the 2026-10-14 brainstorm as "Range Day"; renamed Missfix because "Range Day" is already an App Store title.
- Core loop: log shots → find the pattern → one drill.
- Strokes Gained features and any GolfCaddie integration are later, separate work.

## 3. Reasonable assumptions (change freely)
- iOS first, SwiftUI, iOS 17+.
- Shot logging is manual and quick (club plus where the shot went), because a range has no course geometry. Auto-detection is not assumed.
- Pattern-finding is deterministic and inspectable (counts and tendencies per club). Any language model only rephrases a result that was already computed.
- Drills come from a small curated library written in plain language, not invented per user.
- All data stays on the device; no account.

## 4. Open questions (decide before building the affected part)
- How are shots logged: tap-per-shot with a miss-direction picker, voice, or both? What is the minimum data per shot?
- How many shots are needed before a pattern is shown? Below that, the app should say there is not enough data.
- Who writes and approves the drill library, and how are drills matched to a pattern?
- Is launch-monitor or Apple Watch input wanted in v1? (Not assumed.)
- Relationship to the golf caddie app: fully separate, or an optional import/export later? No shared code is assumed.
- Pricing model.

## 5. Out of scope
- Swing analysis from video.
- Strokes Gained.
- Social features and leaderboards.
- Course play and GPS distances.

## 6. Project context
| Item | Value |
|---|---|
| Project type | Mobile app |
| Platform | Swift / SwiftUI, iPhone (assumed) |
| Backend | NONE |
| Database | LOCAL |
| Authentication | NONE |
| Hosting / deployment | App Store |
| Analytics | NONE |
| AI / ML | NONE or LOCAL (rephrasing only) |
| Sensitive data classes | USER-ENTERED shot data (club, result). No location or camera in v1 unless decided otherwise. |
| Data processing location | ON-DEVICE |

## Notes
- Do not present a pattern as fact below the minimum sample size. Show how many shots it is based on.

## 7. Documents to keep (per the build standards)
README.md · SECURITY.md · ARCHITECTURE.md · PRIVACY.md · TESTING.md · CHANGELOG.md · .env.example (names only)
