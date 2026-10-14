Version: NAFATH-V4

Track: Software

## Overview

Securing a national service requires more than protecting its own application code. It depends on third-party libraries, AI models, mobile apps, internet routing, and data records, each of which can introduce security risks. Software practices separate configuration from code and protect credentials. AI security addresses attacks that manipulate training data or model inputs. Mobile security standards help developers verify protections for sensitive information and communications. Network routing protections such as RPKI reduce certain risks from unauthorized route announcements. Cybersecurity measures help organizations identify and remediate vulnerabilities such as Log4Shell. SBOMs document software components and dependencies, helping teams identify affected systems when vulnerabilities emerge. Together, these practices improve visibility and support a coordinated response to supply-chain threats.

## Software

The Twelve-Factor App methodology recommends separating deployment-specific configuration and secrets, such as database credentials and API keys and hostnames, from application code by storing them in environment variables. This improves security, flexibility and portability across development, staging and production environments while reducing the possibility of accidental exposure of the credentials through source control.

Resource: The Twelve-Factor App - Config - https://12factor.net/config

## AI

Adversarial attacks on machine learning systems are categorized into evasion attacks, poisoning attacks, and exploratory attacks. Evasion attacks occur during the inference phase, after the model is trained, where attacker manipulate input data to mislead the model without altering it. Poisoning attacks happen during training, involving the injection of malicious data to corrupt the model's learning process. Finally, exploratory attacks aim to gather information about the model to identify weaknesses for future exploits.

Resource: Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://www.nist.gov/publications/adversarial-machine-learning-taxonomy-and-terminology-attacks-and-mitigations-0

## Mobile

The OWASP Mobile Application Security Verification Standard (MASVS) states essential security and privacy requirements for Android and iOS apps across storage, cryptography, authentication, network communication, platform interaction, code quality, resilience, and privacy. It’s used as a guide for developers in secure design, and for testers who implemented controls using the OWASP Mobile Application Security Testing Guides. Security testing profiles like MAS-L1, MAS-L2, and MAS-R, customize assessments based on application’s risk. Compliance reduces security risks but doesn’t ensure complete protection.

Resource: OWASP Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
