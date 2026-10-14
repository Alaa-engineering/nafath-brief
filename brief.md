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

The Border Gateway Protocol (BGP) enables networks to advertise internet traffic routes; BGP route hijacking occurs when an Autonomous System (AS) advertises unauthorized IP address prefixes, leading to traffic redirection, data interception, or service disruption. Resource Public Key Infrastructure (RPKI) reduce this risk by allowing route origin validation using cryptographically signed Route Origin Authorizations (ROAs). However, RPKI does not check the entire AS path, or stop all route leaks and manipulations, requiring additional security measures.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://datatracker.ietf.org/doc/html/rfc6811

## Cybersecurity

Log4Shell (CVE-2021-44228) was a critical remote code execution (RCE) flaw in Apache Log4j 2 open-source Java logging library. Attackers could use vulnerable configurations by submitting crafted input that triggered unsafe Java Naming and Directory Interface (JNDI) lookups, potentially enabling unauthorized code execution. The flaw resulted from unsafe message lookup substitution combined with JNDI functionality. The Apache Software Foundation addressed the issue through successive security patches that disabled dangerous JNDI lookups by default and restricted supported network protocols.

Resource: Apache Log4j Security Vulnerabilities - https://logging.apache.org/security.html

## Data

Software Bill of Materials (SBOM) is an organised, machine-readable list of software components, libraries, modules, and third-party dependencies. It improves software transparency by helping companies in identifying susceptible components, evaluating licensing risks, and swiftly addressing newly identified vulnerabilities. The NTIA minimal elements include supplier and component names, versions, unique identifiers, dependency connections, the SBOM author, and timestamps. An accurate SBOM does not ensure that software components are secure or free of vulnerabilities, even when it helps vulnerability management

Resource: The Minimum Elements for a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom

## Misconception in My Track

It's a common misperception that if the repository is private, hardcoding secrets in source code is acceptable. However, credentials can be exposed by code sharing, future publications, or unintentional access to secret repositories. Deleting secrets from previous iterations in subsequent commits does not remove them. According to the Twelve-Factor App “Store config in the environment” section, developers should separate configuration from code and inject credentials at runtime using environment variables or centralised secrets-management tools. Appropriate access limits and least-privilege permissions are essential since repository privacy cannot guarantee credential security on its own.

## Open Question

How can development teams securely manage and rotate application secrets across development, testing, and production environments without exposing credentials or disrupting services?
