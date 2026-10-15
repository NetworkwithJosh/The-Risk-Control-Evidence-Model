Lesson content

Evidence should support the specific control activity being tested.

Evaluate evidence using four questions:

Relevance: Does it address the control?

Reliability: Can you trust the source?

Completeness: Does it cover the full population or period?

Timeliness: Does it relate to the correct date or review period?

A screenshot may show that a setting existed, but not when it was configured or whether it covered every system.

A signed checklist may show approval, but not whether the reviewer received a complete population.

Strong evidence usually connects the population, procedure, reviewer, date, conclusion, and follow-up.


# Risk-Control-Evidence Model
### Cybersecurity Governance, Risk Management & IT Audit Portfolio Project

## 1. Project Overview

The Risk-Control-Evidence Model is a practical GRC project designed to demonstrate how organizations identify cybersecurity risks, establish internal controls, and evaluate audit evidence.

The project focuses on the relationship between:

**Risk → Control → Evidence → Testing → Findings → Remediation**

The purpose is to develop an understanding of how IT auditors and cybersecurity controls consultants evaluate whether organizational controls are appropriately designed and operating effectively.

This project uses hypothetical organizational scenarios and sample evidence to simulate real-world IT audit and risk assessment activities.

### Project Objectives

- Identify cybersecurity and operational risks.
- Understand how control activities mitigate identified risks.
- Evaluate evidence for relevance, reliability, completeness, and timeliness.
- Distinguish management assertions from independently verified evidence.
- Identify control deficiencies and potential business impacts.
- Develop appropriate audit evidence requests.
- Document preliminary findings and remediation recommendations.

---

# 2. Understanding the Risk-Control-Evidence Relationship

## Risk

A risk represents a potential event that could negatively affect an organization's operations, information security, finances, or regulatory compliance.

## Control

A control is a policy, process, procedure, or technical safeguard designed to prevent, detect, or reduce an identified risk.

## Evidence

Evidence consists of records, documentation, system configurations, logs, and other information used to evaluate whether a control has been implemented or operated as intended.

## Testing

Control testing evaluates whether a control is appropriately designed and whether it operated effectively during the period under review.

## Findings

An audit finding documents an identified control weakness, supported by sufficient and appropriate evidence.

## Remediation

Remediation involves corrective actions taken to address an identified weakness and reduce associated risk.

### Example

| Component | Example |
|---|---|
| Risk | Former employees may retain unauthorized system access. |
| Control | Employee access is revoked upon termination. |
| Evidence | Termination records, IAM logs, and deprovisioning tickets. |
| Testing | Compare termination dates against account deactivation timestamps. |
| Finding | Access was not removed within the required timeframe. |
| Remediation | Automate termination-based access removal and monitor exceptions. |

---

# 3. Audit Evidence Evaluation Framework

Audit evidence should support the specific control activity being tested.

Evidence is evaluated using four criteria.

## 3.1 Relevance

Does the evidence directly address the control objective?

Example:

An AWS logging configuration may support a logging control, but it does not independently demonstrate that security personnel reviewed the logs.

## 3.2 Reliability

Can the evidence source be trusted?

Consider:

- Who produced the evidence?
- Was it generated directly from a system?
- Can its authenticity be verified?
- Has it been modified?
- Does independent evidence corroborate it?

## 3.3 Completeness

Does the evidence cover the required population, systems, transactions, or audit period?

Example:

A screenshot showing one employee's permissions does not establish that every in-scope employee participated in a quarterly access review.

## 3.4 Timeliness

Does the evidence correspond to the correct review period or date?

Example:

A configuration export last modified in February does not independently establish that the control operated effectively throughout the remainder of the year.

### Evidence Evaluation Matrix

| Criterion | Audit Question |
|---|---|
| Relevance | Does the evidence address the specific control? |
| Reliability | Can the source and accuracy be verified? |
| Completeness | Does it cover the required scope? |
| Timeliness | Does it correspond to the required period? |

---

# 4. Evidence Inventory

Three hypothetical evidence documents were evaluated.

