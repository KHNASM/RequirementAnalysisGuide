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

Stakeholder A: "System must require 2FA for all actions"
Stakeholder B: "System must allow quick one-click purchases"


### Step 2: Analyze Type

Type: Interest Conflict
Reason: Security vs Usability
Impact: User experience and system security


### Step 3: Generate Solutions

Option 1: Tiered security based on transaction value
Option 2: Remember device for 30 days
Option 3: Biometric authentication for quick access


### Step 4: Evaluate and Select

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


2. User Story Writing

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


3. Conflict Resolution

Question: "How would you resolve conflicting requirements between security and usability?"

Approach:
1. Identify stakeholders
2. Analyze impact
3. Consider compromises
4. Propose solution with rationale


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

Avoid:
- "etc."
- "and/or"
- "as appropriate"
- "if possible"
- "as required"


2. Unmeasurable Terms

Problematic:
- "user-friendly"
- "fast"
- "secure"
- "efficient"
- "flexible"


3. Implementation Details

Wrong: "System shall use MySQL database"
Right: "System shall store customer data persistently"


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


# Requirements Negotiation and Validation Guide

## Part 1: Requirements Negotiation

### Understanding Requirements Conflicts

#### What is Requirements Negotiation?
- Process of resolving conflicts between stakeholder needs
- Aims to achieve agreement among all parties
- Involves stakeholders, engineers, and developers
- Views conflicts as opportunities for improvement

#### Real-World Example

Scenario: School Grade Viewing System
Stakeholder A (Administrator): "Teachers should see all student grades"
Stakeholder B (Privacy Advocate): "Teachers should only see grades for their subjects"

This represents a typical requirements conflict requiring negotiation.


### Conflict Management Process

#### 1. Identifying Conflicts
Conflicts can emerge during various RE activities:
- During elicitation (stakeholders state contradicting requirements)
- During documentation (different sessions yield contradicting requirements)
- During prioritization (stakeholders have different priorities)
- During validation (team members disagree on requirement correctness)

#### 2. Types of Conflicts

1. Data Conflicts
- Caused by: Information gaps or misinterpretation
- Example:

S_A: "Enable students to change lectures"
S_B: "Should it be 'read' instead of 'change'?"
Root cause: Unclear terminology


2. Interest Conflicts
- Caused by: Different stakeholder goals
- Example:

S_A: "Animated product pictures"
S_B: "Simple visualization to minimize costs"
Root cause: Feature vs. Cost optimization


3. Value Conflicts
- Caused by: Different evaluation criteria
- Example:

S_A: "Support OGG format"
S_B: "OGG format unnecessary"
Root cause: Different priority assessment


4. Overlap Conflicts
- Caused by: Duplicate requirements in different locations
- Solution: Consolidate and maintain single source of truth

### Conflict Resolution Strategies

#### 1. Negotiation Approach
- Characteristics:
  - Selects between existing solutions
  - Creates win-win situations
  - Involves exchange of arguments
- Pros: Creates mutual satisfaction
- Cons: Time-consuming

#### 2. Creative Solution
- Characteristics:
  - Discards original viewpoints
  - Creates entirely new solution
  - Involves innovative thinking
- Pros: All parties win
- Cons: 
  - Time-consuming
  - May affect other requirements

#### 3. Authority Decision
- Characteristics:
  - Higher authority decides
  - Quick resolution
  - Can include voting
- Pros: Fast resolution
- Cons: May demotivate ignored parties

### Documentation of Resolutions

#### Requirements Conflict Table
```
| Requirement | Conflict With | Solution | Rationale |
|-------------|---------------|----------|-----------|
| R1          | R2(D), RX(V)  | ...      | ...       |
| R2          | R1(D)         | ...      | ...       |
| RX          | R1(V)         | ...      | ...       |
```

#### Documentation Elements
1. Solution Documentation

Example: "Requirement_X of Stakeholder_A removed due to conflict with Requirement_Y"


2. Rationale Documentation

Example: "Requirement_X not vital for functionality, Requirement_Y essential"


3. Revision Documentation
- Update existing requirements
- Update dependent requirements
- Maintain traceability

## Part 2: Requirements Validation

### Validation Framework

#### What to Validate?
1. Content
- Completeness of requirements
- Accuracy of documentation
- Proper linking between requirements

