# Apache Port Misconfiguration Issue

## Scenario
Website was not accessible using the default URL.

## Problem
Apache service was running, but the website was not loading on port 80.

## L1 Investigation
- Checked service status
- Tested connectivity using curl
- Verified port binding

## L2 Investigation
- Found Apache listening on port 8080 instead of 80

## Root Cause
Incorrect port configuration in Apache settings

## Fix Applied
Updated ports.conf to use port 80 and restarted Apache

## Verification
- Website accessible on port 80
- Service running normally
