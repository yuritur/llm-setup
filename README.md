# llm-setup

This repository contains a personal setup for AI coding assistants (Claude/Cursor style workflows).

It focuses on consistent execution patterns:
- lightweight global rules (`.claude/rules`)
- reusable agent skills (`.claude/skills`)
- a dedicated code reviewer agent (`.claude/agents`)

The setup is designed for a plan-first, review-driven workflow: clarify intent, create an implementation plan, execute tasks, and review quality before merging.

## How to use

1. Copy the `.claude` directory into your project.
2. Adjust rules and skill prompts for your stack and team conventions.
3. Use the workflow skills to keep implementation predictable and repeatable.

## Skill selection guideline

Add stack-specific skills when they provide clear value.
Example: for a Python project, include a `python-senior` style skill; for a Go project, include a Go-focused skill.

Avoid loading too many skills at once because they consume context and can make responses less focused.
Only keep skills relevant to the current codebase and task (e.g., do not use Python skills in a Go-only project).
