# Video Script

Target runtime 2:30–3:00. Timings from Discussion #4.

| Segment | Time | Who |
|---|---|---|
| Intro | ~0:15 | Leslie |
| Equifax 2017 | ~0:30 | Danielle |
| SolarWinds 2020 | ~0:30 | Lucas |
| EY data breach 2026 | ~0:30 | Chris |
| Google Gemini hacked 3 companies 2026 | ~0:30 | Eder |
| Conclusion | ~0:15 | Leslie |

Write your spoken lines under your heading. Read it out loud and time it before
committing — 30 seconds is roughly 75–85 words.

---

## Intro — Leslie

Hi, I’m Leslie. Here with Danielle, Lucas and Eder. And you’re here for one reason:

Imagine waking up one morning and finding out that a company you trusted has exposed your personal information to hackers. Your name, your address, even your financial details. And the worst part? You did nothing wrong.

2017, there’s Equifax, 2020 SolorWinds and now 2026 with Google’s Gemini AI making the headlines.

So, what happened? And what can we do to prevent small errors from becoming massive disasters?

Time to look at three major cyber security incidents and learn from them, starting with Equifax.

## Equifax 2017 — Danielle

In 2017, Equifax, one of America's three major credit bureaus, experienced a data breach. Hackers exploited an Apache Struts vulnerability between May and July, despite a security patch being available in March. The breach affected approximately 147 million individuals. In July 2019, Equifax agreed to a settlement of at least 575 million dollars. This incident emphasizes the importance of timely software updates, and effective vulnerability management.

## SolarWinds 2020 — Lucas

In 2020, hackers didn't break SolarWinds' software. They broke the machine that builds it.

SolarWinds makes Orion, a tool thousands of companies use to watch their networks. Attackers hid a backdoor in Orion while it was being built, so the update shipped with SolarWinds' official digital signature, the stamp that proves it's genuine.

Up to eighteen thousand organizations installed it. Nine US federal agencies were breached, and nobody noticed for nine months.

The lesson: trusting your vendor isn't enough. Protect your build pipeline like production.

## Google Gemini hacked 3 companies 2026 — Eder

In 2026, a cybersecurity report described how Google's Gemini AI accessed the systems of three companies during testing. The incident raised concerns about security controls and how AI agents are tested. When test environments are not properly isolated and credentials are exposed, an AI agent may reach systems it should not access. The key lesson for developers is to isolate testing environments, protect passwords and credentials, and give AI agents only the permissions they need. AI tools must be tested carefully before they are allowed to interact with real systems.


## Conclusion — Leslie

So, we’ve covered three cybersecurity incidents, from unpatched software to AI systems taking actions on their own.

Here’s 5 lessons learned:

1: Keep software updated.

2: Protect your credentials.

3: Limit permissions.

4: Test for failure.

5: Monitor and prepare.

Security isn’t an afterthought. Build it in early, test it continuously, and maintain it throughout the software lifecycle.

So, next time you think, “It’s probably fine,” remember the 147 million people affected by the Equifax breach.

Thanks for watching!
