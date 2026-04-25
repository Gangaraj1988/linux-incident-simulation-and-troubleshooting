# Linux Production Incident - Permission Issue

## Scenario
Application was running but users reported it was not working.

## Problem
Application logs were not accessible and system behavior was abnormal.

## L1 Investigation
- Checked process → running
- Checked logs → permission denied
- Checked directory → no permissions

## L2 Investigation
- Identified permission issue blocking access
- Application unable to interact with filesystem

## Commands Used
See commands.txt

## Root Cause
Directory permission changed to 000, removing all access.

## Fix Applied
chmod 755 /opt/payment-app

## Verification
- Logs accessible
- Application functioning normally

## Screenshots
![Process Check](screenshots/01_process_check.png)
![Permission Denied](screenshots/02_permission_denied.png)
![Root Cause](screenshots/03_ls_output.png)
![Fix](screenshots/04_fix_applied.png)
![Verification](screenshots/05_verification.png)
