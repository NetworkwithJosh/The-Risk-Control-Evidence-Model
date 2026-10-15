
# Risk-Control-Evidence Model
## Northstar Practice: Control Design Assessment

### Project Overview

This project demonstrates how cybersecurity and IT controls are evaluated for design effectiveness.

The assessment focuses on five hypothetical organizational controls involving:

- Identity and Access Management (IAM)
- Employee Termination and Deprovisioning
- Change Management
- Incident Response
- Security Logging and Retention

The objective is to determine whether each control is sufficiently defined to address its associated risk and whether an auditor could understand how the control should operate.

This project uses a simulated Northstar control inventory.

---

# 1. Understanding Control Design

A control is an action, procedure, or technical safeguard implemented to manage risk and help an organization achieve its objectives.

An effective control description should answer seven questions:

1. **Who:** Who owns and performs the control?
2. **What:** What activity is performed?
3. **When:** How frequently is it performed?
4. **Population:** What systems, users, or transactions are covered?
5. **Criteria:** What requirements are used?
6. **Evidence:** What documentation demonstrates performance?
7. **Exceptions:** What happens when an issue is identified?

## Control Statement Structure

A useful structure is:

> [Control owner or operator] performs [control activity] at [frequency] for [population], using [defined criteria]. Evidence of the activity is retained, and identified exceptions are investigated, documented, and remediated.

## Understanding Control Classifications

### Preventive Controls

Designed to prevent an unwanted event before it occurs.

Examples:

- Multifactor authentication
- Change approval requirements
- Access restrictions

### Detective Controls

Designed to identify problems or unauthorized activity after they occur.

Examples:

- User access reviews
- Security monitoring
- Reconciliation procedures

### Corrective Controls

Designed to resolve identified problems or restore normal operations.

Examples:

- Removing inappropriate permissions
- Restoring data from backups
- Correcting configuration errors

### Manual Controls

Performed primarily by personnel.

Example: A manager reviewing and approving user access.

### Automated Controls

Performed primarily through configured technology.

Example: An identity platform enforcing MFA.

A control may combine manual and automated activities.

---

# 2. Control Design Assessment Summary

The following five controls were selected from the Northstar control inventory.

| Control ID | Control Name | Owner | Frequency | Method | Type |
|---|---|---|---|---|---|
| AC-01 | Quarterly User Access Reviews | Marcus Lee | Quarterly | Manual | Preventive/Detective |
| AC-02 | Timely Termination Deprovisioning | Hannah Brooks | Per Event | Manual/Automated | Preventive |
| CM-01 | Production Change Approval | Priya Shah | Per Change | Manual/Automated | Preventive |
| IR-02 | Incident Logging and Postmortems | Marcus Lee | Per Incident | Manual | Detective/Corrective |
| LOG-01 | Centralized Logging and Retention | Priya Shah | Continuous | Automated | Detective |

**Assessment approach:**

Each control is evaluated for:

- Control objective
- Control owner
- Frequency
- Control classification
- Expected evidence
- Design completeness
- Potential improvement opportunities

The identified design gaps represent areas requiring clarification, not automatically confirmed control failures.

---

# 3. Control AC-01: Quarterly User Access Reviews

## Original Control Description

> User and privileged access to in-scope systems is reviewed quarterly by designated business and system owners. Inappropriate access is removed and tracked to closure.

## Control Attributes

| Attribute | Description |
|---|---|
| Control ID | AC-01 |
| Control Owner | Marcus Lee |
| Frequency | Quarterly |
| Method | Manual |
| Type | Preventive/Detective |
| Systems | Okta, AWS, GitHub, Snowflake, Salesforce, Zendesk |
| Related Risks | R-01, R-10 |
| SOC 2 Categories | Security, Confidentiality |

## Control Objective

Ensure that user and privileged access to organizational systems remains appropriate based on employee responsibilities and authorized business needs.

The control is intended to identify unnecessary, excessive, or unauthorized access.

