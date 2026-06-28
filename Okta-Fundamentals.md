# Jai Mahakal
# Okta Course Overview

## An Introduction to Modern Identity & Access Concepts
1. SSO (Single-Sign-On)
- Definition: One set of credentials → access to multiple apps.
- Use Case: Employee logs into Microsoft 365 once, then gets seamless access to Outlook, Teams, SharePoint.
- Industry Example: Google Workspace SSO across Gmail, Drive, Docs.
 
3. OAuth 2.0
- Definition: Delegated authorization — app gets limited access without sharing password.
- Use Case: A fitness app pulls your Google Calendar events after you grant permission.
- Industry Example: “Login with Facebook/Google” buttons on third-party apps.

5. OpenID Connect
- Definition: Authentication layer built on OAuth 2.0 — verifies who you are.
- Use Case: Logging into Slack with Google credentials, identity confirmed via OIDC.
- Industry Example: Social logins for apps like Spotify or Trello.

7. SAML (Security Assertions Markup Language)
- Definition: XML-based standard for exchanging authentication data between IdP and service provider.
- Use Case: Employee logs into Salesforce using corporate credentials via SAML.
- Industry Example: Enterprises using Okta + SAML for legacy apps.

9. SCIM (System for Cross-domain Identity Management)
- Definition: Standard for automated user provisioning/de-provisioning.
- Use Case: HR adds a new hire → accounts auto-created in Zoom, Slack, Jira.
- Industry Example: Okta SCIM integration with SaaS apps for lifecycle management.

11. Idps (Identity Providers)
- Definition: Services that manage authentication, authorization, and policies.
- Use Case: Okta or Azure AD acting as the “gatekeeper” for enterprise apps.
- Industry Example: Ping Identity, ForgeRock, Okta, Azure AD.

13. MFA (Multi-Factor Authentication)
- Definition: Requires two or more factors (password + OTP + biometrics).
- Use Case: Banking app asks for password + SMS OTP.
- Industry Example: Microsoft Authenticator, Duo Security.

15. Passwordless Authentication
- Definition: Eliminates passwords, uses biometrics or hardware keys.
- Use Case: Employee logs in with fingerprint or YubiKey.
- Industry Example: Windows Hello, FIDO2/WebAuthn adoption in enterprises.

16. RBAC (Role-Based Access Control)
- Definition: Access tied to job roles.
- Use Case: HR staff can view payroll data, but IT staff cannot.
- Industry Example: AWS IAM roles granting developers access to dev resources only.

18. PAM (Privileged Access Management)
- Definition: Extra security for admin/superuser accounts.
- Use Case: Database admin credentials stored in a secure vault, rotated automatically.
- Industry Example: CyberArk, BeyondTrust PAM solutions.

# Course Introduction

# Understanding Okta / What is Okta
- Okta is mainly an Identity Provider (Idp), capable to connect any application to any person.
- Remember that Okta is neitehr an Authentication nor an Authorization protocol, It's a product, it's a platform.
- What is Okta
  - Okta is a Cloud-native IAM from Day 1.
  - Built as a SaaS (not on-prem IAM like LDAP/AD), API-first, multi-tenant architecture.
  - Founded in 2009 with the name of SaaSure, and rebranded to Okta in 2010.
  - Typical pain point during in that era was Enterprises were rapidly adopting SaaS apps (Salesforce, Google Apps, etc.)
  - Traditional on-prem identity systems couldn't scale to cloud environments.
  - Acquired Auth0 in 2021.
  - Auth0 = Identity-as-a-Service (IDaaS) platform for Developers.
  - It provides authentication + authorization as a managed service so you dont have to build login/security yourself.
  - Okta evolved from SAML based SSO --> to --> API driven identity platform --> Zero Trust control plane covering workforce, customers, APIs & Infrastructure.
  -
# Why do we need Okta / What does Okta solve?
  - Historically we know that organizations use Active Directory as the single source of truth for their users.
  - AD is the main database that they use to prove a user is who he claims to be, which is not possible otherwise
  - Now, you have seen the massive adoption of SaaS apps around you, which brings flexibility, scalability, and agility.
  - Now, these SaaS apps have their own directories, which is not synced with your active directory, and cannot be either
  - you dont have a one SaaS app, you have 100 of them in use in your daily life.
  - so, these SaaS apps have their own directory which runs in the cloud
  - So, this makes this whole situation complex, cause the app which user need to access is hosted in the cloud, but the user profile is primarily configured in AD which is on-prem and also protected behind the organization Firewall, so this does not facilitiate this type of connection.
  - And because of this Users have to remember multiple usersnames/passwords for each of these SaaS apps.
  - Refer to this screenshot below:
  - <img width="802" height="507" alt="image" src="https://github.com/user-attachments/assets/f5e0d998-ed5e-4e9d-9cd9-9111428314c2" />
  - And as Okta is a cloud-native IAM, which comes right in between users and Apps, and work like a broker and facilitate cloud based identity service.
  - Refer to the screenshot below
  - <img width="775" height="511" alt="image" src="https://github.com/user-attachments/assets/80f8e64e-9a8c-4e94-880e-e6623f9a35c1" />




