# Entra ID Group Naming Convention Guide


### Problem Statement
Organizations struggle with managing Entra ID groups effectively because inconsistent naming conventions lead to confusion, difficulty in identifying group purposes, and challenges in security governance. A standardized naming convention ensures clarity, improves searchability, enables efficient access management, and supports compliance auditing.

### Description
The organization adopts a structured, hierarchical naming convention for Entra ID security groups. This framework consists of five components separated by hyphens, each serving a distinct purpose in identifying the group's function, scope, and intended use. The convention follows this pattern:
Every new group must follow this exact structure:

#### `(Group Type)-(Assignment Type)-(Service Name)-(Sub-Service Name)-(Descriptive Group Name)`

Example Breakdown:
#### `SGR-USR-Entra-PIM-CloudAdmins`

- SGR (Group Type): It is a Security Group.
- USR (Assignment Type): Users are assigned to it manually.
- Entra (Service Name): It grants access within the Entra service.
- PIM (Sub-Service Name): It is used for Privileged Identity Management (temporary admin access).
- CloudAdmins (Descriptive Name): It is specifically for the Cloud Administrators team.

Each component is designed to be brief, meaningful, and universally understandable across the organization, enabling administrators and users to quickly identify group purposes without requiring additional documentation lookups.

For more detailed information reivew [Entra ID Naming Convention Components and Definitions](https://github.com/K-Lanflo/entra-group-namingconventions/blob/main/component-definitions.md)

### Rationale
Why This Convention Matters:

- Consistency: All groups follow the same predictable structure, eliminating ambiguity
- Searchability: Users can locate relevant groups quickly using Azure portal search functionality
- Governance: Security teams can audit and manage groups systematically based on their type and assignment model
- Scalability: As the organization grows, this convention accommodates hundreds or thousands of groups without confusion
- Compliance: Named groups serve as clear audit trails for regulatory requirements
- Operational Efficiency: Administrators spend less time interpreting group purposes and relationships