| Evidence ID | Document | Primary Subject |
|---|---|---|
| E02 | Q2 2026 Access Review Certification Email | Identity and Access Management |
| E11 | AWS CloudTrail Configuration Export | Logging and Log Retention |
| E09 | Incident IR-2026-004 | Incident Response and Change Management |

The assessments below distinguish information recorded in the documents from conclusions requiring additional verification.

---

# 5. Evidence Assessment: E02

## Q2 2026 Access Review Certification

### Evidence Overview

**Document:** E02_Access_Review_Certification_Email.txt

**Sender:** Marcus Lee, Chief Information Security Officer

**Date:** June 28, 2026

**Subject:** Q2 2026 Access Review Certification

### Management Certification

> I certify that the Q2 2026 access review has been completed for all in-scope systems and that all identified removals have been completed.

## 5.1 What the Evidence Supports

The document supports that:

- The CISO issued a management certification.
- The certification relates to Q2 2026.
- Management represented that all in-scope systems were reviewed.
- Management represented that identified access removals were completed.

The email establishes a documented management assertion.

It does not independently verify the underlying review activities.

## 5.2 What the Evidence Does Not Support

The email alone does not establish:

- Which systems were included in the review.
- Whether the user population was complete.
- Which individuals performed the reviews.
- When individual reviews occurred.
- Which access permissions were evaluated.
- Whether inappropriate permissions were identified.
- Whether required access removals actually occurred.
- Whether remediation was completed within required deadlines.

## 5.3 Additional Evidence Requested

### Request 1: User Access Population

Obtain system-generated user and permission listings for the relevant systems.

**Purpose:**

Determine whether the access review included the complete in-scope population.

### Request 2: Access Review Records

Obtain documentation showing:

- Assigned reviewers.
- Review dates.
- Users and permissions examined.
- Reviewer decisions.
- Approvals or identified exceptions.

**Purpose:**

Determine whether the required review activities were performed.

### Request 3: Access Removal Evidence

Obtain:

- Deprovisioning tickets.
- IAM audit logs.
- Account modification records.
- Evidence of exception closure.

**Purpose:**

Determine whether access removal decisions were implemented.

## 5.4 Evidence Quality Assessment

| Criterion | Assessment |
|---|---|
| Relevance | Relevant to the access review control. |
| Reliability | Management certification; underlying activities require corroboration. |
| Completeness | The email does not demonstrate complete population coverage. |
| Timeliness | Dated within Q2 2026, but individual review and remediation dates are not established. |

### Preliminary Conclusion

**Evidence Status: Additional Evidence Required**

The certification establishes that management asserted completion of the quarterly access review.

However, the document alone is insufficient to conclude that the control operated effectively.

No confirmed control failure can be established solely from this certification.

---

# 6. Evidence Assessment: E11

## AWS CloudTrail Logging and Retention

### Evidence Overview

**Document:** E11_AWS_Log_Retention_Configuration.txt

### Recorded Configuration

| Configuration Field | Recorded Value |
|---|---|
| AWS Account | northstar-prod |
| CloudTrail Trail | organization-trail |
| Logging | Enabled |
| S3 Lifecycle Retention | 90 days |
| CloudWatch Retention | 90 days |
| Last Modified | February 12, 2026 |
| Configuration Owner | Theo Nakamura |

## 6.1 What the Evidence Supports

The configuration export records that:

- Logging was configured as enabled.
- The identified trail was `organization-trail`.
- S3 lifecycle retention was configured as 90 days.
- CloudWatch retention was configured as 90 days.
- Theo Nakamura was identified as the configuration owner.
- The reported last-modified date was February 12, 2026.

The evidence is relevant to the existence and configuration of logging and retention settings.

## 6.2 What the Evidence Does Not Support

The export alone does not establish:

- Whether all required AWS accounts and resources were covered.
- Whether log collection operated continuously during the audit period.
- Whether the required log records were actually retained.
- Whether the configuration met organizational retention requirements.
- Whether logs were reviewed or monitored.
- Whether the configuration changed during the period under review.
- Whether the export was obtained directly from an authoritative AWS source.

Logging configuration, log monitoring, and log retention represent related but distinct control activities.

## 6.3 Additional Evidence Requested

### Request 1: AWS Configuration Verification

