# lesson-2.2–the-first-iteration

## Objective

Build the first working version of a Python Sysmon parser.

## Completed

- Created `parser.py`.
- Installed Python 3.12 using `winget`.
- Tested the parser against sample Sysmon XML files.
- Verified that the parser extracted the target fields from Sysmon Event ID 1.
- Confirmed that all three sample files parsed correctly.

## What the Parser Does

The parser takes a Sysmon XML file path as a command-line argument, extracts key Event ID 1 process creation fields, and outputs the results as JSON.

## Fields Extracted

- EventID
- UtcTime
- Image
- CommandLine
- User
- IntegrityLevel
- ParentImage
- ParentCommandLine
- Computer
- Hashes

## Commands Used

```powershell
python parser.py samples/event1.xml
python parser.py samples/event2.xml
python parser.py samples/event3.xml

##What I learned

I learned how to use Claude Code to create and test a Python security tool. I also learned that my system did not have a working Python interpreter installed, 
so Python 3.12 had to be installed before the parser could be tested.

##Cybersecurity Connection

Sysmon Event ID 1 records process creation activity. Parsing these logs into JSON can help analysts investigate suspicious comman lines, 
parent-child process relationships, encoded PowerShell commands, and user activity during threat hunting or incident response.

##Reflection 

This lesson showed me how AI can help build a first version of a security tool, but it also reminded me that the environment must be configured
correctly before code can be tested. Installing Python was an important setup step for continuing the course.
