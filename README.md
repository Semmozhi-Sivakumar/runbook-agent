<img width="1512" height="672" alt="image" src="https://github.com/user-attachments/assets/03345fdc-432b-4096-9b71-5c5c67526e0f" />


<img width="1527" height="731" alt="image" src="https://github.com/user-attachments/assets/ac79341c-2457-4ea0-ba25-642fde8236ae" />



# AI-Powered Runbook Following Agent

## Overview

The AI-Powered Runbook Following Agent automates operational runbooks used by DevOps and Site Reliability Engineering (SRE) teams.

Traditionally, when a system incident occurs, engineers manually read runbooks and execute recovery steps. This project reduces manual effort by automatically parsing runbooks, validating actions, executing approved commands, and generating execution reports.

The system demonstrates agentic workflows, operational automation, safety controls, and DevOps best practices.

---

## Problem Statement

During production incidents, engineers often need to:

- Read runbooks manually
- Identify required actions
- Execute commands one by one
- Verify results
- Document actions taken

This process can be slow and error-prone, especially during critical outages.

The Runbook Following Agent automates these repetitive operational tasks while maintaining safety controls and human oversight.

---

## Features

### Runbook Parsing
- Reads operational runbooks written in Markdown.
- Extracts executable steps automatically.

### Command Mapping
- Maps runbook instructions to approved shell commands.
- Prevents execution of unknown actions.

### Safety Validation
- Uses an allowlist of approved commands.
- Blocks unauthorized or dangerous commands.

### Human Approval Workflow
- Requests approval before executing sensitive operations.
- Supports human-in-the-loop automation.

### Command Execution
- Executes validated commands through a controlled execution layer.
- Captures outputs and execution status.

### Execution Reporting
- Generates detailed execution reports.
- Records success, failure, timestamps, and outputs.

### Audit Support
- Maintains execution history for operational visibility.

---

## Architecture

```text
Runbook (Markdown)
        │
        ▼
Runbook Parser
        │
        ▼
Step Extraction
        │
        ▼
Command Mapping
        │
        ▼
Safety Validation
        │
        ▼
Approval Check
        │
        ▼
Command Execution
        │
        ▼
Report Generation
```

---

## Technology Stack

### Programming Language
- Python 3.x

### Frontend
- Streamlit

### Backend
- Python

### Libraries
- Streamlit
- subprocess
- pathlib
- markdown processing libraries
- JSON

### Version Control
- Git
- GitHub

---

## Project Structure

```text
runbook-agent/
│
├── app.py
├── parser.py
├── executor.py
├── report.py
├── auth.py
├── permissions.py
├── audit.py
├── active_users.py
├── failure_analysis.py
├── data_stores.py
├── mcp_server.py
│
├── runbooks/
│   ├── restart_nginx.md
│   ├── high_cpu.md
│   └── disk_full.md
│
├── requirements.txt
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/Semmozhi-Sivakumar/runbook-agent.git
cd runbook-agent
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Environment

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Application

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

## Sample Workflow

1. User selects a runbook.
2. Agent parses runbook steps.
3. System maps instructions to approved commands.
4. Safety validation is performed.
5. Approval is requested for sensitive actions.
6. Commands are executed.
7. Results are collected.
8. Execution report is generated.

---

## Example Use Cases

### Restart NGINX Service

Runbook:

```text
Check NGINX status
Restart NGINX
Verify service health
```

Agent Actions:

```bash
systemctl status nginx
systemctl restart nginx
systemctl status nginx
```

---

### High CPU Investigation

Runbook:

```text
Check CPU utilization
Identify top processes
Collect diagnostics
```

---

### Disk Space Troubleshooting

Runbook:

```text
Check disk usage
Identify large files
Generate cleanup recommendations
```

---

## Security Considerations

- Command allowlist enforcement
- Human approval for risky actions
- Controlled command execution
- Audit logging
- Execution reporting

---

## Future Enhancements

- Integration with monitoring tools
- Real-time incident detection
- LLM-based runbook understanding
- Cloud deployment
- Role-based access control
- Notification integrations
- Kubernetes support

---

## Skills Demonstrated

- Python Development
- DevOps Automation
- Agentic Workflows
- Operational Runbooks
- Safety Validation
- Command Execution
- Streamlit Development
- Git & GitHub
- Incident Response Automation

---

## Author

Semmozhi Sivakumar

GitHub:
https://github.com/Semmozhi-Sivakumar
