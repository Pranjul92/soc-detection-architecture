# Detection Strategy Aligned with MITRE ATT&CK

## Objective
Design a detection strategy that prioritizes early compromise detection,
risk amplification points, and persistent attacker control for a mid size organisation.

## Prioritized MITRE Tactics

### 1. Initial Access
Initial Access is prioritized to enable early detection and prevention of compromise,
reducing downstream impact and disruptive response actions.

### 2. Privilege Escalation
Privilege escalation represents a step-change in attacker capability and business risk,
making it a high-confidence detection anchor.

### 3. Command and Control
Command and Control is prioritized because it reflects sustained attacker control and intent,
even when initial execution is missed or bypassed.

## Attack Path Narrative
A user receives a phishing email impersonating the finance department, claiming urgent
salary-related changes and containing a malicious attachment. Due to the urgency and
personal relevance, the user downloads and executes the file, providing the attacker
initial access to the endpoint.

Once execution occurs, the attacker establishes a foothold and performs credential
access activities to obtain authentication material. Using these credentials, the
attacker attempts privilege escalation to gain higher-level access and expand control.

After achieving sufficient privileges, the attacker establishes command-and-control
communication with an external server to maintain persistence, execute commands remotely,
and enable lateral movement or data exfiltration.

## Detection Philosophy
Detection is designed around attacker behavior rather than individual events,
prioritizing confidence and intent over volume.

## Explicit Non-Goals
Not all MITRE tactics are prioritized. Execution, persistence, and reconnaissance are
deprioritized due to higher noise, overlap with other tactics, or limited internal visibility.

## Trade-Offs
This strategy favors confidence and operational impact over exhaustive coverage,
accepting certain detection gaps to reduce false positives and analyst fatigue.
