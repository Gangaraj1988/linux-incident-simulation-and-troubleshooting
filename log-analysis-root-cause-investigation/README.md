# Apache Log Analysis & Root Cause Investigation

## Scenario
Apache service failed after introducing an invalid configuration entry.

## Problem
Web service became unavailable because Apache configuration validation failed.

## Investigation Performed
- Checked service status using systemctl
- Investigated logs using journalctl
- Performed configuration validation using apache2ctl configtest

## Root Cause
Invalid directive added inside apache2.conf

## Fix Applied
Removed the invalid configuration and validated syntax successfully.

## Verification
- Apache configuration returned Syntax OK
- Service restarted successfully
- Website accessibility restored using curl

## Skills Demonstrated
- Apache troubleshooting
- Log analysis
- Root cause investigation
- Linux administration
- Service recovery
