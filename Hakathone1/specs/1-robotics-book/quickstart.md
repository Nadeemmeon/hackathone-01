# Quickstart Guide: Physical AI & Humanoid Robotics Book

## Prerequisites

- Node.js (version 18 or higher)
- npm or yarn package manager
- Git for version control
- Text editor or IDE for Markdown editing

## Setup Instructions

### 1. Clone the Repository
```bash
git clone [repository-url]
cd [repository-name]
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Start Development Server
```bash
npm start
```
This will start the Docusaurus development server and open the book in your browser at `http://localhost:3000`.

### 4. Create New Chapter
```bash
# Navigate to the docs directory
cd docs

# Create a new markdown file for your chapter
touch modules/[module-name]/[chapter-name].md
```

## Project Structure Overview

```
docs/
├── modules/                    # All book modules and chapters
│   ├── robotic-nervous-system/ # Module 1: The Robotic Nervous System
│   ├── ai-control-systems/     # Module 2: AI Control Systems
│   ├── hardware-integration/   # Module 3: Hardware Integration
│   └── advanced-topics/        # Module 4: Advanced Topics
├── src/                        # Custom React components
├── static/                     # Static assets
├── docusaurus.config.js        # Docusaurus configuration
├── sidebars.js                 # Navigation sidebar configuration
└── package.json               # Project dependencies and scripts
```

## Writing a Chapter

### Chapter File Template
```markdown
---
title: Chapter Title
sidebar_label: Chapter Title
description: Brief description of the chapter content
---

# Chapter Title

## Learning Objectives

- Objective 1
- Objective 2
- Objective 3

## Introduction

Brief introduction to the chapter topic...

## Main Content

### Section 1

Content for the first section...

### Section 2

Content for the second section...

## Summary

Brief summary of key concepts covered in the chapter.
```

### Content Guidelines

1. **Focus on Concepts**: Emphasize architectural and conceptual understanding over implementation details
2. **Textual Diagrams**: Describe diagrams and visual elements in text format rather than including images
3. **Progressive Learning**: Build on concepts introduced in earlier chapters
4. **Clear Objectives**: Define what students should understand after reading each chapter
5. **Target Audience**: Write for advanced students with AI/SE background

## Building for Production

```bash
npm run build
```

This generates a static site in the `build/` directory that can be deployed to GitHub Pages.

## Deployment to GitHub Pages

The site can be deployed to GitHub Pages using the following command:

```bash
GIT_USER=<Your GitHub username> npm run deploy
```

Or configure GitHub Actions for automated deployment by adding the workflow file to `.github/workflows/deploy.yml`.

## Navigation Structure

The sidebar navigation is defined in `sidebars.js` and organized by modules:

```javascript
module.exports = {
  docs: [
    {
      type: 'category',
      label: 'Module 1: The Robotic Nervous System',
      items: [
        'modules/robotic-nervous-system/ros2-architecture-for-humanoids',
        'modules/robotic-nervous-system/python-agents-and-robot-control',
        'modules/robotic-nervous-system/modeling-the-body-with-urdf'
      ],
    },
    // Additional modules...
  ],
};
```