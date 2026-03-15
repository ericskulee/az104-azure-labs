# Project 4 Notes

## Conditional Access Limitation
Conditional Access policy creation is greyed out due to 
Entra ID Free tier licensing.

## What Conditional Access requires
- Entra ID P1 license (minimum)
- Entra ID P2 for risk-based policies

## What we would have configured
- Policy name: ca-mfa-project4
- Users: Admin, Developer, Reader (project4 users)
- Target app: app-project4
- Control: Require MFA
- This would force MFA for all users accessing app-project4

## In production Conditional Access can
- Require MFA based on location, device, or risk level
- Block access from specific countries
- Require compliant devices (Intune managed)
- Block legacy authentication protocols
- This is heavily tested in SC-300 and AZ-500

## MFA Limitation
Per-user MFA configuration also requires Entra ID P1
for full Conditional Access integration. Basic MFA 
can be enabled via Security Defaults instead.
