# QualityMax

**AI-Powered Test Case Generation Platform**

Transform your web application into comprehensive test coverage with intelligent crawling and automated test generation.

[![Website](https://img.shields.io/badge/Website-app.qamax.co-blue)](https://app.qamax.co)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-QualityMax-0077B5)](https://www.linkedin.com/company/qualitymax/)
[![CLI](https://img.shields.io/npm/v/qamax-auth-cli)](https://www.npmjs.com/package/qamax-auth-cli)

## What is QualityMax?

QualityMax is an AI-powered platform that automatically generates test cases by crawling your web application. It understands your UI, identifies user flows, and creates comprehensive test coverage - all without writing a single line of test code.

### Key Features

- **AI-Powered Crawling** - Intelligent web crawler that understands your application structure
- **Automatic Test Generation** - Generate test cases from discovered pages and user flows
- **Cloud Browser Execution** - Run generated tests directly in QualityMax Cloud Browser
- **TestRail Integration** - Seamlessly sync generated tests to your TestRail projects
- **Authenticated Crawling** - Capture and reuse authentication sessions for protected pages
- **Team Collaboration** - Share projects and test suites across your team
- **User Data Variables** - Manage test data with encrypted secrets support

## Getting Started

### 1. Sign Up

Visit [app.qamax.co](https://app.qamax.co) to create your account.

### 2. Create a Project

Set up your first project with your application's URL.

### 3. Run AI Crawl

Let QualityMax discover your application's pages and generate test cases.

### 4. Run & Export

Run generated tests in QualityMax Cloud Browser or export to your test management tools.

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

## Documentation

- [Getting Started Guide](docs/getting-started.md)
- [AI Crawl Configuration](docs/ai-crawl.md)
- [User Data Variables](docs/user-data-variables.md)
- [API Reference](docs/api-reference.md)

## Use Cases

### QA Teams
Accelerate test case creation and maintain comprehensive coverage as your application evolves.

### Developers
Generate regression tests automatically when building new features.

### Startups
Get professional test coverage without dedicated QA resources.

### Enterprises
Scale testing across multiple projects with team collaboration features.

## Security

We take security seriously:

- All data encrypted at rest and in transit
- SOC 2 Type II compliance (in progress)
- GDPR compliant
- Regular security audits
- See [SECURITY.md](SECURITY.md) for our security policy

## Contact

- **Email**: contact@qamax.co
- **LinkedIn**: [QualityMax](https://www.linkedin.com/company/qualitymax/)
- **Website**: [app.qamax.co](https://app.qamax.co)
- **Issues**: [GitHub Issues](https://github.com/Quality-Max/qualitymax/issues)

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

Copyright (c) 2025-2026 QualityMax. All rights reserved.
