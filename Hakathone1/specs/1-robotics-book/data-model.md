# Data Model: Physical AI & Humanoid Robotics Book

## Entities

### Module
- **Name**: String (required) - The title of the module
- **Description**: String (required) - Brief overview of the module's focus
- **Chapters**: Array of Chapter entities (exactly 3 per module)
- **Learning Objectives**: Array of strings - What students should understand after completing the module
- **Prerequisites**: Array of strings - Knowledge required before starting this module

### Chapter
- **Title**: String (required) - The chapter title
- **Module**: Module entity (required) - Which module this chapter belongs to
- **Content**: String (required) - The main content in Markdown format
- **Learning Objectives**: Array of strings - What students should understand after completing the chapter
- **Prerequisites**: Array of strings - Knowledge required before starting this chapter
- **Duration**: Number - Estimated reading time in minutes

### Learning Objective
- **Text**: String (required) - Description of what the student should understand
- **Module**: Module entity (optional) - If tied to a specific module
- **Chapter**: Chapter entity (optional) - If tied to a specific chapter
- **Measurable**: Boolean - Whether this objective can be tested/verified

### Content Section
- **Title**: String (required) - Section header
- **Content**: String (required) - Section body in Markdown
- **Type**: String (required) - One of: "concept", "architecture", "workflow", "example", "exercise"
- **Chapter**: Chapter entity (required) - Which chapter this section belongs to

## Relationships

- Module "contains" 3 Chapters (one-to-many)
- Chapter "belongs to" 1 Module (many-to-one)
- Module "has" many Learning Objectives (one-to-many)
- Chapter "has" many Learning Objectives (one-to-many)
- Chapter "contains" many Content Sections (one-to-many)

## Validation Rules

- Each Module MUST have exactly 3 Chapters
- Each Chapter MUST have a unique title within its Module
- Each Chapter MUST have at least one Learning Objective
- Each Content Section MUST have a valid Type from the allowed list
- Module Learning Objectives SHOULD align with the overall module focus
- Chapter Learning Objectives SHOULD contribute to the module's overall objectives
- Content Sections SHOULD be logically ordered within each Chapter