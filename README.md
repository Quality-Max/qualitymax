<p align="center">
  <img src="assets/logo.png" alt="QualityMax" width="300">
</p>

<h1 align="center">QualityMax</h1>

<p align="center">
  <strong>AI-Native Test Automation Platform</strong>
</p>

<p align="center">
  Generate, execute, and self-heal tests for Go, Rust, Python, and Playwright — across your entire CI/CD pipeline.
</p>

<p align="center">
  <a href="https://qualitymax.io"><img src="https://img.shields.io/badge/Website-qualitymax.io-7c3aed" alt="Website"></a>
  <a href="https://app.qualitymax.io"><img src="https://img.shields.io/badge/App-app.qualitymax.io-10b981" alt="App"></a>
  <a href="https://www.linkedin.com/company/qualitymax/"><img src="https://img.shields.io/badge/LinkedIn-QualityMax-0077B5" alt="LinkedIn"></a>
</p>

---

## What is QualityMax?

QualityMax is the AI QA engineer for your team. Install the GitHub App, and on every pull request:

- **AI reviews your code** — Claude Haiku analyzes the diff, flags security issues, posts inline annotations
- **Runs your tests** — clones your repo, executes `go test` / `cargo test` / `pytest` on our cloud, reports pass/fail
- **Runs AI-generated tests** — tests that QualityMax created from analyzing your codebase run alongside yours
- **Reports results as a GitHub check** — directly on the PR

Zero config. No YAML. No GitHub Actions minutes consumed.

## How It Works

```
Install GitHub App -> Link repo -> Every PR gets:

  Gate Alpha -- AI code review + SAST security scan
  Gate Gamma -- Run your repo's own test suite
  Gate Delta -- Run AI-generated tests
  Results posted as GitHub check + PR comment
```

## Key Features

| Feature | Description |
|---------|-------------|
| **Multi-Language Testing** | Go (`go test`), Rust (`cargo test`), Python (`pytest`), Playwright (browser E2E) |
| **AI Test Generation** | Analyze your repo, identify test gaps, generate test cases and scripts |
| **CI/CD Pipeline** | AI review + repo tests + AI tests on every PR |
| **Cloud Execution** | Run tests on QualityMax infrastructure |
| **Self-Healing Tests** | Broken Playwright tests auto-fix when selectors change |
| **10 App Types** | CLI tools, TUI agents, libraries, mobile apps, browser extensions |
| **MCP Integration** | Works with Claude Code and qmax-code as an AI agent tool |
| **GitHub and GitLab** | Full support for both platforms |

## Quick Start

### Option 1: GitHub App (recommended)

1. Install the [QualityMax GitHub App](https://github.com/apps/qualitymaxapp) on your repo
2. Import the repo at [app.qualitymax.io](https://app.qualitymax.io)
3. Deep scan runs automatically, test areas identified, review and approve
4. Tests generated and run on every future PR

### Option 2: CLI Agent

```bash
# Install qmax-code (Go TUI agent)
brew install qualitymax/tap/qmax-code

# Or use with Claude Code via MCP
claude --mcp qualitymax
```

## Pipeline Architecture

```
PR Opened
  Gate Alpha: AI Code Review + SAST (~17s)
  Gate Gamma: Clone and Run Repo Tests (~30-60s)
  Gate Delta: Run AI-Generated Tests (~30s)
  Gate Beta: E2E Tests Against Preview Deploy (web apps only)
```

## Supported Languages

| Language | Test Command | Cloud Execution | CI/CD Pipeline |
|----------|-------------|-----------------|----------------|
| **Go** | `go test -json ./...` | Yes | Yes |
| **Rust** | `cargo test` | Yes | Yes |
| **Python** | `pytest` | Yes | Yes |
| **Playwright** | `npx playwright test` | Yes | Yes |

## Security

- Tests run in isolated environments with secrets-free env whitelist
- Resource limits (4GB memory, 1024 processes) prevent abuse
- GitHub App tokens scrubbed from all logs and error messages
- Input validation on all webhook payloads

## Contact

<p>
  <a href="mailto:contact@qualitymax.io">contact@qualitymax.io</a> ·
  <a href="https://www.linkedin.com/company/qualitymax/">LinkedIn</a> ·
  <a href="https://discord.gg/kbEC28D4">Discord</a> ·
  <a href="https://qualitymax.io">Website</a> ·
  <a href="https://github.com/Quality-Max/qamax-rag-app/issues">Issues</a>
</p>

---

<p align="center">
  Built in Berlin | Copyright 2025-2026 QualityMax. All rights reserved.
</p>
