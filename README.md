📟 On-Call Shift Handling – L2 / L3 Support
1. Purpose & Scope

This document defines the on-call support process for L2/L3 engineers, ensuring:

Timely incident response

Clear ownership and escalation

Minimal service disruption

Consistent communication and documentation

Scope:
Applies to all production incidents, alerts, and customer-reported issues handled during on-call hours.

2. On-Call Coverage Model
Item	Details
Support Level	L2 / L3
Coverage Type	24x7 / Business Hours (update as applicable)
Shift Rotation	Weekly / Bi-weekly
Primary On-Call	Assigned Engineer
Secondary / Backup	Assigned Engineer
Escalation Manager	Engineering Manager / Duty Manager
3. Roles & Responsibilities
🔹 L2 On-Call Engineer

Monitor alerts from monitoring tools (Splunk, Grafana, Dynatrace, etc.)

Perform initial triage and impact analysis

Resolve known issues using runbooks / SOPs

Escalate to L3 when:

Issue is complex

Code/config changes are required

Maintain incident updates and documentation

🔹 L3 On-Call Engineer

Handle complex, high-severity, or recurring incidents

Perform deep-dive troubleshooting (code, infra, DB, performance)

Implement temporary fixes or permanent solutions

Coordinate with development, SRE, infra, or vendors

Lead RCA for critical incidents

🔹 Incident / Duty Manager (if applicable)

Ensure SLA adherence

Coordinate communication with stakeholders

Support decision-making during major incidents

4. Alert Intake & Monitoring
Monitoring & Alert Sources

Dynatrace

Grafana

Splunk

Cloud Alerts (AWS / Azure / OCI)

ServiceNow / PagerDuty / OpsGenie

Alert Validation Checklist

Is the alert genuine or false positive?

Impacted services / regions?

Severity level (P1 / P2 / P3 / P4)?

Customer impact confirmed?

5. Incident Severity Definition
Severity	Description	Response SLA
P1	Complete outage / critical business impact	Immediate
P2	Partial outage / degraded performance	≤ 30 mins
P3	Minor issue / workaround available	≤ 4 hrs
P4	Informational / low impact	Next business day
6. On-Call Incident Handling Flow

Alert received

Acknowledge alert within SLA

Perform impact analysis

Assign severity

Start investigation

Mitigation / resolution

Communication & updates

Incident closure

RCA (if required)

7. Escalation Matrix
Scenario	Action
No response from primary	Escalate to secondary
Issue unresolved in SLA	Escalate to L3
Major incident	Notify Duty Manager
External dependency	Engage vendor/cloud provider
8. Communication Guidelines
Internal Communication

Incident bridge (Teams / Slack)

ServiceNow updates

Status page (if applicable)

Update Frequency

P1: Every 15–30 mins

P2: Every 60 mins

P3/P4: As needed

9. Documentation & Ticketing

All incidents must be logged in ServiceNow

Include:

Timeline

Root cause

Resolution steps

Preventive actions

Link related alerts, dashboards, and logs

10. Post-Incident Activities (RCA)
RCA Mandatory For:

P1 incidents

Repeated P2 incidents

SLA breaches

RCA Should Include:

What happened

Why it happened

What worked well

What didn’t

Action items with owners & timelines

11. Knowledge Base & Runbooks

Refer existing SOPs and runbooks

Create new documentation if gaps are identified

Update runbooks after incident learnings

12. On-Call Best Practices

Always acknowledge alerts promptly

Avoid assumptions—validate with data

Communicate clearly and proactively

Document while handling incidents

Handover properly at shift end

13. Shift Handover Process

Pending incidents

Known risks or alerts

Ongoing investigations

Any planned changes during next shift

14. Compliance & Audit Readiness

Follow ITIL incident management practices

Ensure audit-ready documentation

Adhere to security and access policies

15. References

Incident Management Policy

Monitoring Dashboards

Runbooks & SOPs

ServiceNow Guide