## Expected Evidence

- System-generated access review exports
- Reviewer certifications
- Access removal tickets
- Exception tracking records

## Control Design Evaluation

### Strengths

The control identifies:

- A quarterly review frequency.
- Responsibility assigned to business and system owners.
- User and privileged access as the population.
- A requirement to remove inappropriate access.
- Tracking of remediation activities.

### Potential Design Gaps

The description does not clearly specify:

1. How the organization verifies that the access population is complete.
2. What criteria reviewers use to determine appropriate access.
3. Whether review completion deadlines are established.
4. How unresolved exceptions are escalated.
5. How review evidence and remediation records are retained.

## Proposed Design Improvements

The organization should define:

- How access listings are generated and validated.
- How reviewers determine whether access remains appropriate.
- How review decisions are documented.
- How exceptions are tracked and escalated.
- How completed reviews are independently verified, where required.

### Preliminary Assessment

**Design Status: Defined, with clarification opportunities**

The original description includes several important control elements.

Additional procedural detail would make the control more consistently executable and testable.

---

# 4. Control AC-02: Timely Termination Deprovisioning

## Original Control Description

> People Operations notifies IT of terminations, and access to in-scope systems is disabled within 24 hours of the effective termination time.

## Control Attributes

| Attribute | Description |
|---|---|
| Control ID | AC-02 |
| Control Owner | Hannah Brooks |
| Frequency | Per Event |
| Method | Manual/Automated |
| Type | Preventive |
| Systems | Workday, Okta, Downstream Applications |
| Related Risk | R-03 |
| SOC 2 Category | Security |

## Control Objective

Prevent former employees from retaining access to organizational systems after their employment ends.

## Expected Evidence

- Employee termination reports
- Okta deprovisioning logs
- Access removal tickets
- System account status records

## Control Design Evaluation

### Strengths

The control establishes:

- Responsibility for termination notification.
- The requirement to disable access.
- A measurable 24-hour deadline.
- A defined triggering event.
- General system coverage.

### Potential Design Gaps

The description does not clearly establish:

1. How IT receives termination notifications.
2. Whether all downstream accounts are included.
3. How failed automated deprovisioning activities are detected.
4. Who verifies access removal.
5. How exceptions are documented and escalated.

## Proposed Design Improvements

- Document the HR-to-IT termination workflow.
- Establish a complete in-scope application inventory.
- Monitor failed account deactivation activities.
- Maintain timestamps for termination and access removal.
- Define procedures for overdue or incomplete deprovisioning.

### Preliminary Assessment

**Design Status: Defined, with operational clarification needed**

The original control contains a measurable requirement.

Its effectiveness depends on complete notification and deprovisioning processes.

---

# 5. Control CM-01: Production Change Approval

## Original Control Description

> Production changes require documented testing, peer review, and approval before deployment. Emergency changes are reviewed within five business days.

## Control Attributes

| Attribute | Description |
|---|---|
| Control ID | CM-01 |
| Control Owner | Priya Shah |
| Frequency | Per Change |
| Method | Manual/Automated |
| Type | Preventive |
| Systems | GitHub, Jira, AWS |
| Related Risk | R-02 |
| SOC 2 Categories | Security, Availability |

## Control Objective

Ensure that production changes are appropriately tested, reviewed, and authorized before implementation.

The control helps reduce the risk of unauthorized changes, security weaknesses, and operational disruptions.

## Expected Evidence

- Jira change tickets
- Pull requests
- Peer review records
- Approval documentation
- Testing results
- Deployment records

## Control Design Evaluation

### Strengths

The control identifies:

- Required testing activities.
- Peer review expectations.
- Approval before production deployment.
- A review deadline for emergency changes.
- Change management systems.

### Potential Design Gaps

The description does not specify:

1. Which roles are authorized to approve changes.
2. Whether the implementer may approve their own changes.
3. Minimum testing requirements.
4. How emergency changes are identified and documented.
5. What happens when approval or testing requirements are missing.
6. How exceptions are reported and resolved.

