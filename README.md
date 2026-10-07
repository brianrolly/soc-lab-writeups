# SOC Writeups

Detection engineering and purple-team writeups from authorized client work, covering OPNsense, Suricata IDS, and a Wazuh/OpenSearch SIEM. The writeups show the methods, sanitized evidence, and operational artifacts behind their claims.

**Read them on the live site: [brianrolly.github.io/soc-lab-writeups](https://brianrolly.github.io/soc-lab-writeups/)**

| Writeup | Area | Summary |
|---|---|---|
| [Rogue-Agent Log Injection](https://brianrolly.github.io/soc-lab-writeups/rogue-agent-log-injection.html) | Purple team | An anonymous host enrolls into the SIEM with no credential, becomes a trusted agent, and injects a forged security alert. Sanitized command and output excerpts document the chain and verified fix. |
| [Vertical Scan Detection](https://brianrolly.github.io/soc-lab-writeups/vertical-scan-detection.html) | Detection engineering | A port-scan detector on OPNsense + Wazuh, tuned from a six-hour sample at five-minute granularity after a seven-day study exposed a measurement error. Controlled and real-world results document coverage and its limits. |
| [What a 9.8 Actually Means](https://brianrolly.github.io/soc-lab-writeups/what-a-98-means.html) | Validation | A credentialed scan found a CVSS 9.8 in the SIEM's bundled Node.js. The triage separates version-vulnerable from exploitable: reachability checks, inspection of the then-current vendor package, and why one of two scanners never saw it. |
| [What Three Emulations Caught — and What They Missed](https://brianrolly.github.io/soc-lab-writeups/caldera-discovery-detection.html) | Endpoint | Three CALDERA operations against a monitored Linux host, from first-minutes discovery to a full staging-and-exfiltration chain. auditd captured all seven stages; Wazuh alerted on two. The gap list is the deliverable. |
| [The Scanner My Detection Couldn’t See](https://brianrolly.github.io/soc-lab-writeups/modat-distributed-scanner.html) | Threat intel | A real commercial internet-wide scanner living in the logs — 79 IPs, one netblock, splitting targets so each source stayed under threshold. Characterized, with the honest reason per-source detection misses it. |
| [The Query That Exposed a Broken SIEM](https://brianrolly.github.io/soc-lab-writeups/indexer-heap-undersizing.html) | SIEM ops | Measuring detection data exposed a 1 GB heap on a 12 GB host. Queries hit the parent circuit breaker; raising the heap cleared the tested failures. Broader search risks and remaining shard pressure are documented. |
| [From Alert to Action](https://brianrolly.github.io/soc-lab-writeups/operational-runbooks.html) | Response | The runbooks that turn a firing alert into a decision: a high-severity Linux IR workflow, and a scan-triage guide for reading firewall and Suricata schemas side by side. |

The HTML files in this repository are the published pages.
