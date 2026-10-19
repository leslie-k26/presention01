# SolarWinds 2020 — spoken script

Lucas Krawczak · ~30 seconds · 84 words

---

In 2020, nobody hacked SolarWinds' software. They hacked the machine that built it.

Attackers slipped a backdoor into Orion before it compiled, so the update shipped
signed, valid, and trusted. Eighteen thousand organizations installed it. Nine US
federal agencies got breached. It went unnoticed for nine months.

Every check we tell developers to run, passed. The signature was real. The hash
matched.

So here's the lesson: you don't just inherit your dependencies' code. You inherit
their build server.

---

Timing note: read at a normal pace this lands at 28–32 seconds. If we are over
budget, cut "The signature was real. The hash matched." and it drops to ~25.