## Proposed Design Improvements

- Establish authorized change approver roles.
- Define minimum testing criteria based on change risk.
- Require traceable approval records.
- Document emergency change classification.
- Monitor overdue emergency reviews.
- Establish escalation procedures for unauthorized changes.

### Preliminary Assessment

**Design Status: Defined, with approval and exception-handling gaps**

The control contains clear preventive requirements.

Additional design detail would strengthen consistency and accountability.

---

# 6. Control IR-02: Incident Logging and Postmortems

## Original Control Description

> Security incidents are logged, classified, escalated, and closed with postmortems for Severity 1 and 2 events within ten business days.

## Control Attributes

| Attribute | Description |
|---|---|
| Control ID | IR-02 |
| Control Owner | Marcus Lee |
| Frequency | Per Incident |
| Method | Manual |
| Type | Detective/Corrective |
| Systems | PagerDuty, Jira |
| Related Risk | R-06 |
| SOC 2 Categories | Security, Availability |

## Control Objective

Ensure security incidents are formally recorded, classified, escalated, investigated, and followed by appropriate corrective actions.

## Expected Evidence

- Incident tickets
- Incident timelines
- Severity classifications
- Postmortem reports
- Corrective action records

## Control Design Evaluation

### Strengths

The control establishes:

- Incident documentation requirements.
- Classification requirements.
- Escalation expectations.
- Postmortem requirements for Severity 1 and 2 incidents.
- A ten-business-day deadline.

### Potential Design Gaps

The description does not clearly identify:

1. Who assigns severity classifications.
2. What criteria determine incident severity.
3. Who approves incident closure.
4. Whether postmortems require formal review.
5. How corrective actions are assigned.
6. How overdue postmortems are escalated.
7. How remediation completion is verified.

## Proposed Design Improvements

- Define severity classification criteria.
- Assign incident response responsibilities.
- Establish postmortem review and approval requirements.
- Track corrective actions with owners and due dates.
- Escalate overdue follow-up activities.
- Retain documentation supporting incident closure.

### Preliminary Assessment

**Design Status: Defined, with follow-up and accountability gaps**

The control establishes important incident management requirements.

Additional details would strengthen the ability to evaluate consistent execution.

---

# 7. Control LOG-01: Centralized Logging and Retention

## Original Control Description

> Security-relevant logs for in-scope systems are centrally collected and retained for at least 365 days.

## Control Attributes

| Attribute | Description |
|---|---|
| Control ID | LOG-01 |
| Control Owner | Priya Shah |
| Frequency | Continuous |
| Method | Automated |
| Type | Detective |
| Systems | AWS, Datadog, CareBridge Production |
| Related Risks | R-08, R-12 |
| SOC 2 Categories | Security, Availability |

## Control Objective

Ensure security-relevant activity is logged and retained to support monitoring, incident investigation, forensic analysis, and applicable compliance requirements.

## Expected Evidence

- Logging configuration records
- Retention settings
- System-generated configuration exports

## Original Control Design Evaluation

### Strengths

The existing description identifies:

- Centralized security logging.
- Continuous control operation through its metadata.
- A minimum retention requirement of 365 days.
- An accountable control owner.
- Relevant systems and platforms.

### Design Gaps

The original description does not clearly explain:

1. Who performs periodic verification of logging operation.
2. How completeness of log collection is determined.
3. How logging failures are identified.
4. How retention settings are validated.
5. What evidence demonstrates continuous operation.
6. How exceptions are investigated.
7. Who verifies that remediation was completed.

## Proposed Complete Control Statement

The following is a proposed design enhancement, not a representation of an existing verified procedure.