Obtain authoritative AWS configuration records demonstrating the applicable CloudTrail and retention settings.

**Purpose:**

Validate the accuracy and reliability of the configuration export.

### Request 2: AWS Account and Resource Inventory

Obtain the inventory of AWS accounts and relevant resources within the control scope.

**Purpose:**

Determine whether required systems and accounts are covered by logging controls.

### Request 3: Log Retention Policy

Obtain the organization's approved logging and retention requirements.

**Purpose:**

Determine the required retention duration and evaluate whether the documented settings align with policy.

### Request 4: Historical Log Retention Evidence

Obtain timestamped log records and supporting storage or retention configuration evidence covering the period being tested.

**Purpose:**

Evaluate whether required logs were collected and retained.

### Request 5: Log Review Records (If Applicable)

If the control includes monitoring, obtain records documenting log review activities.

**Purpose:**

Determine whether assigned personnel performed required monitoring activities.

## 6.4 Evidence Quality Assessment

| Criterion | Assessment |
|---|---|
| Relevance | Directly relevant to logging and retention configuration. |
| Reliability | Source authenticity and configuration accuracy require verification. |
| Completeness | Coverage of all required accounts and systems is not demonstrated. |
| Timeliness | A last-modified date is provided, but continuous effectiveness during the audit period is not established. |

### Preliminary Conclusion

**Evidence Status: Additional Evidence Required**

The export documents specific logging and retention settings.

However, the evidence does not independently establish complete logging coverage or effective retention throughout the audit period.

A 90-day setting cannot be classified as compliant or noncompliant without the applicable retention requirements and verification of actual operation.

---

# 7. Evidence Assessment: E09

## Incident IR-2026-004

### Evidence Overview

**Document:** E09_Incident_IR-2026-004.txt

| Field | Recorded Information |
|---|---|
| Incident ID | IR-2026-004 |
| Severity | 1 |
| Incident Date | April 17, 2026 |
| System | CareBridge Production |
| Customers Affected | 41 |
| Outage Duration | 52 minutes |

### Incident Summary

A production API configuration change caused elevated error rates and a service outage.

### Recorded Incident Timeline

| Time | Activity |
|---|---|
| 09:06 | Datadog alert triggered |
| 09:12 | On-call engineer acknowledged PagerDuty page |
| 09:24 | Recent configuration change identified |
| 09:41 | Rollback initiated |
| 09:58 | Service restored |

### Recorded Root Cause

Change `CHG-1842` was deployed without documented approval, and testing evidence was incomplete.

### Follow-Up Status

A postmortem was required within ten business days.

As of May 18, 2026, the postmortem remained incomplete.

## 7.1 What the Evidence Supports

The incident report documents:

- A specific production service disruption.
- The reported duration and customer impact.
- The sequence of detection and response activities.
- The reported identification of a configuration change.
- The reported rollback and restoration activities.
- A documented approval and testing concern.
- An incomplete postmortem as of the stated follow-up date.

The report provides a documented incident history and identifies potential control issues.

## 7.2 What the Evidence Does Not Support

The report alone does not independently establish:

- Whether all reported timestamps are accurate.
- Whether every required escalation occurred.
- Whether response activities complied with approved procedures.
- Whether the reported root cause was independently validated.
- Whether the configuration change was authorized through another documented channel.
- Whether the postmortem was completed after May 18, 2026.
- Whether corrective actions were implemented and verified.
- Whether the incident response control operated effectively across the full incident population.

## 7.3 Additional Evidence Requested

### Request 1: Monitoring and Alert Records

Obtain Datadog alert history and PagerDuty acknowledgment records.

**Purpose:**

Corroborate the documented detection and acknowledgment timeline.

### Request 2: Change Management Evidence

Obtain the change ticket for `CHG-1842`, including applicable approvals, testing records, deployment history, and rollback documentation.

**Purpose:**

Validate the reported change management control issues.

### Request 3: Incident Response Procedures

Obtain applicable incident response and escalation procedures in effect at the time of the incident.

**Purpose:**

Determine the expected response activities and compare them against the documented incident timeline.

### Request 4: Postmortem Documentation

Obtain the completed postmortem, if available, along with its completion date.