2. Documentation
- Adherence to specification format
- Quality criteria compliance
- User story formatting (if applicable)

3. Agreement
- Stakeholder consensus
- Conflict resolution status
- Final approvals

### Validation Techniques

#### 1. Inspections (Primary Technique)
- Systematic process
- Group-based analysis
- Action-oriented outcomes

Process:

1. Prepare materials
2. Individual review
3. Group discussion
4. Document issues
5. Agree on actions
6. Follow up


#### 2. Commenting
- Peer review approach
- Expert opinion gathering
- Quality assessment

Process:
1. Share specifications
2. Collect expert feedback
3. Mark issues
4. Provide explanations
5. Return for revision


#### 3. Walkthroughs
- Lightweight inspection
- Informal process
- Quick feedback loop

### Assistance Techniques

#### 1. Checklists
Example Validation Checklist:

□ Requirements are complete
□ Format is correct
□ No ambiguity exists
□ Conflicts are resolved
□ Traceability is maintained


#### 2. Perspective-based Reading
Views to Consider:
1. User Perspective

□ Functionality is clear
□ Quality requirements are specified
□ User needs are met


2. Architect Perspective

□ Technical feasibility
□ System constraints
□ Integration requirements


3. Tester Perspective

□ Testability of requirements
□ Clear acceptance criteria
□ Measurable outcomes


#### 3. Prototyping
Benefits:
- Early user feedback
- Risk reduction
- Requirement clarification

### Ethical Considerations

#### Key Principles
1. Regulatory Compliance
- Organizational rules
- Industry standards
- Legal requirements

2. Impact Assessment
- Stakeholder effects
- Public perception
- Professional standards

#### Ethical Decision Framework

1. Identify affected parties
2. Assess potential impacts
3. Consider public perception
4. Evaluate professional standards
5. Document decisions and rationale

# Requirements Management & Agile Development Study Guide

## Table of Contents

