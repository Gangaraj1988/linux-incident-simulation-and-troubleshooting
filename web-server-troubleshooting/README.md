# Apache Service Down Incident

## Scenario
Website was not accessible on localhost.

## Problem
Application (Apache web server) was down and not responding.

## L1 Investigation
- Checked service status using systemctl
- Verified port 80 using ss command
- Checked logs for errors
- Tested connectivity using curl

## L2 Investigation
- Identified that Apache service was stopped
- No port was listening on port 80

## Commands Used
See commands.txt

## Root Cause
Apache service was manually stopped, causing website to become inaccessible.

## Fix Applied
Restarted Apache service using systemctl start apache2

## Verification
- Verified service status is active
- Confirmed port 80 is listening
- Verified website accessibility using curl
