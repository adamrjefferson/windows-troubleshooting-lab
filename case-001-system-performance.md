# Case 001 — Windows System Performance Investigation

**Project:** Windows Troubleshooting & Diagnostics Lab  
**Date:** October 22, 2026  
**Operating System:** Windows  
**Device:** Personal laptop  
**Diagnostic Tool:** Windows Task Manager  
**Case Status:** Completed — No confirmed fault

## 1. Objective

Perform a baseline performance assessment of a Windows laptop using built-in diagnostic tools, evaluate system resource utilization, investigate any unusual findings, and document recommendations.

## 2. Initial System Assessment

The laptop was functioning normally without noticeable freezing, lag, application crashes, or other performance issues.

The following baseline measurements were collected using Windows Task Manager:

| Component | Observation |
|---|---|
| Processor | Intel Core Ultra 5 225U |
| CPU utilization | 10% |
| Installed RAM | 8 GB |
| Initial memory utilization | 84% |
| Primary storage | SSD |
| Disk active time | 9% |

### Initial Findings

CPU and storage activity were relatively low during the observation.

Memory utilization was elevated at 84%, prompting further investigation.

## 3. Memory Investigation

Additional information was collected from Task Manager's Performance and Processes sections.

| Memory Metric | Result |
|---|---|
| In use (Compressed) | 6.5 GB (389 MB compressed) |
| Available | 1.0 GB |
| Cached | 862 MB |
| Committed | 15.0 / 20.0 GB |

### Top Memory-Consuming Processes

| Process | Reported Memory |
|---|---:|
| Google Chrome | 654.6 MB |
| Windows Widgets | 127.2 MB |
| Microsoft Defender Antimalware | 111.2 MB |
| Microsoft Edge | 99.1 MB |
| Task Manager | 80.5 MB |

## 4. Analysis

The investigation identified elevated physical memory utilization and limited available RAM.

Windows memory compression was active, with 389 MB reported as compressed. This is a normal operating system memory-management mechanism and does not independently indicate a problem.

Committed memory was 15.0 GB against a 20.0 GB commit limit. This represents committed virtual memory, not physical RAM usage.

The five largest reported processes did not individually exhibit unusually large memory usage, and their combined usage did not account for all system memory consumption.

Although memory utilization was elevated, the laptop exhibited no noticeable performance degradation.

The available evidence did not establish a memory leak, malfunctioning application, or system fault.

## 5. Troubleshooting Actions

1. Opened Windows Task Manager.
2. Recorded CPU, memory, and storage utilization.
3. Identified memory utilization as the primary area for investigation.
4. Examined detailed memory statistics.
5. Reviewed and documented the highest memory-consuming processes.
6. Compared the diagnostic findings against observed system performance.

No system settings were changed, processes terminated, or services disabled during the investigation.

## 6. Conclusion

**Finding:** Elevated memory utilization without confirmed performance degradation.

**Resolution:** No corrective action required based on the current evidence.

The laptop remained functional throughout the assessment. The investigation established a performance baseline for future comparisons.

## 7. Recommendations

- Monitor available memory if performance problems develop.
- Review resource usage when running additional demanding applications.
- Compare future measurements against this baseline.
- Consider upgrading RAM if memory-intensive workloads cause persistent slowdowns and the hardware supports an upgrade.
- Avoid disabling system services or terminating processes without evidence of a problem.

## 8. Skills Demonstrated

- Windows Task Manager diagnostics
- CPU, memory, and storage performance analysis
- Understanding physical and virtual memory
- Process resource monitoring
- Evidence-based troubleshooting
- Technical documentation
- Preventive IT maintenance assessment

## 9. Lessons Learned

This investigation reinforced the importance of evaluating diagnostic measurements alongside actual system behavior.

High resource utilization does not automatically indicate a malfunction. Effective troubleshooting requires collecting evidence, investigating potential causes, and avoiding unnecessary corrective actions when no fault has been established.
