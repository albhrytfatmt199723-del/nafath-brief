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
Cybersecurity
Data
Misconception in My Track
Open Question
