# Comprehensive Requirements Engineering Study Guide

## Introduction to Requirements Engineering

### What is Requirements Engineering?
Requirements Engineering (RE) is a systematic approach to:
- Collecting, understanding, and documenting stakeholder needs
- Analyzing and validating these needs
- Converting them into precise system specifications
- Managing changes to these requirements throughout the project lifecycle

Think of RE as being like an architect working with clients to design a house:
- You need to understand what the clients want
- Translate their wishes into specific plans
- Ensure all building codes (constraints) are met
- Document everything clearly for the builders

### Why is RE Important?
Studies show that poor requirements are the leading cause of project failures:
- 60-80% of project failures are due to poor requirements
- Fixing a requirement error after delivery costs 100x more than fixing it during RE
- Nearly 50% of budget overruns are related to requirement issues

## Detailed Requirements Types

### 1. Functional Requirements
Definition: What the system should DO.

Examples:
```
Good Example:
"The system shall allow users to reset their password by:
- Clicking 'Forgot Password' link
- Entering their registered email
- Receiving a reset link via email
- Creating a new password that meets security criteria"

Bad Example:
"The system should have password reset functionality"
```

### 2. Quality Requirements (Non-Functional)
Definition: HOW WELL the system should perform its functions.

Categories and Examples:

a) Performance
```
Good: "The system shall load user profiles within 2 seconds when accessed from a 4G network"
Bad: "The system should be fast"
```

b) Security
```
Good: "The system shall lock user accounts after 3 failed login attempts within 15 minutes"
Bad: "The system should be secure"
```

c) Usability
```
Good: "First-time users shall be able to complete user registration within 3 minutes"
Bad: "The system should be user-friendly"
```

d) Reliability
```
Good: "The system shall maintain 99.9% uptime during business hours (9 AM - 5 PM)"
Bad: "The system should always work"
```

### 3. Constraints
Definition: Limitations and conditions that must be respected.

Types:
1. Technical Constraints
```
"The system must:
- Be developed using Java 11 or higher
- Run on AWS cloud infrastructure
- Support Chrome 80+ and Firefox 75+"
```

2. Business Constraints
```
"The system must:
- Comply with GDPR regulations
- Be delivered within 6 months
- Cost less than $100,000 to develop"
```

## User Stories in Detail

### Anatomy of a User Story
```
As a [specific user role]
I want to [concrete action/feature]
So that [tangible benefit/value]
```

Extended Example:
```
Title: Online Course Enrollment
As a university student
I want to enroll in available courses for next semester
So that I can secure my spot in required classes

Acceptance Criteria:
1. Can view list of available courses
2. Can see prerequisites for each course
3. Can view course schedule conflicts
4. Receive confirmation email after enrollment
5. Can view enrolled courses in student dashboard

Technical Notes:
- Must check prerequisite completion
- Must verify student's academic standing
- Must check for schedule conflicts
- Must update course capacity
```

### Common User Story Mistakes and Fixes

1. Too Large (Epic)
```
Bad:
"As a user, I want a complete account management system"

Better (Split into):
- "As a user, I want to register for an account"
- "As a user, I want to update my profile information"
- "As a user, I want to change my password"
- "As a user, I want to delete my account"
```

2. Too Technical
```
Bad:
"As a user, I want to use SHA-256 encryption for my password"

Better:
"As a user, I want my password to be securely stored"
```

3. Too Vague
```
Bad:
"As a user, I want the system to be nice"

Better:
"As a user, I want color-coded error messages so that I can easily understand what went wrong"
```

## Requirements Validation Techniques

### 1. Reviews and Inspections
Structured process:

1. Planning
- Select participants
- Schedule meeting
- Distribute materials

2. Preparation
- Individual review
- Mark issues
- Prepare questions

3. Meeting
- Present findings
- Discuss issues
- Document decisions

4. Follow-up
- Update requirements
- Verify changes
- Document results

### 2. Prototyping
Types:

1. Throwaway Prototypes
- Quick mockups
- Test concepts
- Discard after feedback

