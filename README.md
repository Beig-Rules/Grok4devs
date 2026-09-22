# Grok4devs

**Senior engineering skills for AI coding agents** — optimized for Grok and production labs.

Lifecycle: **Spec → Plan → Build → Test → Review → Ship**

Inspired by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills), rewritten as a condensed Grok-native pack with stronger gates, verification-before-claims, and lab-ready conventions.

---

## English

### What this is

AI agents code fast and skip the surrounding discipline. **Grok4devs** packages the workflows senior engineers use so agents follow a gated path instead of guessing.

| Phase | Trigger examples | Principle |
|-------|------------------|-----------|
| Spec | `/spec`, new feature, unclear requirements | Spec before code |
| Plan | `/plan`, task breakdown | Small atomic tasks |
| Build | `/build`, `/build auto` | One slice + TDD |
| Test / Debug | `/test`, bugs | Proof over claims |
| Review | `/review` | Five-axis quality |
| Ship | `/ship`, deploy | Evidence + rollback |

### Install (Grok / local skills)

Copy into your agent skills directory:

```bash
# Example path used by this lab
mkdir -p ~/.grok/skills/senior-agent-lifecycle/references
cp skills/senior-agent-lifecycle/SKILL.md ~/.grok/skills/senior-agent-lifecycle/
cp skills/senior-agent-lifecycle/references/* ~/.grok/skills/senior-agent-lifecycle/references/
```

Or clone and point your agent at `skills/senior-agent-lifecycle/`.

### Slash-style commands

Treat these phrases as lifecycle entry points:

`/spec` `/plan` `/build` `/build auto` `/test` `/review` `/ship` `/webperf` `/code-simplify` `/constraints`

### Five-axis review

Correctness · Readability · Architecture · Security · Performance

### Upgrades vs upstream

- Single orchestrator skill (token-efficient) instead of 25 separate files for default path
- Explicit **verification evidence** required before “done / deployed”
- Lab hooks: bilingual docs, package auto-decision, GitHub Pages plan limits
- Composes with security-audit and UI craft skills when present
- Anti-sycophancy and scope discipline baked in

### License & attribution

- Copyright © Beig-Rules / Grok4devs contributors
- Upstream inspiration: [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) — not a verbatim copy
- Distributed for use with AI coding agents; respect upstream license terms for any borrowed wording

---

## فارسی

### این چیست؟

ایجنت‌های کدنویس سریع کد می‌زنند و مرحلهٔ مشخصات، برنامه و ریویو را رد می‌کنند. **Grok4devs** گردش‌کار مهندس ارشد را فشرده کرده تا مسیر **مشخصات → برنامه → پیاده‌سازی → تست → ریویو → انتشار** رعایت شود.

### نصب

پوشهٔ `skills/senior-agent-lifecycle/` را در مسیر skills ایجنت خود کپی کنید (مثلاً `~/.grok/skills/`).

### دستورات

`/spec` `/plan` `/build` `/build auto` `/test` `/review` `/ship`

### ریویو پنج‌محوره

صحت · خوانایی · معماری · امنیت · کارایی

### تفاوت با منبع الهام

- یک اسکیل هماهنگ‌کننده به‌جای ده‌ها فایل جدا
- ادعای «تمام شد / دیپلوی شد» فقط با **شاهد** (خروجی دستور، HTTP 200 و …)
- مناسب لَب ارتقای پروژه و قوانین مستندات دوزبانه

### کپی‌رایت

- © Beig-Rules
- الهام از [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) با بازنویسی و بهینه‌سازی؛ کپی تحت‌اللفظی نیست

---

## Repo layout

```
skills/senior-agent-lifecycle/SKILL.md
skills/senior-agent-lifecycle/references/lifecycle-cheatsheet.md
README.md
LICENSE
NOTICE.md
```
