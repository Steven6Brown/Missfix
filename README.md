<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="branding/missfix-wordmark-on-dark.png">
    <img src="branding/missfix-wordmark-on-light.png" alt="Missfix" width="460">
  </picture>

  <p><strong>Find your miss. Fix it.</strong></p>

  <img src="https://img.shields.io/badge/status-In%20design-F2A33A?style=flat-square" alt="status"> <img src="https://img.shields.io/badge/platform-iOS%2017%2B-111827?style=flat-square" alt="platform"> <img src="https://img.shields.io/badge/license-proprietary-555555?style=flat-square" alt="license"> <img src="https://img.shields.io/badge/by-Aquila%20Digital%20LLC-14213D?style=flat-square" alt="Aquila Digital LLC">
</div>

> **Status: in design.** Missfix is a fully briefed and branded product concept. The plan, scope and open questions are documented; the app has not been built yet.

## The idea

A practice-session companion for the driving range: log your shots, find the pattern in your misses, and get one drill to work on.

- **For:** Golfers who hit balls at the range without a clear idea of what to fix.
- **Outcome:** Leave the range knowing your main miss and the one drill to work on next.

## How it will work

```mermaid
flowchart LR
  A["Log each shot: club + where it went"] --> B["Deterministic pattern-finder counts tendencies per club"] --> C["Main miss is identified once there is enough data"] --> D["One drill from a curated library is recommended"]
```

## Planned features

- Fast, manual shot logging built for the range
- Inspectable pattern-finding (counts and tendencies, not a black box)
- Small curated drill library in plain language
- Says "not enough data" until a pattern is real
- All data on-device, no account

## Tech plan

| Layer | Choice |
|---|---|
| Language / UI | Swift, SwiftUI (iOS 17+) |
| Analysis | Deterministic, on-device |
| Storage | Local |
| Backend | None |

## Privacy by design

All practice data stays on the device. No account.

## Open decisions

Tracked openly in [`docs/PROJECT_BRIEF.md`](docs/PROJECT_BRIEF.md). A few of the big ones:

- How are shots logged: tap-per-shot with a miss-direction picker, voice, or both? What is the minimum data per shot?
- How many shots are needed before a pattern is shown? Below that, the app should say there is not enough data.
- Who writes and approves the drill library, and how are drills matched to a pattern?
- Is launch-monitor or Apple Watch input wanted in v1? (Not assumed.)

## Brand

| | Name | Hex | Role |
|---|---|---|---|
| <img src="https://placehold.co/44x22/111827/111827.png" alt="#111827" /> | Night | `#111827` | Icon field, text, dark surfaces |
| <img src="https://placehold.co/44x22/FFFFFF/FFFFFF.png" alt="#FFFFFF" /> | White | `#FFFFFF` | Target rings, light surfaces |
| <img src="https://placehold.co/44x22/C6F432/C6F432.png" alt="#C6F432" /> | Fix Lime | `#C6F432` | Bullseye, correction arrow, key actions |
| <img src="https://placehold.co/44x22/FF6B35/FF6B35.png" alt="#FF6B35" /> | Miss Orange | `#FF6B35` | The miss, warnings |

**Mark.** A target with an orange miss off to one side and a lime arrow pulling it back to the bullseye: the miss, found and fixed.

**Voice.** Coach-like, specific and encouraging. Name the pattern in plain words ("your 7-iron misses right"), give one thing to work on, never a lecture.

Full logo set (mark, wordmark, app icon in light and dark) and the brand guide are in [`branding/`](branding/BRAND_GUIDE.md).

## Repository contents

```
docs/PROJECT_BRIEF.md   Confirmed requirements, assumptions, open questions, scope
branding/               Logo files and BRAND_GUIDE.md
```

## License

Proprietary. Shared publicly for portfolio and demonstration purposes only. See [LICENSE](LICENSE).

---

<div align="center">

Built by [Aquila Digital LLC](https://github.com/Steven6Brown) · *Per Aspera Ad Astra*

</div>
