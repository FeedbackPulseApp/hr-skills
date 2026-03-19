# FeedbackPulse HR Skills

A vetted skills registry for AI coding agents (claws) curated by [FeedbackPulse EX Platform](https://feedbackpulse.com)

## Submitting Skills

Open a PR with your proposed skill.

### Security Checks

Every submission is reviewed by multiple frontier AI models before human approval:

| Agent           | Focus                                      |
| --------------- | ------------------------------------------ |
| Claude Opus 4.6 | Prompt injection, instruction manipulation |
| GPT-5.2         | Code execution, system access risks        |

Skills are checked for:

- Prompt injection (hidden instructions, "ignore previous", encoded commands)
- Dangerous tool usage (unrestricted Bash, rm -rf, sensitive file access)
- Data exfiltration (network calls to external URLs, reading credentials)
- Social engineering or manipulation attempts
- Overly permissive allowed-tools

A skill must pass both AI reviews, then receive human approval to be merged.

> **Note:** This repository contains Anthropic's implementation of skills for Claude. For information about the Agent Skills standard, see [agentskills.io](http://agentskills.io).
