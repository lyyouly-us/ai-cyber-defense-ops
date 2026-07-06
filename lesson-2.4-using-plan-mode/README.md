# Lesson 2.4 – Using Plan Mode for Bigger Changes

## Objective

Use Claude Code's Plan Mode to design and implement filtering capabilities for a Sysmon XML parser before writing code.

## Completed

- Entered Plan Mode to design a new parser feature.
- Evaluated implementation tradeoffs before modifying code.
- Added command-line filtering by:
  - Image
  - User
  - IntegrityLevel
- Implemented case-insensitive matching for Image and User filters.
- Used AND logic when combining multiple filters.
- Preserved the original output format for unfiltered runs.
- Returned JSON arrays when filters were applied.
- Verified the implementation through six test cases.

## Commands Used

```powershell
python parser.py samples\event1.xml --image whoami

python parser.py samples\multi_events.xml --user "corp\jsmith"

python parser.py samples\multi_events.xml --integrity-level Medium

python parser.py samples\multi_events.xml --image powershell --user "corp\jsmith"
```

## Verification Results

All verification tests passed successfully.

Verified:

- Image filtering
- User filtering
- Integrity level filtering
- Case-insensitive matching
- AND filter logic
- Empty result handling
- Backward compatibility with unfiltered execution

## What I Learned

Planning before implementation leads to cleaner software. By defining design decisions first, it was easier to add filtering functionality while preserving the parser's original behavior.

Reviewing Claude Code's implementation before approving changes also helped me understand how each modification supported the planned architecture.

## Cybersecurity Connection

Security analysts rarely investigate every event in a log file. Filtering allows investigations to focus on:

- Specific processes
- Individual users
- Privilege levels
- Suspicious activity

These capabilities make log analysis significantly faster during threat hunting and incident response.

## Professional Takeaway

This lesson introduced a development workflow used by professional software teams:

1. Plan the feature.
2. Evaluate tradeoffs.
3. Implement incrementally.
4. Review changes.
5. Verify with automated tests.

Following this workflow helps reduce bugs and improves maintainability.