2. Evolutionary Prototypes
- Working software
- Incrementally improved
- Becomes final system

### Validation Checklist
```
For each requirement, verify:

1. Completeness
□ All necessary information included
□ No missing conditions or scenarios
□ Clear success criteria

2. Consistency
□ No conflicts with other requirements
□ Terminology is consistent
□ No contradicting conditions

3. Feasibility
□ Technically possible
□ Within budget constraints
□ Achievable timeline

4. Testability
□ Can be verified
□ Has measurable criteria
□ Clear pass/fail conditions

5. Traceability
□ Source is documented
□ Links to other requirements clear
□ Impact analysis possible
```

## Conflict Resolution Framework

### Step 1: Identify Conflict
Example:
```
Stakeholder A: "System must require 2FA for all actions"
Stakeholder B: "System must allow quick one-click purchases"
```

### Step 2: Analyze Type
```
Type: Interest Conflict
Reason: Security vs Usability
Impact: User experience and system security
```

### Step 3: Generate Solutions
```
Option 1: Tiered security based on transaction value
Option 2: Remember device for 30 days
Option 3: Biometric authentication for quick access
```

### Step 4: Evaluate and Select
```
Selected: Option 1
Rationale: 
- Low-value transactions: One-click
- High-value transactions: 2FA required
- Balances both requirements

## Exam Tips and Tricks

### Common Question Types

1. Requirement Analysis
```
Question: "Identify issues in this requirement:
'The system should be fast and user-friendly'"

Answer approach:
1. Identify ambiguous terms ("fast", "user-friendly")
2. Note missing metrics
3. Suggest improvements:
   "The system shall respond to user input within 2 seconds"
   "Users shall complete common tasks in under 3 clicks"
```

2. User Story Writing
```
Question: "Write a user story for a password reset feature"

Good Answer:
"As a registered user
I want to reset my forgotten password
So that I can regain access to my account

Acceptance Criteria:
1. Reset link expires after 24 hours
2. New password must meet security requirements
3. User receives confirmation email
4. Previous password cannot be reused"
```

3. Conflict Resolution
```
Question: "How would you resolve conflicting requirements between security and usability?"

Approach:
1. Identify stakeholders
2. Analyze impact
3. Consider compromises
4. Propose solution with rationale
```

### Key Terms to Master

1. Requirements Engineering
- Elicitation: Gathering requirements
- Analysis: Understanding and organizing
- Specification: Documenting
- Validation: Checking correctness
- Management: Handling changes

2. Quality Attributes
- Performance: Speed, efficiency
- Security: Protection, access control
- Reliability: Consistency, availability
- Usability: Ease of use, learning curve
- Maintainability: Ease of changes

3. Documentation Elements
- User Stories
- Use Cases
- Requirements Specification
- Traceability Matrix
- Change Requests

### Red Flags in Requirements

1. Ambiguous Language
```
Avoid:
- "etc."
- "and/or"
- "as appropriate"
- "if possible"
- "as required"
```

2. Unmeasurable Terms
```
Problematic:
- "user-friendly"
- "fast"
- "secure"
- "efficient"
- "flexible"
```

3. Implementation Details
```
Wrong: "System shall use MySQL database"
Right: "System shall store customer data persistently"
```

### Final Checklist for Exam Preparation

1. Core Concepts
□ Define all types of requirements
□ Understand RE process steps
□ Know validation techniques
□ Master conflict resolution approaches

2. Practical Skills
□ Write clear requirements
□ Create user stories
□ Identify requirement problems
□ Resolve conflicts
□ Validate requirements

3. Documentation
□ Know different formats
□ Understand when to use each
□ Recognize good vs bad examples
□ Apply proper structure

4. Process Knowledge
□ Requirements lifecycle
□ Change management
□ Stakeholder management
□ Quality assurance

Remember:
- Always think from stakeholder perspective
- Focus on WHAT, not HOW
- Clarity beats brevity
- Everything must be testable
- Requirements evolve over time
