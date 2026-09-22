---
name: senior-agent-lifecycle
description: Senior engineering lifecycle for AI agents — spec plan build test review ship. Trigger on /spec /plan /build /test /review /ship /webperf /code-simplify /constraints build auto feature implementation PRD task breakdown code review ship production TDD or when building non-trivial software. Upgraded from addyosmani/agent-skills with Beig-Rules lab gates security ui-craft and bilingual ship rules.
---

# Senior Agent Lifecycle (Pro)

Upgraded production pack inspired by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills). Encodes senior-engineer workflows so the agent does **spec → plan → build → test → review → ship** instead of coding first.

**Attribution:** Upstream concepts and lifecycle mapping from Addy Osmani's agent-skills (MIT-style open skills). This skill is a condensed, Grok-native, lab-integrated upgrade — not a verbatim copy.

## Core rule

No non-trivial implementation without a short written target (spec or task card). No merge/ship without a five-axis pass and a rollback idea.

## Intent → phase map (auto)

| User intent | Phase / action |
|-------------|----------------|
| Vague idea, "interview me", unclear ask | **Interview** then **Spec** |
| New feature / product / module | **Spec** → **Plan** → **Build** |
| "Plan" / breakdown / tasks | **Plan** |
| "Build" / implement / `/build auto` | **Build** (+ TDD per task) |
| Bug / error / flaky | **Debug** (repro first) |
| API design | **API design** gates |
| UI / frontend / charts | **UI** + load `ui-craft-pro` |
| Review / PR / before merge | **Review** (five axes) |
| Security concern | **Review** + `security-audit` |
| Perf / Core Web Vitals | **Webperf** |
| Simplify / clean | **Simplify** |
| Deploy / launch / Pages / packages | **Ship** + lab package rules |

## Operating behaviors (always)

1. **Surface assumptions** before non-trivial work — numbered list, invite correction.
2. **Stop on confusion** — name conflict, ask, do not guess silently.
3. **Push back** with concrete downside + alternative; accept informed override.
4. **Simplicity** — prefer boring solutions; delete abstractions that do not earn complexity.
5. **Scope discipline** — touch only what the task requires.
6. **Verification over claims** — "tests pass" / "deployed" only after evidence (command output, URL 200, etc.).

## Phase playbooks

### Interview (underspecified)

Ask **one** high-value question at a time until ~90% confidence. Prefer decisions that change architecture, data, or security. Do not dump a questionnaire.

### Spec

Produce a short PRD before code when the change is multi-file, multi-hour, or architectural:

- Goal / non-goals
- Users and success metrics
- Capability map (if multiple modules)
- Acceptance criteria (testable)
- Boundaries (out of scope)
- Risks and open questions

Gate: human accepts or amends before Plan.

### Plan

Break into **atomic tasks** (each verifiable in one pass):

- Ordered list with dependencies
- Per task: files likely touched, test idea, done-when
- Flag risky tasks (auth, money, migrations, public deploy)

`/build auto` equivalent: after plan approval, execute tasks sequentially without waiting between successes; **pause** on failure, security risk, or missing credential.

### Build (incremental + TDD)

For each task:

1. Write or update failing test / acceptance check when feasible
2. Implement minimal code to pass
3. Refactor if needed
4. Verify (syntax, unit, smoke URL, screenshot, etc.)
5. Commit-sized change conceptually (even if single push)

Never batch unrelated features in one opaque dump.

### Debug

1. Reproducible failure statement
2. Narrow locus (bisect, log, isolate)
3. Fix + regression check
4. No "drive-by" refactors in the same change unless required

### Review (five axes)

Before calling work done or merging:

| Axis | Ask |
|------|-----|
| Correctness | Matches acceptance? Edge/error paths? |
| Readability | Names, structure, dead code? |
| Architecture | Fits patterns? Dependency direction? |
| Security | Injection, secrets, authz, XSS, unsafe HTML? |
| Performance | Obvious N+1, huge payloads, main-thread jank? |

Standard: approve when it **improves** health and meets acceptance — not when perfect.

Compose with `security-audit` for threat-shaped changes; independent verification mindset (do not rubber-stamp self-written code).

### Simplify

Prefer deletion and flattening over new helpers. If two paths do the same thing, keep one.

### Ship

Pre-launch:

- [ ] Acceptance criteria met with evidence
- [ ] Tests / syntax checks green where they exist
- [ ] No secrets in repo
- [ ] Rollback path named (revert commit, previous image, feature flag)
- [ ] Observability: at least how you will know it broke

**Beig-Rules lab extensions:**

- Bilingual README (FA + EN) for user-facing upgrades
- Attribution to upstream inspiration
- Auto packages per stack (npm / GHCR) — see `ui-craft-pro`
- GitHub Pages: public repos free; private needs Pro — do not claim Pages works on private Free
- Official URL only after HTTP 200 proof

## Domain plugins (load companion skills)

| Domain | Companion |
|--------|-----------|
| Visual / CSS / Three.js / fonts | `ui-craft-pro` |
| Full security audit | `security-audit` |
| Platform / DevOps depth | `fullstack-devops-expert` |
| Lab self-improvement | `continuous-evolution` |

## Anti-patterns

- Coding before any acceptance criteria on multi-step work
- Claiming ship without URL or command evidence
- Mass-enabling Maven/NuGet on JS-only repos
- Silently enabling "private Pages" on Free plan
- Giant single commit that mixes format, feature, and refactor
- Sycophantic agreement with a harmful design

## Slash-style user phrases (treat as commands)

`/spec` `/plan` `/build` `/build auto` `/test` `/review` `/ship` `/webperf` `/code-simplify` `/constraints` — enter the matching phase immediately.

## Source

Upstream: https://github.com/addyosmani/agent-skills  
Local upgrade for Grok + Beig-Rules GitHub Upgrade Lab.
