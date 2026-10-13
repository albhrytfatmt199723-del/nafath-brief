Version: NAFATH-V4
Track: Software

Overview
A national service provider depends on software, AI models, mobile applications, and internet connectivity to deliver reliable services. Each part of this system can introduce security risks if it is not properly verified. Software configuration and secrets must be managed securely to prevent unauthorized access. AI models need protection against attacks that manipulate their inputs or training data. Mobile applications should be tested against recognized security standards. Internet routing must also be protected because route hijacking can redirect traffic to unintended destinations. Cybersecurity practices help identify and fix vulnerabilities before attackers can exploit them. Finally, a Software Bill of Materials (SBOM) helps organizations understand which components their software contains and respond to supply-chain risks. Together, these six fields support a more secure and trustworthy technology environment.

Software
The Twelve-Factor App methodology recommends storing configuration separately from application code, commonly in environment variables. Passwords, API keys, and database credentials should not be committed to a repository because other people may gain access to them. Separating configuration from code also makes it easier to use different settings for development and production. If a secret is exposed, developers should revoke or rotate it and investigate where it was disclosed.

Resource: The Twelve-Factor App - Config - https://12factor.net/config

AI
Adversarial machine learning includes several attack categories, particularly evasion and poisoning. Evasion attacks manipulate inputs at the time a model is used, potentially causing incorrect predictions without changing its training data. Poisoning attacks target training data or the learning process to influence the model’s behavior. Understanding this difference helps organizations identify risks throughout the AI lifecycle and choose suitable testing, monitoring, and protective measures.

Resource: NIST - Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security requirements for mobile applications. It covers areas such as secure storage, cryptography, authentication, network communication, and platform interaction. Developers can use MASVS to establish security requirements, while the Mobile Application Security Testing Guide (MASTG) provides practical testing guidance. Together, these resources help teams assess whether an application meets relevant security expectations and identify weaknesses before release.

Resource: OWASP - Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/


Networking
BGP route hijacking occurs when an autonomous system announces incorrect internet routing information, potentially causing traffic to follow an unintended path. Resource Public Key Infrastructure (RPKI) helps networks validate whether an autonomous system is authorized to originate a particular IP prefix. However, RPKI origin validation does not verify the entire AS path or prevent every routing attack. Networks must also configure routing policies and monitor suspicious announcements.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811

Cybersecurity
Log4Shell (CVE-2021-44228) was a critical vulnerability in Apache Log4j 2, a widely used Java logging library. Under vulnerable conditions, an attacker could exploit specially crafted input to trigger remote code execution on an affected system. Its widespread use and potential for severe compromise made it especially dangerous. Organizations should upgrade to a fixed Log4j version appropriate to their environment and verify that vulnerable applications are no longer exposed.

Resource: Apache Log4j Security Vulnerabilities - https://logging.apache.org/log4j/2.x/security.html

Data
A Software Bill of Materials (SBOM) is a structured inventory of the components used to build a software product. It helps organizations identify dependencies and assess whether known vulnerabilities affect their systems. The NTIA identifies minimum elements including supplier name, component name, component version, other unique identifiers, dependency relationships, the SBOM data author, and a timestamp. Maintaining an accurate SBOM improves software supply-chain visibility and supports vulnerability response.

Resource: NTIA - The Minimum Elements for a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom


Misconception in My Track
A common misconception in software development is that storing passwords and API keys in source code is safe as long as the GitHub repository is private. This is incorrect because repository access can change, and secrets may be exposed through sharing or accidental disclosure. The Twelve-Factor App methodology recommends separating configuration from code and storing configuration in the environment. Developers should avoid hard-coding secrets and use appropriate secret-management practices. The evidence for this correction is in the “III. Config” section of The Twelve-Factor App, which explains why configuration should be separated from code.


Open Question
How can software development teams manage API keys and database credentials securely across development, testing, and production environments while preventing accidental exposure?