**Purpose:**

Determine whether the required incident follow-up was completed and whether it met the required deadline.

### Request 5: Corrective Action Tracking

Obtain remediation tickets, responsible owners, due dates, and supporting closure evidence.

**Purpose:**

Evaluate whether corrective actions were implemented and verified.

## 7.4 Evidence Quality Assessment

| Criterion | Assessment |
|---|---|
| Relevance | Relevant to incident response and change management controls. |
| Reliability | Provides an incident record; supporting system records are needed to corroborate key activities. |
| Completeness | Does not include all underlying records, approvals, or completed remediation documentation. |
| Timeliness | Contains incident and follow-up dates; later postmortem completion is not established. |

### Preliminary Conclusion

**Evidence Status: Potential Exceptions Requiring Validation**

The incident report identifies apparent control issues involving change approval, incomplete testing evidence, and delayed incident follow-up.

These observations warrant additional investigation.

A final audit finding should be supported by corroborating evidence, applicable control criteria, and verification of the relevant facts.

---

# 8. Cross-Evidence Comparison

| Evaluation Area | E02: Access Review | E11: AWS Logging | E09: Incident Response |
|---|---|---|---|
| Evidence Type | Management certification | Configuration export | Incident report |
| Primary Control Area | Access management | Logging and retention | Incident response |
| Main Strength | Documents management certification | Records technical configuration values | Documents incident timeline and reported issues |
| Main Limitation | Does not independently prove review execution | Does not establish full coverage or continuous operation | Does not include all corroborating records |
| Additional Evidence | Review records, user listings, removal logs | AWS settings, account scope, retention records | Alerts, change ticket, procedures, postmortem |
| Preliminary Status | Additional evidence required | Additional evidence required | Potential exceptions requiring validation |

---

# 9. Risk Statements Associated With the Evidence

Risk statements are written using the structure:

**Because of [Cause], [Risk Event] may occur, resulting in [Business Impact].**

The following statements describe potential risks based on the control areas examined. They are not assertions that every underlying control deficiency has been confirmed.

## Risk 1: Inappropriate User Access

**Cause:**
Incomplete or ineffective user access review activities.

**Risk Event:**
Users may retain excessive or unauthorized access permissions.

**Business Impact:**
Sensitive data exposure, unauthorized activity, and potential compliance violations.

### Risk Statement

> Because user access reviews may be incomplete or ineffective, inappropriate system permissions may remain undetected, resulting in unauthorized access, sensitive data exposure, or potential regulatory compliance violations.

## Risk 2: Inadequate Log Retention

**Cause:**
Logging coverage or retention configurations may not meet organizational requirements.

**Risk Event:**
Required security events may not be available for investigation.

**Business Impact:**
Reduced incident investigation capabilities, compliance exposure, and increased business risk.

### Risk Statement

> Because logging and retention controls may not cover all required systems or meet established retention requirements, critical security event records may be unavailable when needed, resulting in delayed investigations, reduced forensic capabilities, and potential compliance violations.

## Risk 3: Ineffective Change Management

**Cause:**
Production changes may be deployed without sufficient approval or testing.

**Risk Event:**
Unauthorized or improperly tested changes may disrupt production services.

**Business Impact:**
Service outages, financial losses, and customer dissatisfaction.

### Risk Statement

> Because production changes may be implemented without documented approval or sufficient testing, defective configurations may be introduced into critical systems, resulting in service disruptions, operational losses, and negative customer impacts.

## Risk 4: Incomplete Incident Follow-Up

**Cause:**
Required post-incident activities may not be completed within established deadlines.

**Risk Event:**
Underlying weaknesses may remain unresolved.

**Business Impact:**
Recurring incidents, extended disruptions, and increased recovery costs.

### Risk Statement

> Because post-incident reviews and corrective actions may not be completed within required timeframes, previously identified control weaknesses may remain unresolved, resulting in recurring service disruptions and increased operational risk.

---

# 10. Preliminary Audit Observations

## Observation 1: Access Review Verification Gap

**Evidence:** E02

**Condition:**
The available evidence consists of a management certification without the underlying review records.

**Assessment:**
Evidence is insufficient to independently conclude that the quarterly access review operated effectively.

