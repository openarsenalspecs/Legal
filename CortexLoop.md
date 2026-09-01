# CortexLoop
**Transparent intelligence, enforced by design.**
- HTML Mirror:  [https://roxanneardary.com/cortexloop-specification/](https://roxanneardary.com/cortexloop-specification/)  

---

## Specification

CortexLoop is a modular, open source human-in-the-loop AI orchestration system designed to keep reasoning, recommendations, decisions, and execution transparent, structured, auditable, and under human control.

CortexLoop is not an autonomous agent, autopilot, or self-directed decision system. AI systems may analyze information, generate recommendations, compare alternatives, identify risks, and propose actions, but meaningful decisions remain subject to human authority.

The system follows the principle:

**AI proposes. Human decides. System refines.**

## Core Principles

CortexLoop MUST:

- Preserve human authority over meaningful decisions.
- Clearly distinguish AI recommendations from human decisions.
- Require human authorization for high-impact or irreversible actions.
- Make meaningful system state visible to the human operator.
- Maintain traceable decision and action histories.
- Enforce policies and constraints structurally.
- Preserve decision provenance.
- Support review, rejection, revision, and override.
- Prevent silent autonomous execution.
- Support reconstruction and replay of previous workflows.
- Keep model providers and tools replaceable.
- Give users control over stored context and memory.
- Avoid dependence on hidden autonomous behavior.

---

## Core Modules

### Human Decision Module

The Human Decision Module defines the human as the final authority within the CortexLoop decision process.

Features include:

- Human-in-the-loop decision architecture
- Explicit human authority model
- Human approval checkpoints
- Human override controls
- Decision approval
- Decision rejection
- Decision revision
- Decision redirection
- Decision escalation
- Workflow pause and resume
- Configurable approval requirements
- Decision ownership
- Human decision annotations
- Decision justification
- Separation between AI recommendations and human decisions

The module MUST NOT convert an AI recommendation into a final decision without the required human authorization.

### Reasoning Module

The Reasoning Module provides structured cognitive processing without granting autonomous authority.

Features include:

- Intent interpretation
- Task decomposition
- Structured reasoning
- Multi-step analysis
- Assumption identification
- Constraint identification
- Dependency identification
- Tradeoff analysis
- Alternative generation
- Goal alignment
- Uncertainty detection
- Contradiction detection
- Reasoning prioritization
- Context-aware recommendations
- Recommendation generation

The module produces reasoning outputs and recommendations for evaluation by the human decision layer.

### Multi-Track Reasoning Module

The Multi-Track Reasoning Module allows CortexLoop to generate and compare multiple possible approaches to the same problem.

Features include:

- Optimized approaches
- Conservative approaches
- Minimal approaches
- Experimental approaches
- Alternative architecture paths
- Competing recommendations
- Comparative analysis
- Strength and weakness analysis
- Cost and benefit analysis
- Tradeoff comparison
- Human-selected reasoning paths

The module MUST preserve competing alternatives until the system or human decision process determines that they are no longer relevant.

### Confidence and Risk Module

The Confidence and Risk Module evaluates uncertainty, potential impact, and the need for human attention.

Features include:

- Confidence assessment
- Uncertainty detection
- Risk classification
- Decision-impact assessment
- Reversibility assessment
- Human-attention routing
- High-risk decision escalation
- Confidence explanations
- Risk explanations
- Configurable confidence thresholds
- Configurable risk thresholds
- Context-sensitive review requirements

Confidence and risk values MUST NOT grant the system autonomous authority.

Confidence determines how strongly information should be surfaced for human review. Risk determines the level of review, validation, and authorization required.

### Intent Stabilization Module

The Intent Stabilization Module preserves the user's intended objective throughout an ongoing workflow.

Features include:

- Persistent intent tracking
- Goal tracking
- Scope tracking
- Scope-change detection
- Contradiction detection
- Instruction conflict detection
- Goal drift detection
- Context-shift detection
- Change confirmation
- Original-intent preservation
- Intent history
- Intent comparison

The module MUST identify meaningful changes in intent and provide mechanisms for human confirmation before consequential changes are accepted.

### Policy Module

The Policy Module provides structural enforcement of rules governing CortexLoop behavior.

Features include:

- Rule enforcement
- Policy validation
- Constraint enforcement
- Pre-execution validation
- Pre-output validation
- Policy conflict detection
- Policy priority handling
- Policy versioning
- Policy inheritance
- Human-authorized policy overrides
- Policy audit history
- Project-level policies
- Organization-level policies
- User-level policies

Policies MUST be evaluated before actions or other consequential operations that fall within their scope.

### Constraint Module

The Constraint Module manages persistent requirements governing reasoning, workflows, outputs, and actions.

Features include:

- Persistent constraints
- Behavioral requirements
- Workflow rules
- Formatting requirements
- Project conventions
- Repository requirements
- Compliance requirements
- Naming conventions
- Output requirements
- Constraint priority
- Constraint inheritance
- Constraint expiration
- Constraint revision history
- Human-controlled constraint editing

Constraints MUST remain distinguishable from temporary contextual information.

### Decision Ledger Module

The Decision Ledger Module records the lifecycle of recommendations, decisions, approvals, revisions, and actions.

Features include:

- Immutable decision records
- AI proposal records
- Human decision records
- Alternative-path records
- Approval records
- Rejection records
- Revision records
- Override records
- Policy evaluation records
- Risk assessments
- Confidence assessments
- Timestamped events
- Decision provenance
- Decision relationships
- Decision history
- Exportable audit records

The Decision Ledger MUST preserve sufficient information to establish what was proposed, what was decided, who authorized the decision, and what occurred afterward.

### Provenance Module

The Provenance Module establishes relationships between inputs, context, models, tools, policies, recommendations, decisions, and outputs.

Features include:

- Source tracking
- Input provenance
- Context provenance
- Model provenance
- Tool provenance
- Policy provenance
- Human decision provenance
- Output provenance
- Transformation history
- Source-to-output relationships
- Provenance validation

Provenance records MUST remain associated with the relevant workflow and decision history.

### Replay Module

The Replay Module reconstructs previous workflows and decisions for auditing, analysis, debugging, and evaluation.

Features include:

- Workflow replay
- Decision replay
- State reconstruction
- Historical context reconstruction
- Policy reconstruction
- Decision-path reconstruction
- Output reconstruction
- Debugging replay
- Audit replay
- Workflow-version comparison
- Replay from selected checkpoints

Replay MUST preserve historical conditions sufficiently to distinguish the original workflow from subsequent changes.

### Explanation Module

The Explanation Module provides human-readable explanations of recommendations, decisions, risks, policies, and workflow transitions.

Features include:

- Decision explanations
- Recommendation rationale
- Assumption reporting
- Tradeoff reporting
- Alternative reporting
- Risk explanations
- Confidence explanations
- Policy explanations
- Human-decision annotations
- Decision history visualization
- Explainable workflow transitions

The module focuses on decision transparency and useful explanations rather than exposing private model chain-of-thought.

### Context Graph Module

The Context Graph Module organizes relationships among projects, tasks, decisions, policies, constraints, workflows, and knowledge.

Features include:

- Project relationships
- Repository relationships
- Task relationships
- Decision relationships
- Constraint relationships
- Policy relationships
- Workflow relationships
- Dependency mapping
- Knowledge relationships
- Historical context
- Cross-project context
- Context inheritance
- Context prioritization
- Context expiration
- Graph-based retrieval

The module MUST support explicit control over which contextual relationships are active within a workflow.

### Loop Controller Module

The Loop Controller Module manages the lifecycle of the human-in-the-loop process.

Features include:

- Loop-state management
- Workflow orchestration
- State transitions
- Checkpoint management
- Approval management
- Rejection handling
- Revision handling
- Loop branching
- Loop merging
- Pause and resume
- Workflow cancellation
- Human escalation
- Error recovery

The Loop Controller MUST preserve human approval states and prevent unauthorized transitions into consequential execution states.

### Workflow Module

The Workflow Module defines reusable processes for reasoning, review, validation, approval, and execution.

Features include:

- Reusable workflows
- Custom workflow definitions
- Workflow templates
- Conditional workflow paths
- Human approval stages
- Policy checkpoints
- Review stages
- Validation stages
- Rollback stages
- Workflow versioning
- Workflow history
- Workflow sharing

Workflows MUST support explicit human checkpoints wherever required by policy, risk, impact, or configuration.

### Human Interface Module

The Human Interface Module presents system state and decision information to the human operator.

Features include:

- Structured decision panels
- Option comparison
- Recommendation display
- Risk indicators
- Confidence indicators
- Assumption display
- Policy status
- Approval controls
- Revision controls
- Rejection controls
- Comment and annotation support
- Decision justification
- Side-by-side alternatives
- Decision history

The interface MUST clearly communicate when information represents an AI recommendation, a system validation result, or a human decision.

### Model Abstraction Module

The Model Abstraction Module separates CortexLoop from any specific AI model or provider.

Features include:

- Multiple model providers
- Local models
- Remote models
- Model adapters
- Model routing
- Model selection
- Model comparison
- Model fallback
- Model capability profiles
- Model-specific policies
- Model version tracking
- Model provenance

The module MUST allow model components to be replaced without changing the fundamental human-governance architecture.

### Tool Governance Module

The Tool Governance Module controls access to external tools and records tool activity.

Features include:

- Tool registration
- Tool permissions
- Tool capability declarations
- Tool invocation logging
- Tool-result validation
- Tool risk classification
- Human approval for sensitive tools
- Tool execution history
- Tool rollback where supported
- Tool provenance
- Tool policy enforcement

Tools MUST operate within explicit permission boundaries and MUST NOT bypass the human decision architecture.

### Execution Safety Module

The Execution Safety Module provides safeguards for actions proposed or authorized through CortexLoop.

Features include:

- Permission boundaries
- Action classification
- Reversible and irreversible action detection
- Pre-action validation
- Human approval gates
- Execution logging
- Rollback support
- Failure handling
- Error reporting
- State integrity checks
- Duplicate-action prevention
- Unauthorized-action prevention

Irreversible or high-impact actions MUST require the appropriate human authorization before execution.

### Audit Module

The Audit Module provides comprehensive visibility into system activity.

Features include:

- Complete workflow history
- Decision audit trails
- Policy audit trails
- Human approval history
- Model activity history
- Tool activity history
- Configuration history
- Version history
- Exportable audit logs
- Audit filtering
- Audit search
- Audit comparison

Audit records MUST be protected against unauthorized modification.

### Versioning Module

The Versioning Module tracks changes to the system's decision environment.

Features include:

- Workflow versioning
- Policy versioning
- Constraint versioning
- Context versioning
- Decision versioning
- Configuration versioning
- Model version tracking
- Historical replay
- Change tracking
- Rollback support

Version information MUST be available when reconstructing historical decisions.

### Collaboration Module

The Collaboration Module supports workflows involving multiple human participants.

Features include:

- Multiple human reviewers
- Assigned decision ownership
- Review queues
- Approval delegation
- Secondary review
- Consensus workflows
- Conflicting-review handling
- Decision comments
- Annotations
- Shared context
- Team policies
- Organization policies

Collaborative workflows MUST preserve the identity and authority of each participating decision-maker.

### Human Feedback Module

The Human Feedback Module converts human interaction into controlled system feedback.

Features include:

- Explicit feedback
- Decision corrections
- Recommendation ratings
- Error reporting
- Preference updates
- Constraint updates
- Policy feedback
- Workflow feedback
- Feedback history
- Feedback-to-rule conversion
- Human-controlled learning signals

Human feedback MUST NOT silently change system behavior without the appropriate review or authorization process.

### Knowledge and Memory Module

The Knowledge and Memory Module manages persistent information used to support future workflows.

Features include:

- Session context
- Persistent project context
- Structured memory
- Decision memory
- Constraint memory
- Workflow memory
- Policy memory
- Provenance memory
- Context retrieval
- Memory prioritization
- Memory expiration
- Human-controlled memory editing

Users MUST be able to inspect, modify, and remove persistent information according to configured controls.

### Transparency Module

The Transparency Module provides visibility into the state and behavior of CortexLoop.

Features include:

- Visible system state
- Visible workflow state
- Visible active policies
- Visible constraints
- Visible assumptions
- Visible risks
- Visible confidence
- Visible model information
- Visible tool activity
- Visible human approvals
- Complete decision history

Meaningful system activity MUST NOT be intentionally hidden from the human decision-maker.

### Privacy and Data Control Module

The Privacy and Data Control Module provides controls over data storage, retention, access, and deletion.

Features include:

- Local-first deployment options
- User-controlled data storage
- Configurable retention
- Memory deletion
- Context deletion
- Audit-log retention policies
- Data access controls
- Workspace isolation
- Project isolation
- Sensitive-context restrictions
- Human-controlled data export

Data controls MUST respect configured retention, deletion, access, and isolation requirements.

### Governance Module

The Governance Module defines how authority, policies, approvals, delegation, and conflicts are managed.

Features include:

- Human authority hierarchy
- Policy hierarchy
- Rule precedence
- Approval authority
- Delegated authority
- Escalation rules
- Conflict resolution
- Governance history
- Governance versioning
- Governance auditability

Governance rules MUST remain explicit and auditable.

### Compliance Module

The Compliance Module manages license and project compliance requirements.

Features include:

- AGPL-3.0+ licensing
- License-aware workflows
- Attribution requirements
- License validation
- Attribution validation
- Notice tracking
- Contributor tracking
- Compliance checkpoints
- Network-deployment compliance considerations
- License provenance
- Compliance audit records

### Observability Module

The Observability Module provides visibility into operational system behavior.

Features include:

- System event logging
- Loop-state monitoring
- Workflow monitoring
- Decision monitoring
- Policy monitoring
- Tool monitoring
- Model monitoring
- Error monitoring
- Performance monitoring
- Audit monitoring
- System health reporting

---

## Optional Plugin Modules

CortexLoop MAY be extended through optional plugin modules. Plugins MUST operate within the core human-in-the-loop, transparency, policy, auditability, and safety requirements.

Plugins MUST NOT bypass core authorization controls or create undisclosed autonomous authority.

### Knowledge Plugin

Provides optional integrations for external or specialized knowledge sources.

Capabilities may include:

- Knowledge source connectors
- Specialized knowledge bases
- Document indexing
- Knowledge retrieval
- Source ranking
- Knowledge provenance
- Knowledge validation

### Search Plugin

Provides optional search and discovery capabilities.

Capabilities may include:

- Web search
- Local search
- Repository search
- Document search
- Source comparison
- Search provenance
- Search-result validation

### Research Plugin

Provides optional structured research workflows.

Capabilities may include:

- Research planning
- Source collection
- Evidence comparison
- Claim tracking
- Citation tracking
- Research synthesis
- Research review workflows

### Coding Plugin

Provides optional software-development reasoning and workflow capabilities.

Capabilities may include:

- Code analysis
- Architecture analysis
- Change proposals
- Test planning
- Code review
- Dependency analysis
- Repository reasoning
- Human-approved code changes

### Document Plugin

Provides optional document analysis and generation capabilities.

Capabilities may include:

- Document analysis
- Structured extraction
- Document comparison
- Revision proposals
- Document generation
- Document validation
- Approval workflows

### Data Analysis Plugin

Provides optional structured data reasoning capabilities.

Capabilities may include:

- Data inspection
- Data validation
- Statistical analysis
- Pattern detection
- Visualization recommendations
- Analysis comparison
- Human-reviewed conclusions

### Communication Plugin

Provides optional communication workflows.

Capabilities may include:

- Draft generation
- Message analysis
- Communication review
- Recipient validation
- Approval workflows
- Publication controls
- Communication audit records

### Automation Plugin

Provides optional controlled workflow automation.

Capabilities may include:

- Scheduled workflows
- Conditional workflows
- Repeated tasks
- Event-triggered workflows
- Human approval gates
- Execution monitoring
- Failure handling

Automation plugins MUST remain subordinate to CortexLoop's human authorization and policy controls.

### External Tool Plugin

Provides adapters for external applications and services.

Capabilities may include:

- Tool discovery
- Tool registration
- Permission management
- Invocation controls
- Result validation
- Tool provenance
- Tool auditing

### Storage Plugin

Provides optional storage backends for context, decisions, provenance, and audit records.

Capabilities may include:

- Context storage
- Decision storage
- Audit storage
- Provenance storage
- Memory storage
- Retention controls
- Export and import

### Interface Plugin

Provides alternative human interfaces.

Capabilities may include:

- Web interfaces
- Desktop interfaces
- Command interfaces
- Mobile interfaces
- Accessibility interfaces
- Custom decision dashboards

All interface plugins MUST preserve the visibility of decision state and human authorization controls.

### Governance Plugin

Provides specialized governance models.

Capabilities may include:

- Organization governance
- Team governance
- Multi-reviewer governance
- Consensus workflows
- Delegated authority
- Approval hierarchies
- Specialized compliance policies

### Audit Plugin

Provides specialized audit and compliance capabilities.

Capabilities may include:

- External audit export
- Compliance reporting
- Audit dashboards
- Historical comparison
- Policy compliance analysis
- Provenance verification

## Core Decision Loop

CortexLoop operates through a controlled decision loop:

**Observe → Understand → Reason → Compare → Evaluate → Present → Human Decide → Validate → Execute → Record → Review → Loop**

Each stage MUST preserve the distinction between machine-generated recommendations and human-authorized decisions.

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/cortexloop/](https://roxanneardary.com/cortexloop/)

---

## ⚖️ License & Notice Requirements

CortexLoop is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- CortexLoop specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file. 
