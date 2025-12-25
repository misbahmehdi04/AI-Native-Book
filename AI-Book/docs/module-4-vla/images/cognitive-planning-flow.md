# Conceptual Diagram: Cognitive Planning with LLMs

## Cognitive Planning Architecture

```
Natural Language Goal
        |
        v
[LLM Goal Interpreter] --> Structured Goal + Context
        | (Intent Recognition,
        |  Entity Extraction)
        |
        v
[LLM Task Decomposer] --> Subtasks + Dependencies
        | (Goal Decomposition,
        |  Planning Strategy)
        |
        v
[Constraint Integrator] --> Feasible Plan + Constraints
        | (Robot Capabilities,
        |  Environment Constraints)
        |
        v
[Classical Planner] --> Executable Action Sequence
        | (Motion Planning,
        |  Path Planning)
        |
        v
[Execution Monitor] --> Execution Status + Feedback
        | (State Tracking,
        |  Exception Detection)
        |
        v
Robot Action Execution
```

## Alternative Planning Approaches

### Hierarchical Planning
```
High-Level Goal
     |
     v
[LLM] Goal → Subtasks
     |        /    |    \
     v       v     v     v
[Classical] Task1 Task2 Task3
     |       |     |     |
     v       v     v     v
Actions   Actions Actions Actions
```

### Reactive Planning
```
Goal + Context
     |
     v
[LLM] Current Action
     |
     v
Execution → Feedback → [LLM] Next Action
     |                     |
     v                     v
Environment ←------------- Monitoring
```

## Uncertainty Handling Flow

```
Ambiguous Goal
     |
     v
[LLM] Multiple Interpretations
     |
     v
Confidence Scoring
     |
     v
   High?  Low?
    /        \
Execute   Request Clarification
  |              |
  v              v
Monitor      User Response
```