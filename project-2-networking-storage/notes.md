# Project 2 Notes

## SAS Token Observation
When attempting to generate a SAS token, the portal showed a warning:
"Authorization with Shared Key is disabled for this account."

## Why this happened
We configured the storage account with:
- Public access disabled
- Private endpoint only (snet-database subnet)
- Shared Key authorization disabled

This is the CORRECT secure configuration for production. SAS tokens 
use Shared Key authorization under the hood, so disabling Shared Key 
also disables SAS token generation.

## Security Lesson
For secure storage in production:
- Use private endpoints instead of public access
- Use Azure AD authentication instead of Shared Key/SAS
- SAS tokens are convenient but less secure than Azure AD RBAC
- This is exactly what AZ-500 tests on storage security
