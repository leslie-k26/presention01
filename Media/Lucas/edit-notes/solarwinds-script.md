# SolarWinds 2020 — spoken script

Lucas Krawczak · ~30 seconds · 85 words

Revised after Leslie's review on #10: explains what Orion is and what a signed
update means, drops "the hash matched" (too much jargon for 30 seconds).

---

In 2020, hackers didn't break SolarWinds' software. They broke the machine that builds it.

SolarWinds makes Orion, a tool thousands of companies use to watch their networks.
Attackers hid a backdoor in Orion while it was being built, so the update shipped
with SolarWinds' official digital signature, the stamp that proves it's genuine.

Up to eighteen thousand organizations installed it. Nine US federal agencies were
breached, and nobody noticed for nine months.

The lesson: trusting your vendor isn't enough. Protect your build pipeline like production.

---

## Visual cues for the edit (@leslie-k26)

| Line | On screen |
|---|---|
| "the machine that builds it" | Simple diagram: code → **build server** (red, compromised) → update → customers |
| "Orion ... watch their networks" | Label: *Orion = network monitoring software* |
| "official digital signature" | Padlock / ✔ "Signed by SolarWinds" badge over the infected update |
| "Eighteen thousand ... nine months" | Stat cards: **up to 18,000** installed · **9** federal agencies · **9 months** undetected |
| "Protect your build pipeline" | Takeaway card, same style as the other segments |

Timing note: read at a normal pace this lands at ~30 seconds. If we are over
budget, cut "a tool thousands of companies use to watch their networks" to
"a network monitoring tool" and it drops to ~27.