> Under the accountability of Priya Shah, the designated IT or security operations personnel maintain automated, centralized collection of security-relevant logs from in-scope AWS resources, Datadog, and CareBridge Production systems. Logging operates continuously, and retained logs must meet the organization's minimum retention requirement of 365 days.
>
> Designated personnel periodically verify that required systems are included in the logging configuration, that log collection is functioning, and that applicable retention settings meet established requirements. Configuration exports, retention records, and verification results are retained as control evidence.
>
> Identified logging failures, missing sources, or retention exceptions are documented, investigated, assigned to responsible personnel, and tracked through remediation and closure.

### Important Design Consideration

The rewritten statement introduces a periodic verification activity.

The organization would still need to formally define:

- The exact verification frequency.
- The designated control operator.
- The verification procedure.
- Exception escalation timelines.
- Evidence retention requirements.

These details should be confirmed with the control owner before finalizing the design.

---

# 8. LOG-01: Control Element Breakdown

| Required Element | Proposed Control Design |
|---|---|
| Who | Priya Shah is accountable; designated IT/security personnel perform verification. |
| What | Centrally collect and retain security logs and verify logging operation. |
| When | Automated collection operates continuously; verification frequency must be established. |
| Population | In-scope AWS resources, Datadog, and CareBridge Production systems. |
| Criteria | Security-relevant logs must be retained for at least 365 days. |
| Evidence | Configuration exports, retention records, and verification documentation. |
| Exceptions | Logging failures and retention exceptions are investigated and tracked to closure. |

## Why the Rewritten Control Is Stronger

The original statement defines the core control activity and required retention period.

The rewritten version adds clarity regarding:

- Operational responsibility.
- Verification activities.
- Supporting evidence.
- Population coverage.
- Exception handling.
- Remediation tracking.

These additions make the control easier to execute consistently and evaluate during an audit.

---

# 9. Risk-Control-Evidence Connection

## Risk R-08: Insufficient Audit Log Retention

### Cause

Logging coverage or retention practices may not satisfy required organizational standards.

### Risk Event

Security-relevant activity records may be unavailable when needed for investigation or assurance.

### Business Impact

- Delayed incident investigations
- Reduced forensic capabilities
- Potential compliance violations
- Increased operational and security risk

### Risk Statement

> Because security logging and retention controls may not cover all required systems or meet established retention requirements, critical event records may become unavailable, resulting in impaired investigations, reduced forensic capabilities, and potential regulatory or contractual compliance issues.

### Control

**LOG-01: Centralized Logging and Retention**

### Evidence

- Logging configuration exports
- System retention settings
- Log availability records
- Verification records, where required

### Testing Approach

1. Obtain the approved logging and retention requirements.
2. Identify the complete population of in-scope systems.
3. Obtain relevant logging configurations.
4. Compare configured retention periods against requirements.
5. Evaluate whether logging was operating during the review period.
6. Investigate identified exceptions.
7. Document testing results and conclusions.

---

# 10. Connection to Previous Evidence Assessment

## E11: AWS CloudTrail Configuration Export

The earlier evidence assessment identified the following:

| Configuration | Recorded Setting |
|---|---|
| AWS Account | northstar-prod |
| CloudTrail Trail | organization-trail |
| Logging | Enabled |
| S3 Lifecycle Retention | 90 days |
| CloudWatch Retention | 90 days |
| Last Modified | February 12, 2026 |

## Comparison to LOG-01

| Requirement | Documented Configuration |
|---|---|
| Minimum retention | 365 days |
| E11 S3 lifecycle retention | 90 days |
| E11 CloudWatch retention | 90 days |

### Preliminary Observation

The 90-day settings documented in E11 appear inconsistent with LOG-01's stated minimum retention requirement of 365 days.

However, further validation is needed before concluding that the control failed.

An auditor should determine:

- Whether E11 applies to the complete in-scope environment.
- Whether additional archival mechanisms provide longer retention.
- Whether the recorded configuration is accurate.
- Whether the requirement applies to the specific records examined.
- Whether the configuration operated as documented during the audit period.

### Preliminary Status

**Potential Exception: Requires Validation**

