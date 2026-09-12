```text
 ██████╗ ██╗   ██╗ █████╗ ██╗     ██╗████████╗██╗   ██╗███╗   ███╗ █████╗ ██╗  ██╗
██╔═══██╗██║   ██║██╔══██╗██║     ██║╚══██╔══╝╚██╗ ██╔╝████╗ ████║██╔══██╗╚██╗██╔╝
██║   ██║██║   ██║███████║██║     ██║   ██║    ╚████╔╝ ██╔████╔██║███████║ ╚███╔╝     ╱|、
██║▄▄ ██║██║   ██║██╔══██║██║     ██║   ██║     ╚██╔╝  ██║╚██╔╝██║██╔══██║ ██╔██╗    (˚ˎ 。7
╚██████╔╝╚██████╔╝██║  ██║███████╗██║   ██║      ██║   ██║ ╚═╝ ██║██║  ██║██╔╝ ██╗    |、˜〵
 ╚══▀▀═╝  ╚═════╝ ╚═╝  ╚═╝╚══════╝╚═╝   ╚═╝      ╚═╝   ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    じしˍ,)ノ
```

# QualityMax

**Independent verification for AI-written code.**

Discover user journeys, generate and run tests, review changes, and inspect the evidence behind your next release.

[Website](https://qualitymax.io) · [Open QualityMax](https://app.qualitymax.io) · [Documentation](https://docs.qualitymax.io/) · [Standalone tools](https://docs.qualitymax.io/free-and-open-source/)

This repository is the public product guide and documentation entry point. The hosted platform source is maintained separately. Individual tools below have their own source repositories, licenses, and requirements.

## Choose your starting point

| I want to… | Start here |
|---|---|
| Generate coverage and inspect a first completed run | [Web app quickstart](https://docs.qualitymax.io/quickstart-web-app/) |
| Connect my coding agent to hosted QualityMax | [MCP quickstart](https://docs.qualitymax.io/quickstart-mcp/) |
| Use the platform CLI and local execution agent | [CLI quickstart](https://docs.qualitymax.io/quickstart-cli/) |
| Try local tools without a QualityMax account | [Standalone tools guide](https://docs.qualitymax.io/free-and-open-source/) |
| Evaluate QualityMax for my team | [Team evaluator guide](https://docs.qualitymax.io/persona-team-evaluator/) |

Hosted workflows require a QualityMax account and use the allowances of your plan. Standalone tools have separate prerequisites; model providers, coding-agent subscriptions, and your own compute can have costs.

## From a user journey to reviewable evidence

```text
┌─ FROM JOURNEY TO EVIDENCE ───────────────────────────────┐
│                                                          │
│   01  DISCOVER    Map application journeys               │
│        │                                                 │
│   02  GENERATE    Create cases and scripts               │
│        │                                                 │
│   03  REVIEW      Check intent and assertions            │
│        │                                                 │
│   04  EXECUTE     Run the reviewed tests                 │
│        │                                                 │
│   05  INSPECT     Read results and available artifacts   │
│        │                                                 │
│   06  REFINE      Review repairs if needed; rerun        │
│        │                                                 │
│        └────────> Retain the evidence                    │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

QualityMax organizes work as **Projects → Test Cases → Automation Scripts**. A test case records expected behavior; scripts implement that intent for a framework. Inspect the completed execution and its available artifacts before treating a queued job or a generated script as proof. [Core concepts](https://docs.qualitymax.io/core-concepts/)

## Explore the platform

| Capability | What to expect | Documentation |
|---|---|---|
| Discovery and generation | Discover application journeys and produce reviewable cases and scripts | [Discovery & Generation](https://docs.qualitymax.io/discovery-generation/) |
| PR verification | Review changes, run supported suites, and check deployed previews | [Code Review & Gates](https://docs.qualitymax.io/code-review-gates/) |
| Nexus | Specialist reviews with attributed findings and shareable reports | [Nexus review](https://docs.qualitymax.io/nexus-review/) |
| AI application validation | Conversation evaluation, adversarial evaluations, and hallucination checks | [AI validation](https://docs.qualitymax.io/ai-validation/) |
| Agentic Eyes | Simulated browser journeys with observations about usability and friction | [Agentic Eyes](https://docs.qualitymax.io/agentic-eyes/) |
| Self-healing | Investigate failed tests and review proposed repairs | [Self-healing](https://docs.qualitymax.io/self-healing/) |
| Slack | Project-aware questions and supported actions through proposals and approval | [Slack](https://docs.qualitymax.io/slack/) |
| Grounded project context | Reuse verified facts and inspect their sources | [Memory & Grounding](https://docs.qualitymax.io/memory-grounding/) |
| Test management and portability | Organize cases/scripts, import assets, and exchange QTML | [Test management](https://docs.qualitymax.io/test-management/) · [QTML](https://docs.qualitymax.io/export-qtml/) |
| Performance | k6 workflows and migration guides for existing performance assets | [Performance](https://docs.qualitymax.io/performance/) |
| Mobile | Responsive readiness audits and managed mobile-flow guidance | [Mobile](https://docs.qualitymax.io/mobile/) |
| Evidence | Interpret execution artifacts, signed verdicts, and exposure receipts | [Evidence & Trust](https://docs.qualitymax.io/evidence-trust/) |

### Understand the PR gates

| Gate | Purpose | Behavior |
|---|---|---|
| Alpha | Review the diff and run static security checks | Blocking verdicts can fail the check |
| Gamma | Run a detected, supported native test suite | Failures can fail the check; skips when there is no applicable suite |
| Delta | Run QualityMax-generated project scripts | Advisory warnings |
| Beta | Run browser tests against a deployed preview | Triggered by the successful deployment event; failures can fail the check |

Configure your repository's required checks for merge enforcement. Enabled gates, supported frameworks, preview deployment events, and project settings determine what runs. The GitHub App and the explicit GitHub Action have different setup and execution paths. See [gate verdicts](https://docs.qualitymax.io/code-review-gates-verdicts/) for the decision rules.

Nexus on-demand specialist review is a separate workflow from automatic PR review. A Slack reply from one active specialist does not imply that a full multi-persona review ran.

## Local tools and integrations

```text
┌─ FIND YOUR WORKSPACE ────────────────────────────────────┐
│                                                          │
│   QualityMax                                             │
│   ├── In the browser                                     │
│   │   └── Hosted projects, tests, runs, and reports      │
│   ├── In your terminal                                   │
│   │   ├── qmax-code       Coding and QA agent            │
│   │   └── qmax            Platform CLI / local agent     │
│   ├── In your coding agent                               │
│   │   ├── qmax-mcp        Local browser QA tools         │
│   │   └── Free QA Skills  Reusable QA workflows          │
│   └── In your workflow                                   │
│       ├── GitHub          PR checks and Actions          │
│       └── n8n / Slack     Integrations and context       │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

| Project | Use it for | License / status |
|---|---|---|
| [qmax-mcp](https://github.com/Quality-Max/qmax-mcp) | Four standalone MCP tools: scan, inspect, generate a Playwright reproduction, run a test | MIT |
| [qmax-code](https://github.com/Quality-Max/qmax-code) | A QA terminal agent with standalone and hosted-connected modes | Source available, FSL-1.1-ALv2 |
| [Free QA Skills](https://github.com/Quality-Max/free-qa-skills) | QA workflows inside supported coding agents | Apache-2.0 |
| [9lives](https://github.com/Quality-Max/9lives) | Local test repair, reruns, and reviewable diffs | MIT; prototype |
| [Test Grader](https://github.com/Quality-Max/qualitymax-grader) | Static Playwright test-quality grading | Apache-2.0 |
| [Supply Chain Scanner](https://github.com/Quality-Max/supply-chain-scanner) | Python dependency supply-chain checks | Apache-2.0 |
| [qmax local agent](https://github.com/Quality-Max/qmax-local-agent) | Platform CLI and local test execution | Apache-2.0 |
| [GitHub Action](https://github.com/Quality-Max/qualitymax-github-action) | Explicit CI workflows with results and report links | MIT |
| [n8n integration](https://github.com/Quality-Max/n8n-nodes-qualitymax) | Connect project, test, and performance workflows | MIT |
| [qmax-receipt](https://github.com/Quality-Max/qmax-receipt) | Shared signed exposure-receipt schema | MIT |

**Local MCP versus hosted MCP:** starting the standalone qmax-mcp package exposes its local tools without a QualityMax account. To use hosted projects and execution, follow the [hosted MCP quickstart](https://docs.qualitymax.io/quickstart-mcp/) or the package's documented proxy mode. They are distinct connection paths.

For qmax-code installation, use the [maintained source README](https://github.com/Quality-Max/qmax-code#install) and [latest release](https://github.com/Quality-Max/qmax-code/releases/latest). Advanced terminal commands can be experimental; check the source README for current availability.

## See concrete examples

- [Local MCP walkthrough](https://github.com/Quality-Max/qmax-mcp/tree/main/demo): inspection, reproduction, and execution artifacts.
- [9lives repair demo](https://github.com/Quality-Max/9lives/blob/main/demo/heal.gif): a local repair workflow.
- [Test Grader examples](https://github.com/Quality-Max/qualitymax-grader#live-example): sample grades and actionable findings.
- [n8n regression-to-Slack workflow](https://github.com/Quality-Max/n8n-nodes-qualitymax#hero-workflow): an integration template with setup requirements.
- [CI example repository](https://github.com/Quality-Max/qualitymax-demo-playground): inspect the example and its current run history.
- [Self-healing sandbox cookbook](https://github.com/Quality-Max/e2b-cookbook-self-healing-tests): a separate example with its own provider and compute requirements.

These examples demonstrate their named workflows; they are not live production certifications or universal performance benchmarks. The [example guide](docs/examples.md) explains what to inspect.

## Deployment and embedding

The hosted application is the standard evaluation path. Sovereign is a **private preview** with design partners; supported topology and operational responsibilities are agreed during evaluation. [Deployment guide](https://docs.qualitymax.io/deployment/)

For embedding workflows and evaluating branding requirements, see [Partner / White-label](https://docs.qualitymax.io/partner-white-label/).

## Help and contributions

Use [documentation](https://docs.qualitymax.io/) for setup and product behavior, [issues](https://github.com/Quality-Max/qualitymax/issues) for public bugs and documentation feedback, and [CONTRIBUTING.md](CONTRIBUTING.md) for contributions. Report sensitive issues through [SECURITY.md](SECURITY.md).

This repository's [license](LICENSE) is separate from the licenses of the individual tools linked above.
