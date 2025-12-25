# Data Model: Isaac Robot Brain Module

## Educational Content Structure

### Chapter Entity
- **name**: String (chapter title)
- **description**: String (brief chapter overview)
- **learning_objectives**: Array of strings (specific learning goals)
- **content_sections**: Array of Section entities
- **prerequisites**: Array of strings (required knowledge)
- **duration**: Number (estimated completion time in hours)

### Section Entity
- **title**: String (section heading)
- **content_type**: String (text, code, diagram, video)
- **body**: String (main content in Markdown format)
- **examples**: Array of Example entities (optional)
- **exercises**: Array of Exercise entities (optional)

### Example Entity
- **title**: String (example title)
- **description**: String (what the example demonstrates)
- **code**: String (optional code snippet)
- **explanation**: String (detailed explanation)

### Exercise Entity
- **title**: String (exercise title)
- **description**: String (what the exercise covers)
- **difficulty**: String (beginner, intermediate, advanced)
- **solution**: String (optional solution)

## Relationships
- Chapter contains multiple Sections
- Section may contain multiple Examples
- Section may contain multiple Exercises

## Validation Rules
- Each Chapter must have at least one Section
- Each Section title must be unique within a Chapter
- Content type must be one of: text, code, diagram, video
- Difficulty must be one of: beginner, intermediate, advanced

## State Transitions (if applicable)
- draft → review (content written, ready for review)
- review → approved (content reviewed and approved)
- approved → published (content published to Docusaurus site)