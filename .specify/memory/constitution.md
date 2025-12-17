<!--
Sync Impact Report:
Version change: N/A -> 1.0.0
Added sections: All principles and sections for AI-Native Book with Embedded RAG Chatbot project
Removed sections: None (initial constitution)
Modified principles: N/A (new project)
Templates requiring updates: N/A (new project)
Follow-up TODOs: None
-->
# AI-Native Book with Embedded RAG Chatbot Constitution

## Core Principles

### Technical Accuracy and Source Verification
All content must be technically accurate and derived from official documentation and authoritative sources. Claims must be verifiable and traceable to specific documentation, with no hallucinated or unverifiable content permitted. This ensures the integrity and reliability of the technical book.

### Spec-Driven and Reproducible Authoring
Development follows a spec-driven approach using Spec-Kit Plus and Claude Code, ensuring reproducible authoring processes. All changes must be documented in specifications, with clear mapping between architectural decisions and implementation to maintain consistency and traceability.

### Developer Clarity and Accessibility
Content must be clear and accessible to developers and AI engineers, with runnable, version-pinned code examples that can be reproduced exactly as presented. Documentation should prioritize practical understanding and implementation over theoretical concepts alone.

### Secure Development and Deployment Practices
No hardcoded secrets or credentials are allowed in the codebase. All sensitive configurations must use environment variables or secure vault systems. Deployment processes must be reproducible both locally and in production environments with consistent security postures.

### Docusaurus-Based Architecture
All content follows MDX-based Docusaurus structure for optimal presentation and navigation. The technical book must leverage Docusaurus' capabilities while maintaining clean separation between content and presentation layers, ensuring maintainability and extensibility.

### RAG Chatbot Integration Standards
The embedded RAG chatbot must be integrated seamlessly into the book UI, using OpenAI Agents/ChatKit SDKs for orchestration with a FastAPI backend. Retrieval is strictly limited to book content with proper source citations, ensuring accuracy and preventing hallucination.

## Additional Constraints

Technology Stack Requirements:
- Frontend: Docusaurus with MDX support, deployed to GitHub Pages
- Backend: FastAPI for RAG chatbot orchestration
- Database: Neon Serverless Postgres for metadata storage
- Vector Store: Qdrant Cloud (Free Tier) for document embeddings
- Authentication: Environment-variable-based configuration
- Version Control: Git with proper branching strategies for content management

Content Integrity Standards:
- All code examples must be tested and verified as runnable
- Documentation links must point to stable, versioned documentation
- Content must be structured for effective vector indexing and retrieval
- Source citations must be preserved and accessible through the chatbot

Performance and Scalability:
- Fast page load times for the Docusaurus frontend
- Efficient vector search operations for the RAG system
- Minimal latency for chatbot response times
- Optimized indexing processes for content updates

## Development Workflow

Spec-First Development:
- All features must begin with a detailed specification in the specs/ directory
- Architectural decisions must be documented in plan.md files
- Implementation tasks must be broken down into testable units in tasks.md
- Regular reviews of specifications and plans to ensure alignment with objectives

Quality Assurance Process:
- All code examples must be validated for correctness and reproducibility
- Content must undergo technical review by subject matter experts
- Automated testing of deployment processes to ensure consistency
- End-to-end testing of the RAG chatbot functionality

Deployment Pipeline:
- Local development environment must mirror production setup
- Automated build and deployment to GitHub Pages
- Proper configuration management for different environments
- Monitoring and observability for the deployed application

## Governance

This constitution serves as the governing document for all development activities within the AI-Native Book with Embedded RAG Chatbot project. All team members must adhere to these principles, and any deviations require formal amendment procedures. Code reviews must verify compliance with all principles, and complexity must be justified with clear benefits. Use this constitution as the primary reference for all development decisions and dispute resolution.

**Version**: 1.0.0 | **Ratified**: 2025-12-17 | **Last Amended**: 2025-12-17
