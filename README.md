# Technical Writing Skill

Skill for writing, reviewing, and structuring technical tutorials and articles following technical writing standards.

## Install 

     npx skills add https://github.com/fordnox/technical-writing --skill technical-writing

## What It Does

- **Write** new tutorials from scratch using proven article templates
- **Review** existing articles against a quality checklist
- **Structure** outlines for procedural, conceptual, or short-form articles

## Usage

Install as a Claude Code skill, then ask things like:

- "Write a tutorial on deploying a Node.js app with PM2 on Ubuntu 24.04"
- "Review this article for style and structure issues"
- "Create an outline for a conceptual article about container networking"

The skill automatically applies technical guidelines: outcome-focused language, explained commands, linked prerequisites, and proper heading hierarchy.

## File Structure

```
SKILL.md                         # Main skill definition
references/
  structure-templates.md         # Copy-paste article skeletons
  style-examples.md              # Good vs. bad style comparisons
```

## Key Guidelines Enforced

- Every command explained before execution
- No condescending language (simple, easy, just, obviously)
- Second person ("you") throughout
- Outcome-focused introductions
- Prerequisites with links to supporting tutorials
- Conclusions with next steps
