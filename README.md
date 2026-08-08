# YouTube Agent Automation

AI agent workflows for automating YouTube content production, built on
Anthropic Claude models running via Amazon Bedrock.

## About

This project explores how a set of specialized AI agents can handle the
repetitive parts of running a YouTube channel — research, drafting,
and metadata — so that creative decisions stay with the human.

## Architecture

The system is organized as an orchestrator coordinating four sub-agents:

| Agent | Responsibility |
|---|---|
| Research | Topic discovery, source gathering, summarization |
| Script | Draft generation, revision passes, tone adjustment |
| Metadata | Title, description, and tag optimization |
| Review | Fact-checking and consistency validation |

The orchestrator manages task state, routes work between agents, and
handles retries and error recovery.

## Tech Stack

- **Models:** Anthropic Claude via Amazon Bedrock Runtime API
  (`InvokeModel` / `Converse`)
- **Development environment:** Claude Code
- **Language:** Python
- **AWS SDK:** boto3
- **Auth:** IAM user with least-privilege scoped permissions
- **Region:** us-east-1

## Roadmap

- [ ] Core orchestrator loop
- [ ] Research agent with web source summarization
- [ ] Script agent with multi-pass revision
- [ ] Metadata optimization agent
- [ ] Persistent task state and logging
- [ ] Cost tracking per pipeline run

## Status

Early development. Built as a personal learning project in AI agent
design, prompt engineering, and cloud infrastructure.

## Author

Mehmet Taha Kızıltan — [@mtk-axis](https://github.com/mtk-axis)
