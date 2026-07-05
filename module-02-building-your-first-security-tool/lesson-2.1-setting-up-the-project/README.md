# Lesson 2.1 – Setting Up the Project

## Objective

Create the project workspace for the Sysmon parser and initialize it with Claude Code.

## What I Learned

- How to create a project folder
- How to start Claude Code inside the correct workspace
- Why `CLAUDE.md` helps Claude understand the project
- Why keeping work in a dedicated folder is safer and more organized

## Commands Used

```powershell
cd $HOME
mkdir sysmon-parser
cd sysmon-parser
claude

# Lesson 2.1 – Setting Up the Project

## Objective

Set up a new Claude Code project for building a Sysmon parser.

## Completed

- Created a new project directory
- Started Claude Code inside the project
- Initialized the project using `/init`
- Created a `CLAUDE.md` file
- Updated `CLAUDE.md` with project-specific context

## Skills Practiced

- Project initialization
- Claude Code
- Project documentation
- Workspace management

## Next Step

Create sample Sysmon XML data for testing.

---

# concepts.md

```markdown
# Concepts

## Workspace

Claude Code works within the current project directory.

## CLAUDE.md

CLAUDE.md stores persistent project instructions so Claude understands the project's purpose every time it starts.

## Project Context

Providing Claude with the project goals, technology stack, and expected output improves the quality and consistency of its assistance.
# Reflection

## What I learned

Claude Code uses the current directory as its workspace and relies on CLAUDE.md to understand the project's context.

## What surprised me

The latest version of Claude Code asks interactive questions during initialization instead of generating a generic CLAUDE.md file.

## Why this matters

Clearly defining a project's purpose helps Claude generate more relevant code and recommendations.

