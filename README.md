<p align="center">
  <img src="assets/logo.png" alt="QualityMax" width="300">
</p>

<h1 align="center">QualityMax</h1>

<p align="center">
  <strong>AI-Powered Test Case Generation Platform</strong>
</p>

<p align="center">
  Enforce your web application with comprehensive test coverage via intelligent crawling and automated test generation.
</p>

<p align="center">
  <a href="https://app.qamax.co"><img src="https://img.shields.io/badge/Website-app.qamax.co-7c3aed" alt="Website"></a>
  <a href="https://www.linkedin.com/company/qualitymax/"><img src="https://img.shields.io/badge/LinkedIn-QualityMax-0077B5" alt="LinkedIn"></a>
  <a href="https://www.npmjs.com/package/qamax-auth-cli"><img src="https://img.shields.io/npm/v/qamax-auth-cli?color=7c3aed" alt="CLI"></a>
</p>

---

## What is QualityMax?

QualityMax is an AI-powered platform that automatically generates test cases by crawling your web application. It understands your UI, identifies user flows, and creates comprehensive test coverage - all without writing a single line of test code.

## Key Features

| Feature | Description |
|---------|-------------|
| **AI-Powered Crawling** | Intelligent web crawler that understands your application structure |
| **Automatic Test Generation** | Generate test cases from discovered pages and user flows |
| **Cloud Browser Execution** | Run generated tests directly in QualityMax Cloud Browser |
| **TestRail Integration** | Seamlessly sync generated tests to your TestRail projects |
| **Authenticated Crawling** | Capture and reuse authentication sessions for protected pages |
| **Team Collaboration** | Share projects and test suites across your team |
| **User Data Variables** | Manage test data with encrypted secrets support |

## Getting Started

Visit [app.qamax.co](https://app.qamax.co) and sign up for the waitlist. Authorise your email and wait for an invite with further instructions how to login. We will send it very soon.

Once you have access:

```
1. Create Project →  Set up your first project with your application's URL
2. Run AI Crawl   →  Let QualityMax discover pages and generate test cases
3. Run & Export   →  Execute tests in Cloud Browser or export to your tools
```

## CLI Tool

For authenticated crawling, use our CLI to capture browser sessions:

```bash
# Install
npm install -g qamax-auth-cli

# Login to QualityMax
qamax-auth login

# Capture authentication
qamax-auth capture https://your-app.com -p PROJECT_ID -n "my-auth"
```

See [qamax-auth-cli](https://github.com/Quality-Max/qamax-auth-cli) for more details.

## Use Cases

**QA Teams** - Accelerate test case creation and maintain comprehensive coverage as your application evolves.

**Developers** - Generate regression tests automatically when building new features.

**Startups** - Get professional test coverage without dedicated QA resources.

**Enterprises** - Scale testing across multiple projects with team collaboration features.

## Security

We take security seriously:

- All data encrypted at rest and in transit
- SOC 2 Type II compliance (in progress)
- GDPR compliant
- Regular security audits

See [SECURITY.md](SECURITY.md) for our security policy.

## Documentation

- [Getting Started Guide](docs/getting-started.md)
- [AI Crawl Configuration](docs/ai-crawl.md)
- [User Data Variables](docs/user-data-variables.md)
- [API Reference](docs/api-reference.md)

## Contact

<p>
  <a href="mailto:contact@qamax.co">contact@qamax.co</a> ·
  <a href="https://www.linkedin.com/company/qualitymax/">LinkedIn</a> ·
  <a href="https://app.qamax.co">Website</a> ·
  <a href="https://github.com/Quality-Max/qualitymax/issues">Issues</a>
</p>

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

<p align="center">
  Copyright (c) 2025-2026 QualityMax. All rights reserved.
</p>
