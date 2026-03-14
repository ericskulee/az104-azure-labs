# Project 3 Notes

## Azure Site Recovery Observation
Attempted to enable replication from East US to West Europe.
Deployment failed at the automation account creation step.

## Why this happened
Azure free/trial subscriptions have limitations on:
- Cross-region replication resources
- Automation account creation in certain regions
- Site Recovery vault deployments

## What was demonstrated
- Successfully navigated the full DR configuration workflow
- Selected target region (West Europe)
- Configured replication and storage settings
- Understood the ASR architecture: source VM > cache storage > replica disk

## In production
Azure Site Recovery would:
- Continuously replicate the VM to the target region
- Allow test failovers without impacting production
- Enable RTO (Recovery Time Objective) of minutes instead of hours
