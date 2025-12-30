# SIEM Requirements – VA Context

## Purpose
Develop defensible SIEM requirements aligned to NIST and OMB guidance.

## Inputs Required
- System description
- Data types
- Hosting model

## Prompt
You are a federal cybersecurity architect supporting a FISMA-regulated environment.

Develop a set of SIEM requirements for the following system:

SYSTEM CONTEXT:
- Organization: Department of Veterans Affairs (VA)
- System type: [e.g., genomics platform, clinical research system, enterprise application]
- Data types: [e.g., PII, PHI, genomic data]
- Hosting model: [on-prem / cloud / hybrid]
- FISMA impact level: [Low / Moderate / High]

TASK:
1. Identify core SIEM functional requirements needed to support:
   - Continuous monitoring
   - Incident detection and response
   - Audit and compliance reporting
   - Threat detection and correlation

2. Align requirements to relevant federal guidance, including:
   - NIST SP 800-53
   - NIST SP 800-61
   - OMB FISMA reporting expectations

3. Group requirements into logical categories such as:
   - Log collection and ingestion
   - Correlation and analytics
   - Alerting and response support
   - Retention and data management
   - Reporting and dashboards
   - Integration with other security tools

4. For each requirement, provide:
   - A clear, testable requirement statement
   - The security objective it supports
   - Relevant NIST control references where applicable

CONSTRAINTS:
- Do not speculate beyond the provided system context
- Clearly state any assumptions
- Avoid vendor-specific language
- Use clear, federal-appropriate language suitable for acquisition artifacts

OUTPUT FORMAT:
- A structured table of SIEM requirements
- Followed by a short summary highlighting key risks if SIEM capabilities are not implemented

## Expected Output
- Requirements table
- Risks and assumptions

## Constraints
- Do not speculate
- Cite NIST or OMB where applicable

## Notes
Initial draft