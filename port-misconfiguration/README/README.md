# Linux Incident - Service Running but Not Accessible

## Scenario
Application was running but users reported it was not accessible.

## Problem
Users were unable to connect to the application.

## L1 Investigation
- Checked process → running
- Checked port → expected port not listening
- Tested connectivity → failed on expected port

## L2 Investigation
- Verified actual listening ports
- Found application running on a different port (9999)

## Commands Used
See commands.txt

## Root Cause
Application configured on incorrect port (9999 instead of 5000)

## Fix Applied
Updated correct port or accessed correct endpoint

## Verification
- curl to correct port successful

## Screenshots

![Process Running](screenshots/01_process_running.png)
![Port Check](screenshots/02_port_check.png)
![Connection Failed](screenshots/03_connection_failed.png)
![Connection Success](screenshots/04_connection_success.png)