**Next Step:**
Obtain population, review execution, and access remediation records.

**Classification:**
Evidence insufficiency; no confirmed control deficiency established.

## Observation 2: Logging Control Verification Gap

**Evidence:** E11

**Condition:**
A configuration export records enabled logging and 90-day retention settings, but does not independently establish complete coverage or effective retention throughout the period.

**Assessment:**
Additional evidence is needed to evaluate configuration accuracy, coverage, and operating effectiveness.

**Next Step:**
Compare authoritative configuration and historical retention evidence against applicable requirements.

**Classification:**
Evidence insufficiency; compliance status undetermined.

## Observation 3: Potential Change Management Exception

**Evidence:** E09

**Condition:**
The incident report states that a production change lacked documented approval and had incomplete testing evidence.

**Assessment:**
A potential change management deficiency requires corroboration.

**Next Step:**
Examine the change record, approvals, testing evidence, and applicable procedures.

**Classification:**
Potential control exception requiring validation.

## Observation 4: Potential Incident Follow-Up Exception

**Evidence:** E09

**Condition:**
A required incident postmortem was recorded as incomplete as of May 18, 2026.

**Assessment:**
The report indicates a potential failure to complete required follow-up on time.

**Next Step:**
Verify the applicable deadline and actual completion status using postmortem and tracking records.

**Classification:**
Potential control exception requiring validation.

---

# 11. Recommended Remediation Considerations

These recommendations are preliminary and should be refined after control testing confirms actual weaknesses.

| Control Area | Potential Recommendation |
|---|---|
| Access Management | Maintain complete access review records and evidence of remediation. |
| Logging | Verify complete system coverage and align retention settings with approved requirements. |
| Change Management | Require documented approvals and appropriate testing before production deployment. |
| Incident Response | Track required postmortems and corrective actions through documented closure. |
| Audit Readiness | Maintain reliable, complete, and time-relevant supporting evidence. |

---

# 12. Lessons Learned

This project reinforced several important GRC and IT audit principles.

### 1. Management Assertions Are Not the Same as Independent Verification

A certification email may establish that management represented a control as completed.

It does not necessarily demonstrate that the underlying activity occurred as required.

### 2. Control Configuration Is Not the Same as Operating Effectiveness

A system may be configured correctly at a given point in time without proving that the control operated effectively throughout the entire audit period.

### 3. Evidence Must Match the Control Objective

Evidence supporting logging configuration does not necessarily support log review.

Evidence supporting account creation does not necessarily support periodic access certification.

### 4. Population Completeness Matters

An auditor must determine whether the evidence covers all relevant systems, users, records, or transactions.

### 5. Audit Findings Require Corroboration

A reported weakness should be evaluated against control criteria and supported by sufficient and appropriate evidence before being classified as a confirmed deficiency.

### 6. Business Risk Must Be Connected to Control Weaknesses

Audit observations become more meaningful when their potential effects on operations, information security, compliance, and business continuity are clearly explained.

---

# 13. Project Limitations

This project is a simulated GRC and IT audit exercise.

- The organization and evidence scenarios are hypothetical.
- No direct access to the underlying organizational systems was available.
- No independent system validation was performed.
- No complete audit population was established.
- No formal sampling methodology was executed.
- Preliminary observations should not be interpreted as confirmed audit findings.
- No professional assurance opinion is expressed.

The project demonstrates evidence evaluation methodology, professional skepticism, risk analysis, and preliminary audit documentation.

---

# 14. Conclusion

The Risk-Control-Evidence Model demonstrates how cybersecurity and IT auditing activities connect organizational risks, internal controls, and supporting evidence.

Through three simulated evidence assessments, the project examines:

- Quarterly user access certification.
- AWS CloudTrail logging and retention.
- Incident response and change management.

The central lesson is that the existence of documentation does not automatically establish effective control operation.

Auditors must evaluate whether evidence is relevant, reliable, complete, and timely before drawing conclusions.

**Risk identifies what could go wrong.**

**Controls are designed to reduce that risk.**

**Evidence helps demonstrate whether the controls operated as intended.**

**Testing determines whether the available evidence supports the control objective.**