The discrepancy warrants further investigation, but it does not independently establish a confirmed compliance violation.

---

# 11. Control Design Findings Summary

| Control | Primary Design Concern | Preliminary Assessment |
|---|---|---|
| AC-01 | Population validation and review criteria | Clarification needed |
| AC-02 | Deprovisioning verification and exceptions | Clarification needed |
| CM-01 | Approval authority and emergency change handling | Clarification needed |
| IR-02 | Postmortem accountability and corrective action closure | Clarification needed |
| LOG-01 | Logging verification and exception management | Rewrite proposed |

The assessments identify documentation and design clarification opportunities.

They do not represent confirmed control failures or completed operating effectiveness testing.

---

# 12. Discussion: Which Control Element Is Most Commonly Missing?

In this simulated assessment, one recurring weakness is insufficient detail about **exception handling and follow-up**.

Several controls describe the primary activity but do not fully explain:

- What happens when the control identifies a problem.
- Who is responsible for resolution.
- How remediation is documented.
- When unresolved issues must be escalated.
- How the organization confirms closure.

Another recurring concern is the lack of clearly defined verification procedures.

A well-written control should describe not only the activity being performed but also how identified failures are managed.

This is an observation from the five selected controls, not a statistical conclusion about all organizations.

---

# 13. Key Lessons Learned

## 1. A Control Description Must Be Testable

A control should provide sufficient information for an auditor to identify the expected activity and determine what evidence is necessary.

## 2. Control Ownership and Operation Are Different

A control owner may be accountable for ensuring a control functions without personally performing every control activity.

## 3. Clear Frequency Matters

Statements such as "regularly" or "periodically" should be supported by a defined schedule or documented procedure.

## 4. Population Completeness Matters

A control cannot be fully evaluated without understanding which systems, users, events, or transactions it is expected to cover.

## 5. Evidence Must Support the Activity

The existence of a policy or configuration does not automatically establish that a control operated effectively.

## 6. Exception Handling Is Essential

Controls should define how problems are identified, investigated, escalated, and resolved.

## 7. Design Effectiveness and Operating Effectiveness Are Different

**Design Effectiveness:**

Would the control, if performed as designed, adequately address the relevant risk?

**Operating Effectiveness:**

Did the control actually operate as required during the period being evaluated?

A well-written control description alone does not establish operating effectiveness.

---

# 14. Recommended Next Steps

Future development of this project could include:

1. Reviewing supporting evidence for the five controls.
2. Building a formal risk-control matrix.
3. Mapping controls to SOC 2 Trust Services Criteria.
4. Developing control testing procedures.
5. Documenting exception identification and remediation.
6. Evaluating control design and operating effectiveness separately.
7. Creating standardized audit workpapers.
8. Recording validated findings and management responses.

---

# 15. Project Limitations

This project is based on a simulated organizational control inventory.

- Organizational names and scenarios are hypothetical.
- Control design evaluations are preliminary.
- Proposed enhancements are not confirmed organizational procedures.
- Underlying processes have not been independently validated.
- No formal operating effectiveness testing was completed for the five controls.
- Identified gaps should not be interpreted as confirmed audit findings.
- No professional assurance opinion is expressed.

---

# 16. Conclusion

The Northstar Control Design Assessment demonstrates how cybersecurity controls can be evaluated for clarity, completeness, and alignment with organizational risks.

Five controls were reviewed across access management, employee deprovisioning, change management, incident response, and centralized security logging.

LOG-01 was selected for a detailed rewrite to demonstrate how control statements can be strengthened through clearer responsibilities, verification activities, evidence requirements, and exception handling procedures.

### Core Principle

**Risk:** What could go wrong?

**Control:** What action reduces or manages that risk?

**Evidence:** What demonstrates the control activity?

**Testing:** Does the evidence establish that the control was properly designed and operated as required?

A strong control description should allow management, control operators, and auditors to understand what must happen, who is responsible, when it happens, and how completion can be demonstrated.