- [1. Requirements Management](#1-requirements-management)
- [2. Traceability](#2-traceability)
- [3. Prioritization](#3-prioritization)
- [4. Scrum Framework](#4-scrum-framework)
- [5. SAFe Framework](#5-safe-framework)

## 1. Requirements Management

### Change Management Process
Requirements change management ensures changes are properly evaluated and implemented. The process includes:

1. **Classification** - Categorize incoming changes as:
   - Exceptional ("hot fixes")
   - Corrective (fixing errors)
   - Adaptive (evolution)

2. **Impact Analysis**
   - Estimate implementation effort
   - Identify affected requirements
   - Assess impact on architecture/design

3. **Evaluation & Decision**
   - Analyze costs vs benefits
   - Accept or reject change

4. **Prioritization**
   - If accepted, prioritize against other requests
   - Schedule for implementation

5. **Implementation & Monitoring** 
   - Track integration progress
   - Keep stakeholders informed

### Common Change Triggers
- Evolution of stakeholder needs
- New technologies emerging
- Changes in laws/standards  
- Updated organizational policies
- Changes in system usage patterns

## 2. Traceability

### Types of Traceability

1. **Pre-traceability**
   - Links to predecessor artifacts
   - Source documentation
   - Original requirements

2. **Post-traceability** 
   - Links to successor artifacts
   - Design elements
   - Implementation code
   - Test cases

3. **Inter-requirements**
   - Links between requirements
   - Dependencies
   - Relationships
   - Conflicts

### Benefits
- Impact analysis capability
- Requirements validation
- Change management support
- Project tracking
- Compliance verification

## 3. Prioritization 

### Key Criteria
- Business value/importance
- Implementation cost
- Development duration  
- Technical risk
- Dependencies
- User value
- Volatility

### Methods

#### MoSCoW Method
Categorizes requirements as:
- **Must Have**: Essential features
- **Should Have**: Important but not vital
- **Could Have**: Desired but not critical  
- **Won't Have**: Not in current scope

#### Cost of Delay
- Quantifies delay impact
- Prioritizes high-value, low-effort items
- Uses WSJF (Weighted Shortest Job First)

## 4. Scrum Framework

### Core Elements

1. **Roles**
   - Product Owner
   - Scrum Master  
   - Development Team

2. **Artifacts**
   - Product Backlog
   - Sprint Backlog
   - Increment

3. **Events** 
   - Sprint Planning
   - Daily Scrum
   - Sprint Review
   - Sprint Retrospective

### Product Backlog
- Prioritized feature list
- Continuously refined
- More detail at top
- Less detail at bottom
- Dynamic and evolving

## 5. SAFe Framework

### Overview
- Enterprise-scale agile framework
- Coordinates multiple teams
- Integrates lean principles
- Supports large systems

### Requirements Model
Hierarchical structure:

1. **Epics**
   - Large initiatives
   - Business/architecural changes
   
2. **Capabilities**
   - Groups of related features
   - Major system functions

3. **Features**
   - User-valuable functionality
   - Deliverable increments

4. **Stories**
   - Implementation units
   - Sprint-level work items

5. **NFRs**
   - Performance requirements
   - Quality attributes
   - System constraints

### Best Practices
- Use clear definitions
- Maintain traceability
- Regular backlog refinement
- Continuous prioritization
- Stakeholder collaboration

---

# Goal-Oriented Requirements Engineering (GORE) Study Guide

## Table of Contents
- [1. Introduction to GORE](#1-introduction-to-gore)
- [2. Motivation for GORE](#2-motivation-for-gore)
- [3. Goals](#3-goals)
- [4. Goal Modeling](#4-goal-modeling)
- [5. Goals and Requirements](#5-goals-and-requirements)

## 1. Introduction to GORE

Goal-Oriented Requirements Engineering focuses on using goals to drive requirements elicitation, documentation, negotiation, validation, and management.

### Core Concept
Goals capture various objectives that:
- An organization wants to achieve
- A system under consideration should fulfill
- Express different levels of abstraction

## 2. Motivation for GORE

### Key Benefits
1. **Requirements Elicitation**
   - Better understanding of the system
   - Goals provide context and rationale

2. **Requirements Justification**
   - Goals document why requirements exist
   - Links high-level objectives to system requirements

3. **Stability Analysis**
   - Goals tend to be more stable than requirements
   - Higher-level goals are most stable
   - Requirements represent specific ways to achieve goals

4. **Alternative Analysis**
   - Goals help identify different solutions
   - Support systematic evaluation of alternatives

5. **Conflict Management**
   - Goals help detect conflicts between requirements
   - Provide framework for conflict resolution

6. **Completeness Assessment**
   - Goals provide criteria for specification completeness
   - Requirements are complete if they achieve all goals

## 3. Goals

### Goal Types

1. **By Abstraction Level**
   - High-level strategic goals
   - Mid-level tactical goals
   - Low-level operational goals

2. **By Nature (i* approach)**
   - Hard goals (clear-cut satisfaction)
   - Soft goals (satisfaction cannot be clearly determined)

### Goal Documentation

Best Practices:
1. Start with "the goal is..."
2. Express as: desired condition + resource + features
3. Follow SMART criteria:
   - Specific
   - Measurable
   - Accepted
   - Realistic
   - Time-framed

## 4. Goal Modeling

### Goal Decomposition Types

1. **AND Decomposition**
   - All sub-goals must be satisfied
   - Sufficient for parent goal satisfaction

2. **OR Decomposition**
   - One sub-goal satisfaction is sufficient
   - Represents alternatives

3. **AND/OR Decomposition**
   - Combination of both
   - Used for high/middle level goals
   - Avoid in detailed RE activities

### Dependencies

1. **Supports/Motivates**
   - Shows positive influence
   - Vertical relationship for refinement

2. **Hinders**
   - Shows negative influence
   - Opposite of supports

3. **Conflicts**
   - Shows mutual exclusion
   - Used for conflicting goals

## 5. Goals and Requirements

### Hierarchy Levels

1. **Strategic Level**
   - Company vision
   - High-level business goals
   - 3-5 decomposition levels

2. **Operational Level**
   - Unit-specific goals
   - Business function goals
   - 3-6 decomposition levels

3. **Detailed Level**
   - Project/system specific goals
   - Information system requirements
   - 3-5 decomposition levels

### GORE in Agile RE

Best Practices:
1. Focus on operational/detailed goals
2. Aim for leaf goals that specify system needs
3. Transform leaf goals into user stories:
   - One goal → one story
   - One goal → multiple stories
   - One goal → epic (needs breakdown)
4. Examine all leaf goals for potential stories
5. Clarify goals requiring only manual activities


