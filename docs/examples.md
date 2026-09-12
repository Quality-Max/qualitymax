# Examples and evidence

Use these public examples to understand one workflow at a time. Follow each repository's setup instructions and inspect its current status before running it.

| Example | What to inspect |
|---|---|
| [qmax-mcp demo](https://github.com/Quality-Max/qmax-mcp/tree/main/demo) | Page observations, chosen locators, generated reproduction, and the execution result |
| [9lives repair recording](https://github.com/Quality-Max/9lives/blob/main/demo/heal.gif) | The original failure, repair proposal, rerun, and final diff; 9lives is a prototype |
| [Grader examples](https://github.com/Quality-Max/qualitymax-grader#live-example) | Why different tests receive different grades; a static grade does not establish application correctness |
| [GitHub Action example](https://github.com/Quality-Max/qualitymax-demo-playground) | Workflow configuration and current run history, including the tested revision |
| [n8n integration](https://github.com/Quality-Max/n8n-nodes-qualitymax#hero-workflow) | Required connections, execution polling, and the final report link |
| [Sandbox cookbook](https://github.com/Quality-Max/e2b-cookbook-self-healing-tests) | Isolated execution setup, model requirements, and the rerun result |

For a platform evaluation, follow the [web quickstart](https://docs.qualitymax.io/quickstart-web-app/) and retain the project/run identifiers, tested revision or target, expected behavior, result, and available artifacts. A queued job, generated test, or screenshot without an assertion is not a passing execution.

When presenting a repair, show the same assertion failing before the change and passing afterward. Inspect any changed assertion separately. For a PR gate, include the required-check configuration and the exact commit the check evaluated.

Remove account data, credentials, and customer content before publishing screenshots or reports. Label synthetic examples and recordings as examples rather than current production evidence. See [Evidence & Trust](https://docs.qualitymax.io/evidence-trust/) for interpretation limits.
