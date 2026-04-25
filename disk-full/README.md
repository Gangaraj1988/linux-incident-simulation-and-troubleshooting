# Linux Incident - Disk Full Causing Application Failure

## Scenario
Application stopped functioning even though the process was running.

## Problem
Logs were not being written and application behavior was inconsistent.

## L1 Investigation
- Checked process → running
- Checked logs → write errors observed
- Checked disk → 100% usage

## L2 Investigation
- Identified disk full condition
- Application unable to write logs due to no available space

## Commands Used
See commands.txt

## Root Cause
Disk full prevented application from writing logs, causing functional failure.

## Fix Applied
Removed unnecessary large files to free disk space.

## Verification
- Disk usage reduced
- Logs started writing again
- Application functioning normally

## Screenshots

![Process Running](screenshots/01_process_running.png)
![Logs Working](screenshots/02_logs_working.png)
![Disk Almost Full](screenshots/03_disk_almost_full.png)
![Disk Full](screenshots/04_disk_full.png)
![Error](screenshots/05_error.png)
![Disk Freed](screenshots/06_disk_freed.png)
![Recovery](screenshots/07_logs_recovered.png)
