<!--
Sync Impact Report:
- Version change: N/A → 1.0.0
- Added sections: All principles and governance sections
- Templates requiring updates: N/A
- Follow-up TODOs: None
-->
# AI/Spec-Driven Book with Embedded RAG Chatbot Constitution

## Core Principles

### Specification-First Development
All development begins with comprehensive specifications using Spec-Kit Plus methodology; No implementation without approved spec; Every feature must have clear acceptance criteria, test cases, and architectural decisions documented before coding begins.

### Accuracy and Retrieval-Grounded Responses
Chatbot responses must be strictly based on retrieved content from the book; No hallucination permitted; When context is insufficient, respond with "answer not available" rather than generating unsupported information; All answers must be traceable to specific book sections.

### Clarity for Technical Readers
Documentation and code must be accessible to technical audiences; Clear separation of concerns between book content, backend services, and chatbot functionality; Well-structured APIs with comprehensive documentation; Modular architecture enabling easy maintenance and extension.

### Reproducibility and Modularity
Full project must be reproducible from clean repository state; All dependencies and configurations documented; Automated deployment processes; Clear separation between book content management, backend services, and chatbot integration; Containerized services where appropriate.

### Technology Stack Compliance
Use specified technology stack: Docusaurus for book, FastAPI backend, OpenAI Agents/ChatKit SDKs, Qdrant Cloud (Free Tier), Neon Serverless Postgres; No unauthorized technology additions without explicit approval; Respect free-tier limits and cost constraints.

### Security and Constraint Adherence
No hardcoded secrets; All sensitive information managed through proper environment variables; Respect all platform limitations and quotas; Automated security scanning as part of deployment pipeline; Privacy-first approach to user data handling.

## Additional Constraints and Standards

Key standards:
- Book written in Docusaurus using `.md` files only
- Authored via Claude Code + Spec-Kit Plus
- Deployed to GitHub Pages
- Clear separation: book, backend, chatbot
- Free-tier limits respected for all cloud services
- Automated, repeatable deployment processes

Technology stack requirements:
- FastAPI backend with proper error handling and validation
- OpenAI Agents / ChatKit SDKs for chatbot functionality
- Qdrant Cloud (Free Tier) for vector storage and retrieval
- Neon Serverless Postgres for persistent data
- GitHub Pages for book hosting

## Development Workflow

- All changes follow Spec-Driven Development (SDD) methodology
- Specifications created using Spec-Kit Plus templates
- Architectural decisions documented in ADRs
- Code reviews must verify compliance with all constitution principles
- Automated testing required for all features
- Prompt History Records (PHRs) created for significant development activities
- Deployment to GitHub Pages upon successful CI/CD pipeline

## Governance

This constitution supersedes all other development practices and must be followed by all contributors. All architectural decisions must align with these principles. Any changes to this constitution require explicit approval and documentation. All pull requests and code reviews must verify compliance with these principles. Development activities must reference this constitution during planning and implementation phases.

**Version**: 1.0.0 | **Ratified**: 2025-12-21 | **Last Amended**: 2025-12-21
