# Architecture And AI Pipeline

## System Architecture
AiKita follows a modular, service-oriented architecture:
- Frontend: Angular-based user interface for observations and planning workflows.
- Backend: .NET API as orchestration layer for business logic, persistence, and access control.
- AI Service: Python-based inference service for classification and recommendation pipeline.
- Data Layer: relational persistence for application state plus vector storage for retrieval support.

## Integration Model
The backend orchestrates all AI requests and returns structured responses to the UI. This setup provides:
- clear separation of concerns,
- controlled API contracts,
- and robust error handling between services.

## AI Pipeline Strategy
The AI stack is hybrid by design:
- Deterministic components (classification and rule-based constraints) provide stable structure.
- Probabilistic components (LLM-based generation) improve language quality and suggestion depth.
- Guardrails enforce schema and response consistency.

## Reliability Patterns
To keep the pipeline operational under uncertainty, the system applies:
- confidence-aware handling of model outputs,
- fallback strategies (for low-confidence or failed generation paths),
- defensive parsing and structured error mapping,
- iterative dataset improvement based on evaluation feedback.

## Security And Data Sensitivity
Because the domain handles sensitive child-related information, architecture decisions prioritize:
- role-based access and permission boundaries,
- secure transport and controlled API access,
- auditable changes and usage traces,
- and privacy-conscious processing paths.

## Why This Matters
The architecture is designed for real-world constraints: predictable behavior for educators, maintainability for developers, and traceability for institutions.