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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
