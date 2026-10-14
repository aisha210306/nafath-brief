Version: NAFATH-V1
Track: AI

## Overview

A secure national digital login service depends on several IT fields working together. Software standards define how users authenticate and how applications receive authorized access to government resources. Artificial intelligence can help identify suspicious login patterns, but its decisions must be evaluated for accuracy, bias, privacy, and security before deployment. Mobile security controls limit what the login application can access on a citizen’s device. Networking technologies, including encrypted DNS, can protect some parts of users’ internet activity, while cybersecurity measures strengthen authentication and reduce phishing risks. Data protection requirements guide how citizens’ personal information is collected, stored, used, and safeguarded. These areas must be designed as one coordinated system rather than separate features. For the AI component, the authority must assess risks using a recognized AI risk management framework before automatically flagging suspicious logins.

## Software
OAuth 2.0 and OpenID Connect (OIDC) serve different purposes in a government login service. OAuth 2.0 enables delegated authorization, allowing an application to access specific resources with permission. OpenID Connect adds an identity layer that helps verify the user's identity and authenticate the user. Therefore, OAuth is mainly used for authorized access, while OIDC is used for sign-in. Using the correct protocol separates identity verification from access permissions.

Resource: OpenID Foundation - How OpenID Connect Works - https://openid.net/developers/how-connect-works/

## AI
The authority should use the NIST AI Risk Management Framework (AI RMF 1.0) to assess the AI system before deployment. The framework includes four functions: Govern, Map, Measure, and Manage. The authority should identify potential risks, test the system’s accuracy, evaluate false alerts, and establish procedures to manage risks. It should also consider privacy, security, and fairness to reduce the chance of incorrectly flagging legitimate users as suspicious. AI decisions should be monitored and reviewed regularly.

Resource: NIST AI Risk Management Framework - https://airc.nist.gov/airmf-resources/airmf/5-sec-core/

## Mobile
An Android government login application should request runtime permissions only when they are needed for a specific feature. The app should explain why access is required and request permission when the user starts the relevant action. It must check whether permission has been granted and handle denial safely without unnecessarily blocking unrelated features. This approach gives users more control over private data and reduces unnecessary access to sensitive information.

Resource: Android Developers - https://developer.android.com/training/permissions/requesting

## Networking
DNS over HTTPS (DoH) sends DNS queries through an encrypted HTTPS connection between a device and a DNS resolver. This helps prevent other parties on the network from easily reading or modifying DNS requests. However, DoH does not encrypt all internet traffic or hide the user's IP address. The DNS resolver can still see the queries, and other information may reveal which services the user accesses.

Resource: Cloudflare - What is DNS over HTTPS? - https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/

## Cybersecurity
Phishing-resistant authentication helps protect government accounts against fake login pages and stolen passwords. Passkeys using FIDO2 or WebAuthn can resist phishing because authentication is tied to the legitimate website or service. Hardware security keys are another strong option. By contrast, SMS codes and ordinary one-time passwords can still be stolen or relayed through phishing. Multi-factor authentication improves security, but not every MFA method is phishing-resistant.

Resource: CISA - Implementing Phishing-Resistant MFA - https://www.cisa.gov/resources-tools/resources/implementing-phishing-resistant-mfa

## Data
Under Oman's Personal Data Protection Law (Royal Decree 6/2022), the authority must process citizens' personal data lawfully and transparently, collect only data needed for specified purposes, and protect it from unauthorized access or disclosure. It should provide required privacy information and obtain consent where the law requires it. The authority must also respect data-subject rights and follow applicable rules for processing sensitive data and transferring personal data outside Oman.

Resource: Oman Ministry of Transport, Communications and Information Technology - Personal Data Protection Law - https://www.mtcit.gov.om/ITAPortal/Pages/Page.aspx?NID=1736

## Misconception in My Track

## Open Question
