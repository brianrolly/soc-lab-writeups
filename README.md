# SOC-Lab Writeups

Detection engineering and purple-team writeups covering OPNsense, Suricata IDS, and a Wazuh/OpenSearch SIEM. Each writeup backs its claims with the queries and raw output behind them.

**Read them on the live site: [brianrolly.github.io/soc-lab-writeups](https://brianrolly.github.io/soc-lab-writeups/)**

| Writeup | Area | Summary |
|---|---|---|
| [Rogue-Agent Log Injection](https://brianrolly.github.io/soc-lab-writeups/rogue-agent-log-injection.html) | Purple team | An anonymous host enrolls into the SIEM with no credential, becomes a trusted agent, and injects a forged security alert. Full kill chain with verbatim output, plus the verified fix. |
| [Vertical Scan Detection](https://brianrolly.github.io/soc-lab-writeups/vertical-scan-detection.html) | Detection engineering | A measurement-driven port-scan detector on OPNsense + Wazuh. Threshold tuned from a week of real traffic, validated against controlled and real-world scans, with the evasion gaps mapped honestly. |
| [What a 9.8 Actually Means](https://brianrolly.github.io/soc-lab-writeups/what-a-98-means.html) | Validation | A credentialed scan found a CVSS 9.8 in the SIEM's own bundled Node.js. The triage that separates version-vulnerable from exploitable: three reachability checks, a vendor that ships it unfixed, and why one of two scanners never saw it. |
| [What Three Emulations Caught — and What They Missed](https://brianrolly.github.io/soc-lab-writeups/caldera-discovery-detection.html) | Endpoint | Three CALDERA operations against a monitored Linux host, from first-minutes discovery to a full staging-and-exfiltration chain. auditd captured all seven stages; Wazuh alerted on two. The gap list is the deliverable. |
| [The Scanner My Detection Couldn’t See](https://brianrolly.github.io/soc-lab-writeups/modat-distributed-scanner.html) | Threat intel | A real commercial internet-wide scanner living in the logs — 79 IPs, one netblock, splitting targets so each source stayed under threshold. Characterized, with the honest reason per-source detection misses it. |
| [The Query That Exposed a Broken SIEM](https://brianrolly.github.io/soc-lab-writeups/indexer-heap-undersizing.html) | SIEM ops | Measuring detection data exposed a 1 GB heap on a 12 GB host — a capacity defect with no symptom that would have silently broken every dashboard. Found, diagnosed, fixed, verified. |
| [From Alert to Action](https://brianrolly.github.io/soc-lab-writeups/operational-runbooks.html) | Response | The runbooks that turn a firing alert into a decision: a high-severity Linux IR workflow, and a scan-triage guide for reading firewall and Suricata schemas side by side. |

The HTML files in this repository are the published pages.