# Understanding Which Apps can be integrated with Okta
  - In today’s identity landscape, applications don’t all speak the same language — 
  - some rely on modern cloud-native protocols like OAuth 2.0, OpenID Connect, and SCIM, 
  - while others still depend on legacy standards such as SAML, LDAP, or RADIUS. 
  - Okta isn’t a protocol itself; it’s the identity platform that acts as a universal translator, 
  - It supports all of these standards so organizations can connect both their latest SaaS tools and their older enterprise systems under one secure umbrella.
  - In one line, Okta supports OIDC, OAuth 2.0, SCIM, SAML, LDAP & Radius.
  - Example of Modern protocols (OIDC, OAuth 2.0, SCIM)
    - Slack : OIDC for login + SCIM for user provisioning/deprovisioning
    - Zoom  : OIDC for login + SCIM for license management
   
  - Example of Legacy protocols (SAML, LDAP, RADIUS)
    - Salesforce : SAML for login + SCIM for provisioning
    - Workday : SAML for authentication + SCIM

# Understanding OIN (Okta Integration Network)
  - The Okta Integration Network is Okta's marketplace of pre-built connectors.
  - It works like a Universal Identity Hub that means Okta speaks whichever "language" the app requires. 
  - OIN is a technical backbone that makes Okta more powerful, scalable, and future-proof. 
  - It enables seamless integration with thousands of application using industry-standard protocols.
  - scale: over 8,000+ pre-built integrations available.
  - Supported protocols: OIDC, OAuth2.0, SCIM, SAML, LDAP, RADIUS.
  - Custom Integrations: Developers can build new connectors via Okta's App Integration Wizard (AIW)
		
# Understanding Okta Platform, & Accounts (Free, Trial, and Paid)

## Okta Developer Account - Overview
  - The Okta Developer Account is a free, forever‑available sandbox environment designed for developers, students, and learners to explore identity and access management. 
  - The Okta Developer Account is the best entry point for students, learners, and developers. 
  - You can practice SSO, OAuth/OIDC, SCIM, MFA, and passwordless authentication — all in a safe environment that mirrors enterprise features.
  - It provides hands‑on access to Okta’s core features without requiring a paid subscription.
  - Sign up at developer.okta.com
  - It provides a sandbox environment with limited users and apps. It's not production grade, therefore best for testing. 
  - Ideal for learning, testing integrations, and building proof-of-concepts.
  - when you sign up, Okta provisions your own tenant (e.g., your-org.okta.com) like (ravikmalhotra.okta.com

# How i created my account.
  - access https://www.developer.okta.com
  - <img width="1656" height="652" alt="image" src="https://github.com/user-attachments/assets/69c68eaa-6074-45b4-a6ca-806346057dd0" />
  - Click on 'Try Auth0 Platforms"
  - then provide the desired personal email ID in the Sign Up screen and click on Continue
  - Next you will see a screen titled 'Create your Auth0 Account', enter an email ID and click on Continue button.
  - Okta will send you 6 digits OTP, validate that
  - then setup the password
  - It will show you a screen with its desired tenant, refer to the screenshot below. I have modified the tenant to my choice 'ravikmalhotra'
  - My tenant looks like ravikmalhotra.us.auth0.com
  - <img width="1670" height="732" alt="image" src="https://github.com/user-attachments/assets/ba9fa417-a873-4f1a-b3e9-425a8b8e73e3" />


## Okta has 2 different platforms
- access https://www.okta.com, and then click on 'Free Trial'
- There you will 2 different platforms, termed as (1) Okta Platform, and (2) Auth0 Platform.
 
1. Workforce Identity Cloud (WIC).
  - This is the core Okta platform (sometimes called “Okta Classic/Identity Engine”).
  - Mostly paid + trial both.
  - it has 8000+ pre-built integrations. No more vendor lock-ins
  - Automated 1-click user onboarding and offboarding.
  - you can easily integrate with your existing business technologies such as - Microsoft, Google, Slack, Workday, AWS, Azure, etc....
  - It offers free trial for 30 days.
  - You need to have a work email for signing up.
   
2. Customer Identity Cloud (Auth0), this offers free tiers.
  - This is built on Auth0, which was acquired by Okta in 2021. 
  - if supports OAuth2.0, OIDC, JWT support for app logins.
  - Offers free tiers (forever) for students, learners, and developers. 

<img width="1656" height="652" alt="image" src="https://github.com/user-attachments/assets/69c68eaa-6074-45b4-a6ca-806346057dd0" />




# Defining Users in Okta
# Configuring External Directories
# Groups in Okta
# Configuring SSO & Provisioning
# Configuring Custom App Integration
# Managing Access Requests Works
# Configuring Universal Directories
# Okta Policy Frameworks

------------------------------------------------------

# Fundamentals

