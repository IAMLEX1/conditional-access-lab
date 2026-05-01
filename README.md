# Conditional Access Lab (Microsoft Entra ID)

## Overview
This project demonstrates how Conditional Access policies are used to secure user access in Microsoft Entra ID (Azure AD). The lab focuses on enforcing Multi-Factor Authentication (MFA), restricting access based on device compliance, and controlling access using trusted locations.

---

## Objectives
- Enforce MFA for Finance users
- Require compliant devices for access
- Restrict access to trusted network locations
- Understand Conditional Access policy structure

---

## Policy 1: MFA Enforcement (Finance)

**Description:**  
This policy enforces Multi-Factor Authentication (MFA) for users in the Finance group.

**Key Configurations:**
- Users: Finance group
- Cloud Apps: All resources
- Grant Control: Require MFA
- Policy Mode: Report-only

![MFA Policy Overview](./screenshots/...)01-mfa-policy-overview.png)  
![MFA Grant Control](./screenshots/...)02-mfa-grant-control.png)

---

## Policy 2: Require Compliant Device (Finance)

**Description:**  
This policy ensures that only compliant (managed and secure) devices can access company resources.

**Key Configurations:**
- Users: Finance group
- Grant Controls:
  - Require MFA
  - Require device to be marked as compliant
- Policy Mode: Report-only

![Device Policy Overview](./screenshots/...)03-device-policy-overview.png)  
![Device Grant Control](./screenshots/...)04-device-grant-control.png)

---

## Policy 3: Location-Based Access Control (Finance)

**Description:**  
This policy restricts access so users must be connecting from a trusted location.

**Key Configurations:**
- Users: Finance group
- Locations: Trusted IP ranges (Headquarters)
- Policy Mode: Report-only

![Location Policy Overview](./...)screenshots/05-location-policy-overview.png)  
![Named Location](./screenshots/...)06-named-location.png)

---

## Key Takeaways
- Conditional Access uses multiple signals (user, device, location)
- MFA is a core security control
- Device compliance protects company resources
- Location policies reduce unauthorized access
- Report-only mode prevents lockouts during testing

---

## Tools Used
- Microsoft Entra ID (Azure AD)
- Conditional Access Policies
