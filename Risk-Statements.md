# GRC Fundamentals: Writing Effective Risk Statements

## Lesson Overview

Risk statements are an important part of Governance, Risk, and Compliance (GRC), IT auditing, and cybersecurity risk management.

A risk statement describes a potential event that could negatively affect an organization's operations, information security, finances, or regulatory compliance.

The purpose of a risk statement is to communicate what could go wrong, why it could happen, and how it could affect the organization.

## 1. Understanding Risk Statements

An effective risk statement answers three questions:

1. **Cause:** What weakness or condition creates the risk?
2. **Risk Event:** What could happen because of this weakness?
3. **Business Impact:** What would the consequences be for the organization?

### Risk Statement Formula

**Because of [Cause], [Risk Event] may occur, resulting in [Business Impact].**

### Example

**Weak Risk Statement:**

> Access risk exists.

This statement is too vague. It does not explain the cause, risk event, or potential business impact.

**Strong Risk Statement:**

> Because terminated employee accounts are not consistently disabled in a timely manner, former employees may retain unauthorized access to company systems, resulting in potential exposure of sensitive information, fraudulent activity, or regulatory compliance violations.

This statement identifies the underlying weakness, explains what could happen, and describes the potential consequences.

---

## 2. The Three Components of a Risk Statement

### A. Cause: Why Could the Risk Occur?

The cause identifies a weakness, vulnerability, or condition that makes a risk event possible.

Common causes include:

- Inadequate access management procedures
- Missing multifactor authentication (MFA)
- Delayed security patching
- Weak password policies
- Insufficient employee security training
- Inadequate monitoring of privileged accounts
- Ineffective change management procedures
- Failure to conduct periodic access reviews

**Example:**

> Because quarterly user access reviews are not consistently performed...

This identifies a weakness in the organization's access management process.

### B. Risk Event: What Could Go Wrong?

The risk event describes the potential security, operational, or compliance issue that may occur.

Examples include:

- Unauthorized access to sensitive systems
- Exposure of confidential customer information
- Fraudulent financial transactions
- Compromise of privileged accounts
- Loss of critical business data
- Disruption of essential business services
- Unauthorized modification of financial records

**Example:**

> ...employees may retain inappropriate access to sensitive systems...

This explains what could happen because of the identified weakness.

### C. Business Impact: Why Does It Matter?

The business impact describes the consequences if the risk event occurs.

Potential impacts include:

- Financial losses
- Regulatory fines or penalties
- Reputational damage
- Business interruptions
- Legal liabilities
- Loss of customer trust
- Exposure of confidential information
- Increased recovery and remediation costs

**Example:**

> ...resulting in potential data exposure, financial losses, or regulatory compliance violations.

This explains why management should be concerned about the risk.

---

## 3. Control Deficiencies vs. Risk Statements

One of the most important concepts in IT auditing is understanding the difference between a control deficiency and a risk.

### Control Deficiency

A control deficiency describes a missing, ineffective, or improperly implemented control.

**Example:**

> Quarterly user access reviews are not performed.

This identifies a control problem but does not explain the associated business risk.

### Risk Statement

A risk statement identifies what could happen because of the control deficiency.

**Example:**

> Because quarterly user access reviews are not consistently performed, employees may retain excessive or inappropriate system permissions, resulting in unauthorized access to sensitive information or potential fraudulent activity.

### Comparison Table

| Control Deficiency | Associated Risk |
|---|---|
| MFA is not enforced | Unauthorized individuals may compromise user accounts. |
| Backups are not tested | Critical business data may not be recoverable following a system failure. |
| User access reviews are not performed | Excessive or inappropriate access may remain undetected. |
| Security patches are delayed | Attackers may exploit known vulnerabilities. |
| Privileged accounts are not monitored | Unauthorized administrative activity may go undetected. |
| Changes are deployed without approval | Unauthorized or defective system changes may disrupt operations. |

**Key Concept:**
