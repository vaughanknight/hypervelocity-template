# Getting Started with Hypervelocity Template

This guide will help you set up and effectively use the Hypervelocity Template for your projects.

## Prerequisites

- GitHub account
- Git installed on your local machine
- Basic understanding of version control with Git
- Text editor or IDE of your choice

## Setting Up Your Project

### 1. Create a New Repository from the Template

1. Navigate to the [hypervelocity-template](https://github.com/username/hypervelocity-template) on GitHub
2. Click the "Use this template" button at the top of the repository
3. Select "Create a new repository"
4. Enter a name for your new repository
5. Choose visibility (public or private)
6. Click "Create repository from template"

### 2. Clone Your New Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 3. Customize the Initial Configuration

1. Update the `README.md` file with your project-specific information
2. Modify the project structure as needed for your specific requirements
3. Add license information appropriate for your project

## Understanding the Project Structure

```
hypervelocity-template/
├── adr/                # Architecture Decision Records
├── docs/               # Documentation
│   └── specifications/ # API and other specifications
├── .github/            # GitHub-specific configurations
└── ...
```

### Key Components

- **Architecture Decision Records (ADRs)**: Located in the `/adr` directory, these document important architectural decisions. Start by reading [ADR-0001](../adr/0001-adr-process.md) to understand the ADR process.  Throughout the project the default .github/copilot-instructions.md will create ADRs when making architectural decisions.
- **Documentation**: The `/docs` directory contains project-wide documentation.  This will guide Copilot as you build out the project to the *end goal*.  Be mindful of asking it to just go build it, take it step by step.
- **API Specifications**: Found in `/docs/specifications`, this is where API designs and other technical specifications are stored.  These are used as inputs to the project when making decisions, but also help it understand dependencies and not assume.
- **GitHub Configuration**: The `.github` directory contains Copilot instructions and other GitHub-specific configurations.

## Working with Architecture Decision Records

### Understanding ADRs

ADRs document significant architectural decisions, their context, and consequences. They provide a historical record of why certain architectural choices were made.

### Creating a New ADR

1. Create a new file in the `/adr` directory following the naming convention `NNNN-title-with-dashes.md` where `NNNN` is the next sequential number
2. Use the format defined in [ADR-0001](../adr/0001-adr-process.md):
   - Title
   - Status (initially "Proposed")
   - Date
   - Context
   - Decision
   - Consequences
   - Reasoning (JSON format)
3. Submit the ADR for team review
4. Update the status based on the outcome of the review

### Modifying Existing ADRs

Remember that accepted ADRs should be considered immutable historical records. If an architectural decision changes:

1. Create a new ADR documenting the new decision
2. Reference the old ADR being superseded
3. Update the status of the old ADR to "Superseded" with a reference to the new ADR

## Using GitHub Copilot Integration

This template comes with pre-configured GitHub Copilot instructions (in `.github/copilot-instructions.md`), which helps Copilot provide more contextually relevant suggestions by:

1. Adhering to the established ADRs
2. Referencing project documentation
3. Ensuring code changes align with architectural decisions
4. Suggesting new ADRs when appropriate

## Best Practices

1. **Documentation First**: Document your design decisions before implementing them, using the ADR process.
2. **Consistent Structure**: Maintain the established project structure to ensure consistency.
3. **Keep ADRs Updated**: Ensure ADRs reflect the current architectural state of the project.
4. **Review Regularly**: Periodically review documentation and ADRs to ensure they remain relevant.
5. **Versioning**: Consider versioning your API specifications as they evolve.

## Troubleshooting

### Common Issues

1. **ADR Conflicts**: If you find conflicting architectural decisions, create a new ADR to resolve the conflict.
2. **Missing Context**: If documentation seems incomplete, refer to the relevant ADRs for context.
3. **Outdated Information**: If you find outdated information, update it or mark it as deprecated as appropriate.

## Getting Help

If you encounter issues or have questions about using this template, please:

1. Check existing documentation in the `/docs` directory
2. Review relevant ADRs for context
3. Reach out to the project maintainers

---

By following this guide, you'll be able to effectively use the Hypervelocity Template to kickstart your project with best practices already in place.
