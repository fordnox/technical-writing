---
name: technical-writing
description: Apply technical writing guidelines to create, review, edit, or structure technical tutorials and articles. Use this skill whenever the user wants to write a technical tutorial, technical article, or developer documentation, "technical writing", "tutorial structure", "how-to guide", "developer docs", or asks to review or improve the quality of a technical article. Also trigger when a user is drafting any step-by-step technical guide or when they want feedback on whether their article follows best practices for developer education content.
---

# Technical Writing Skill

Apply technical writing standards when drafting, structuring, reviewing, or improving technical tutorials and articles.

## Workflow

When a user asks you to work on a technical article, determine which mode applies:

**Writing a new article:**
1. Confirm the article type (procedural tutorial, conceptual article, or short/focused article)
2. Read `references/structure-templates.md` for the matching template
3. Draft using the template structure, following all guidelines below
4. Run through the Quality Checklist before presenting the draft

**Reviewing or editing an existing article:**
1. Read the article
2. Check it against the Quality Checklist at the bottom of this file
3. Read `references/style-examples.md` for good/bad pattern comparisons
4. Provide specific feedback with corrected examples, or apply edits directly if asked

**Structuring or outlining:**
1. Confirm the article type and topic
2. Propose a heading structure following the templates in `references/structure-templates.md`
3. Write a brief description of what each section should cover

---

## Core Principles

Every article must be:

1. **Comprehensive and written for all experience levels** -- Never assume background knowledge. Include every command from first SSH connection to working setup. The goal is for readers to learn concepts, not just copy-paste.
2. **Technically detailed and correct** -- Every command needs explanation including options and flags. Every code block needs prose explaining what it does and why.
3. **Practical, useful, and self-contained** -- The reader finishes with something working, installed, or built. Cover the topic thoroughly from start to finish.
4. **Friendly but formal** -- No jargon, memes, excessive slang, or jokes. Write for a global audience. No first-person singular ("I think...") -- use second person ("You will configure...") or first-person plural ("We will examine...").

### Language Rules

**Words to avoid** -- never use these because they frustrate readers who encounter difficulty:
`simple`, `straightforward`, `easy`, `simply`, `obviously`, `just`

**Outcome-focused language** -- describe what the reader will *do*, not what they will *learn*:
- Bad: "You will learn how to install Apache"
- Good: "In this tutorial, you will install Apache"

---

## Article Structure

Three article types exist. Choose based on the content.

### Procedural Tutorial (most common)
```
# Title (H1)
### Introduction (H3 -- this is intentionally H3, not H2)
## Prerequisites (H2)
## Step 1 -- Doing the First Thing (H2)
## Step 2 -- Doing the Next Thing (H2)
## Step N -- Doing the Last Thing (H2)
## Conclusion (H2)
```

### Conceptual Article
```
# Title (H1)
### Introduction (H3)
## Prerequisites (optional, H2)
## Subtopic 1 (H2)
## Subtopic 2 (H2)
## Conclusion (H2)
```

### Short/Focused Article
```
# Title (H1)
Introduction paragraph (no heading)
## Prerequisites (optional, H2)
Article body
Conclusion paragraph (no heading)
```

---

## Section-by-Section Guide

### Title
- Format: **How To [Accomplish a Task] with [Software] on [Distro]**
- Include the goal, not just the tool: "How To Host a Website with Caddy on Ubuntu" not "How To Use Caddy on Ubuntu"
- Keep under 60 characters when possible

### Introduction (1-3 paragraphs)
Answer these four questions:
1. What is the tutorial about? (software involved and what it does)
2. Why should the reader learn this? (benefits, practical reasons)
3. What will the reader do or create? (be specific)
4. What will they have accomplished when done? (new skills, new capabilities)

### Prerequisites
- Format as a bulleted checklist the reader can work through
- Each item must link to an existing tutorial or official docs
- Start from a fresh server (for sysadmin/DevOps) or clean dev environment (for software dev)
- Be specific: not "Familiarity with JavaScript" but "Familiarity with JavaScript -- see [How To Code in JavaScript series](link)"

**Common sysadmin prerequisites:** server count, distro, initial server setup, memory requirements, software installation, DNS settings, SSL certificates

**Common software dev prerequisites:** local tools (Git, Node.js, Python, Docker), third-party accounts, dev environment setup tutorials, conceptual background articles

### Steps
- Each step heading: `## Step N -- Verb Phrase Describing the Action`
- Before asking the reader to run a command, explain what it does and why
- Explain all command options and flags
- Follow every code block with prose explanation
- Include expected output when it helps readers verify success
- Explain any deviation from defaults

### Conclusion
- Summarize what the reader accomplished
- Describe the working state of their setup
- Suggest next steps, related tutorials, or further reading
- Keep it to 1-3 paragraphs

---

## Formatting Reference

### Code
- Inline code: use backticks for commands, filenames, variables, package names
- Code blocks: triple backticks with language specified (e.g., ```bash)
- File paths: inline code -- `/etc/nginx/nginx.conf`
- Variables the reader must customize: use ALL_CAPS -- e.g., `your_domain` or `YOUR_DOMAIN`

### Callouts (custom Markdown)
```
<$>[note]
**Note:** Use for supplemental info.
<$>

<$>[warning]
**Warning:** Use for potentially destructive actions.
<$>

<$>[info]
**Info:** Use for general context.
<$>
```

### Commands
- Show full commands; don't abbreviate
- Prefix interactive shell commands with `$` (not root)
- Prefix root commands with `#`
- Include expected output as a separate non-copyable block (label with `[Output]`)

### Headings
- H1: Title only (one per article)
- H2: Major sections (Steps, Prerequisites, Conclusion)
- H3: Introduction and sub-sections within steps
- H4: Use sparingly for nested sub-sections

---

## Terminology Quick Reference

| Prefer | Avoid |
|--------|-------|
| Because | Since (when meaning "because") |
| Once you've... | When you've... (ambiguous timing) |
| Log in to | Login to |
| Set up (verb) | Setup (verb) |
| Setup (noun) | Set up (noun) |
| Web server | Webserver |
| Username | User name |

### Technical Terms
- **Ubuntu**: Always capitalize; include version (e.g., Ubuntu 22.04)
- **sudo**: Lowercase, code-formatted when used as command
- **SSH**, **URL**, **DNS**, **API**: Uppercase acronyms

---

## Quality Checklist

Before finalizing any article, verify every item:

- [ ] Title includes the goal (not just the tool)
- [ ] Introduction answers all 4 questions
- [ ] Every prerequisite links to an existing tutorial or official docs
- [ ] Every command is explained before execution
- [ ] Every code block has prose explanation after it
- [ ] No use of: simple, easy, just, simply, obviously, straightforward
- [ ] Second person ("you") used consistently, not "I"
- [ ] Outcome-focused language ("you will install" not "you will learn to install")
- [ ] Conclusion summarizes accomplishment and suggests next steps
- [ ] Tested on fresh server/environment following tutorial exactly

---

## Reference Files

For more detail, read these files as needed:

- `references/structure-templates.md` -- Copy-paste Markdown templates for each article type. Read this when starting a new article to get the right skeleton.
- `references/style-examples.md` -- Good vs. bad examples for common style patterns. Read this when reviewing an article or when unsure about a specific pattern.
