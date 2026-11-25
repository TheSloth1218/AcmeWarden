# AcmeWarden

AcmeWarden is an AI-powered security log analysis and threat detection tool built with Python and Qwen. It analyzes security logs, classifies potentially malicious activity, assigns severity scores, and generates detection rules based on its findings.

## Features

- AI-powered security log classification
- BENIGN, SUSPICIOUS, MALICIOUS, and UNKNOWN classifications
- Severity scoring from 1 to 5, with 0 used for unknown or invalid results
- Structured JSON output with defensive parsing
- Concurrent batch processing of log entries
- CSV and JSON result exports
- Automated Sigma and regex detection rule generation
- Prompt injection mitigation
- Offline testing and input validation
- Secure API key handling
- Optimized inference with streaming responses and disabled thinking mode

## Supported Log Sources

- Linux SSH authentication logs
- Apache access logs
- Firewall logs
- Windows Security event logs
- Sysmon process creation logs
- Custom log files

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- OpenAI Python SDK
- Access to a Qwen-compatible inference API

Install the required dependency:

```bash
pip install openai
```

## Usage

1. Clone or download this repository.
2. Open the Jupyter notebook.
3. Configure the API endpoint and enter your API key when prompted.
4. Set `LOG_FILE` to the log file you want to analyze.
5. Execute the notebook cells in order.
6. Review the classification results and generated detection rules.

## Output Files

| File | Description |
|---|---|
| `triage_results.csv` | Security log classification results in CSV format |
| `triage_results.json` | Structured analysis results in JSON format |
| `detection_rule.txt` | AI-generated detection rule |
| `detection_rule_sigma.txt` | Sigma detection rule |
| `detection_rule_grep_extended_regex.txt` | Regex-based detection rule for Linux log analysis |

## Security Considerations

AcmeWarden treats log entries as untrusted input and uses hardened prompts to mitigate prompt injection. API keys are entered at runtime and are not stored in the source code.

## Technologies

- Python
- Qwen
- GPUStack
- OpenAI-compatible API
- Jupyter
- Sigma
- Regular expressions

## License

Distributed under the MIT License. See `LICENSE` for details.
