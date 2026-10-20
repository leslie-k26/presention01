# Research Notes

Shared research for the presentation. Add your incident's notes under your own heading so we can see who wrote what.

Format per incident (keeps the video consistent — see Discussion #4):

1. What happened (when, who was affected)
2. Root cause (the software or dev failure)
3. Impact (numbers: people, money, systems)
4. Lesson for developers (one takeaway)

---

## Intro — Leslie

- This presentation examines four incidents:

  - SolarWinds cyberattack (2020)
  - Equifax data breach (2017)
  - EY data breach (2026)
  - Google Gemini hacking incidents (2026)

- These cases demonstrate how cybersecurity failures can result from compromised software supply chains, unpatched vulnerabilities, data security weaknesses, and inadequate security controls.

## Equifax 2017 — Danielle
# What Happened (When and Who were Affected)
Equifax is one of the three major credit reporting agencies in the United States. They collect and maintain sensitive financial and personal information used by lenders and other organizations to access creditworthiness

# Root Cause (Software or Development Failure)
 In 2017, Equifax experiences a major cybersecurity breach that compromised personal information of approximately 147 million individuals.The breach began in May 2017, as was officially discovered in July, before being publicly disclosed in September. Investigators determined that the attackers exploited a known vulnerability in Apache Struts a framework used for Java web applications.A security patch had previously been released in March the same year, Equifax's internal procedures failed to ensure it was applied to the affected system.Investigations also identified weaknesses in a network monitoring that delayed the detection of suspicious activity.

 # Impact (People, Money, and Systems)
 Approximately 147 million individuals had their personal information compromised. The incident created significant privacy and security concerns because said information (Social Security numbers, Names, etc.) are very difficult to replace and are a breach of confidentiality. Equifax subsequently faced regulatory investigations, lawsuits and a major settlement with federal and state authorities.

# Lessons for Developers
  The Equifax Data Breach Incident demonstrates that cybersecurity responsibilities extends far beyond the initial development of software. Organizations should regularly maintain their applications, monitor third-party frameworks and always verify that security updates have been successfully implemented 
  
  # Sources / References
  Federal Trade Commission. (2019, July 22). Equifax to pay at least $575 million as part of settlement with FTC, CFPB, and states related to 2017 data breach. https://www.ftc.gov/news-events/news/press-releases/2019/07/equifax-pay-575-million-part-settlement-ftc-cfpb-states-related-2017-data-breach
  
  U.S. Government Accountability Office. (2018, August 30). Data protection: Actions taken by Equifax and federal agencies in response to the 2017 breach (GAO-18-559). https://www.gao.gov/products/gao-18-559

## SolarWinds 2020 — Lucas

1. **What happened:** In 2020, attackers (attributed by the US government to Russia's SVR) broke into SolarWinds' build system and planted the SUNBURST backdoor inside Orion, its network-monitoring product. The poisoned updates shipped March–June 2020 through the normal release channel, signed with SolarWinds' own certificate.
2. **Root cause:** Not a bug in the product. The pipeline that *built* the product was compromised, upstream of the code signature, so every "is this safe?" check still passed.
3. **Impact:** Up to ~18,000 organizations (SolarWinds' SEC filing: "fewer than 18,000") installed the trojanized update; ~100 companies and 9 US federal agencies (incl. Treasury, Commerce, Homeland Security) were actively breached. Undetected ~9 months until FireEye found it in its own network in December 2020.
4. **Lesson for developers:** You inherit your vendors' build servers, not just their code. Lock down CI like production, give build agents least privilege, and keep an SBOM so "are we affected?" takes minutes, not weeks.

Full notes: `Media/Lucas/edit-notes/solarwinds-research.md`

## EY data breach 2026 — Chris

## Google Gemini hacked 3 companies 2026 — Eder

## Conclusion — Leslie

- Several common lessons emerge:
  - Timely patching: Keep software and dependencies updated.
  - Secure development: Identify and fix vulnerabilities throughout the software development lifecycle.
  - Access control: Apply the principle of least privilege and protect credentials
  - Thorough testing: Test software, configurations, and AI systems in isolated environments.
  - Continuous monitoring: Detect suspicious activity and respond quickly to potential breaches.

- Developers' decisions can help prevent vulnerabilities from becoming major incidents.
- Final message: Security should be built into software from the beginning, not added after an incident occurs.
