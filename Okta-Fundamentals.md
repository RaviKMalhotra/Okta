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
 
# Understanding Okta Accounts
- Okta has 2 different platforms
- access https://www.okta.com, and then click on 'Free Trial'
- There you will 2 different platforms, termed as (1) Okta Platform, and (2) Auth0 Platform.
 
1. Workforce Identity Cloud (WIC).
  - This is also known as octa core.
  - Mostly paid + trial both.
  - it has 8000+ pre-built integrations. No more vendor lock-ins
  - Automated 1-click user onboarding and offboarding.
  - you can easily integrate with your existing business technologies such as - Microsoft, Google, Slack, Workday, AWS, Azure, etc....
  - It offers free trial for 30 days.
  - You need to have a work email for signing up.
   
2. Customer Identity Cloud (Auth0), this offers free tiers.

# Free Accounts



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

