---
description: Show help for Spec Driven development workflow commands
allowed-tools:
---


Briefly guide users on how to get started with Spec Driven Developer using the following documentation, without requiring them to write or read any code.


## Spec Driven development Development Workflow Commands

## USAGE

- /spec-COMMAND [feature-name]

## DESCRIPTION

Provides standardized development workflow commands to ensure a smooth progression of projects from concept to implementation.

## WORKFLOW PHASES

### Phase 0: Project Steering (Optional)

- /steering-init          Establishes initial steering documents (product.md, tech.md, structure.md)
- /steering-update        Updates existing steering documents
- /steering-custom        Creates customized steering documents (API specifications, testing strategies, etc.)

### Phase 1: Specification Creation (Core Workflow)

- /spec-init "description"       Initializes specification structure from project description
- /spec-requirements      Generates requirements definition document
- /spec-design           Generates technical design document (after requirements approval)
- /spec-tasks            Generates implementation task list (after design approval)

### Phase 2: Progress Management

- /spec-status: Queries feature development progress and status

## COMMAND DETAILS

- /steering-init: Initializes project steering documents, establishing product overview, technology stack, and project structure specifications.

- /steering-update: Updates steering documents based on recent changes, maintaining the accuracy of project knowledge.

- /steering-custom: Creates specialized steering documents, such as API standards, testing strategies, security policies, etc.

- /spec-init "Detailed project description": Initializes feature specifications based on the description, automatically generating a feature-name and directory structure.

- /spec-requirements \<feature-name\>: Generates user stories and acceptance criteria, requiring manual review and approval.

- /spec-design \<feature-name\>: Creates technical design documents, including architecture diagrams, APIs, and data models.

- /spec-tasks \<feature-name\>: Generates a list of implementation tasks, with each task estimated to take 2-4 hours to complete.

- /spec-status \<feature-name\>: Displays the current phase, approval status, and task completion progress.

## APPROVAL WORKFLOW

Each phase requires manual approval before proceeding to the next:

1.  Generate Requirements → Review requirements.md → Manually update spec.json for approval
2.  Generate Design → Review design.md → Manually update spec.json for approval
3.  Generate Tasks → Review tasks.md → Manually update spec.json for approval
4.  Begin Implementation

## EXAMPLES

(New Project Startup)
- /steering-init
- /spec-init "Develop PDF diagram extraction feature using Next.js and TypeScript"
- /spec-requirements pdf-diagram-extractor
(Review and approve requirements.md)
- /spec-design pdf-diagram-extractor
(Review and approve design.md)
- /spec-tasks pdf-diagram-extractor
(Review and approve tasks.md, then start implementation)
(Query Progress)
- /spec-status pdf-diagram-extractor
(Add New Feature to Existing Project)
- /steering-update
- /spec-init "Add user authentication system"
