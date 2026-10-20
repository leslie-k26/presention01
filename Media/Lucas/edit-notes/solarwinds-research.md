# SolarWinds 2020 — research notes

Lucas Krawczak · segment 3 · ~30 seconds

Following the four-point format from discussion #4.

## 1. What happened

December 2020. Attackers got into SolarWinds' **build system** and planted a
backdoor (SUNBURST) inside Orion, their network monitoring product. The poisoned
update shipped through the normal release channel, signed with SolarWinds' own
certificate. Customers installed it the way they install any update.

Around 18,000 organizations downloaded the trojanized build. A much smaller set,
roughly 100 companies and about 9 US federal agencies, got actively exploited
afterwards. US government attributed it to Russia's SVR.

## 2. Root cause

Not a bug in the product. The **pipeline that built the product** was compromised.

That is the part that matters for us. Every control that is supposed to tell you
software is safe still passed: the update was signed, the certificate was valid,
the vendor was trusted, the hash matched what SolarWinds published. All of it was
true and all of it was useless, because the compromise happened upstream of the
signature.

They also sat undetected for months. Initial access traces back to 2019, the
backdoored builds went out around March to June 2020, and nobody caught it until
FireEye found it in their own network that December.

## 3. Impact

- ~18,000 orgs received the backdoored update
- ~100 companies and ~9 US federal agencies actually exploited
- Treasury, Commerce, Homeland Security, State, Energy among them
- Roughly 9 months of dwell time before anyone noticed
- SolarWinds' stock dropped about 40% in the days after disclosure

## 4. Lesson for developers

Your dependencies are not just the code you pull in. They are also every build
server that produced it.

Practical version: lock down CI like production, give build agents the least
privilege they can function with, and keep an SBOM so that when a vendor gets
breached you can answer "are we affected" in minutes instead of weeks.

## Sources

- CISA Emergency Directive 21-01 — https://www.cisa.gov/news-events/directives/ed-21-01-mitigate-solarwinds-orion-code-compromise
- Mandiant/FireEye SUNBURST writeup — https://cloud.google.com/blog/topics/threat-intelligence/evasive-attacker-leverages-solarwinds-supply-chain-compromises-with-sunburst-backdoor/
- GAO summary of the incident — https://www.gao.gov/products/gao-22-104746

## Note for the team

Numbers above are the widely reported ones. I will re-verify each against the
primary sources before we record, and I will flag anything I cannot confirm
rather than say it on camera.

The "solarwinds123" password story gets repeated a lot. It was real, but it was a
separate FTP server credential and was **not** confirmed as the initial access
vector, so I am leaving it out of the script. It is a good story and a bad fact.
