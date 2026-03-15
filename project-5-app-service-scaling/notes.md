# Project 5 Notes

## Deployment Slots Limitation
Deployment slots require Standard (S1) or higher App Service Plan.
Free F1 tier does not support deployment slots.

## What deployment slots do in production
- Run two versions of the app simultaneously (production + staging)
- Test new features in staging without affecting production
- Swap slots instantly with zero downtime when ready
- This is called blue/green deployment
- Slot swap also swaps all settings unless marked as "slot sticky"
- This is a common AZ-104 exam topic

## Autoscaling Limitation
Autoscaling also requires Standard tier or higher.
Free F1 tier uses shared infrastructure with no scaling options.

## What autoscaling does in production
- Automatically adds instances when CPU > threshold
- Automatically removes instances when load decreases
- Saves cost by scaling down during off-peak hours
- Rules can be based on CPU, memory, HTTP queue length

## What was successfully demonstrated
- Created App Service Plan (asp-project5) on Free F1 tier
- Deployed a live Python Flask web application
- App is publicly accessible at Azure URL
- Demonstrates core App Service deployment workflow

## Backup Limitation
App Service backup requires Basic (B1) tier or higher.
Free F1 tier does not support backup and restore.

## What App Service backup does in production
- Backs up app configuration and file content
- Can include linked databases
- Scheduled or manual backups
- Restore to same or different App Service
- Retention period configurable

## Summary of Free F1 Limitations encountered
| Feature | Required Tier | Status |
|---------|--------------|--------|
| Deployment Slots | Standard S1+ | Blocked |
| Autoscaling | Standard S1+ | Blocked |
| Backup & Restore | Basic B1+ | Blocked |
| Custom Domains | Basic B1+ | Blocked |
| Monitoring & Alerts | All tiers | ✅ Works |
| Code Deployment | All tiers | ✅ Works |

## Key exam takeaway
Free F1 is for development/testing only.
Production workloads require Standard S1 or higher
for full feature set including slots, scaling and backup.
