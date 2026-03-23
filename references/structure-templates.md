# Article Structure Templates

Copy-paste these Markdown templates as starting points.

---

## Procedural Tutorial Template

```markdown
# How To <Accomplish a Task> with <Software> on <Distro>

### Introduction

<Paragraph 1: What is this tutorial about? Briefly describe the software and what it does.>

<Paragraph 2: Why should the reader care? Practical benefits of this setup.>

<Paragraph 3: What will the reader accomplish? What will they have when done?>

## Prerequisites

Before you begin this guide, you will need:

- One <Distro> server set up by following [the <Distro> initial server setup guide](link), including a non-root `sudo`-enabled user and a firewall.
- <Additional software> installed on your server, which you can set up by following [How To Install <Software> on <Distro>](link).
- <Any other requirement>.

## Step 1 — <Verb Phrase Describing First Action>

<Explanation of what this step accomplishes and why it's necessary.>

<Explain the command before showing it.>

```bash
sudo example-command --flag value
```

<Explain the output or result. What should the reader see?>

```
[Output]
Expected output here
```

<Continue with sub-steps as needed using H3 headings.>

## Step 2 — <Verb Phrase Describing Second Action>

...

## Step N — <Verb Phrase Describing Last Action>

...

## Conclusion

In this tutorial, you <summary of what was accomplished>. You now have a <description of working setup>.

As a next step, you might want to:
- [Related Tutorial 1](link)
- [Related Tutorial 2](link)

For more information about <software>, see the [official documentation](link).
```

---

## Conceptual Article Template

```markdown
# Understanding <Topic>

### Introduction

<What is this article about? Why is this topic important? What will the reader learn?>

## What Is <Concept>?

<Explanation of the core concept.>

## How <Concept> Works

<Deeper explanation, with examples.>

## <Related Subtopic>

<Additional context or related information.>

## Conclusion

<Summary of what was covered. Suggested next steps or related tutorials.>
```

---

## Short/Focused Article Template

```markdown
# How To <Do One Specific Thing>

In this tutorial, you will <brief description of the one task>. <One sentence on why this is useful.>

## Prerequisites

- <Prerequisite with link>

To complete this tutorial, run the following command:

```bash
example-command
```

This command <explanation of what it does>.

You have now <brief summary of what was accomplished>. To learn more, see [Related Tutorial](link).
```
