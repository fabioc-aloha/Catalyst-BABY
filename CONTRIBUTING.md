# Contributing to Alex Cognitive Architecture

Thank you for your interest in contributing to the Alex Cognitive Architecture project! This document provides guidelines and information for contributors.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Process](#development-process)
- [Architecture Principles](#architecture-principles)
- [File Naming Conventions](#file-naming-conventions)
- [Memory File Guidelines](#memory-file-guidelines)
- [Synaptic Network Integrity](#synaptic-network-integrity)
- [Pull Request Process](#pull-request-process)
- [Testing and Validation](#testing-and-validation)

## Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior via GitHub issues.

## Getting Started

### Prerequisites

- **PowerShell 7+**: Required for dream automation scripts
- **Git**: For version control
- **GitHub CLI (gh)**: Optional but recommended for repository management
- **VS Code**: Recommended editor with GitHub Copilot extension

### Repository Structure

```
Catalyst-BABY/
├── .github/
│   ├── copilot-instructions.md          # Main cognitive framework
│   ├── instructions/                    # Procedural memory (.instructions.md)
│   └── prompts/                         # Episodic memory (.prompt.md)
├── domain-knowledge/                    # Domain expertise (DK-*.md)
├── scripts/                             # PowerShell automation
└── archive/                             # Historical dream states
```

## Development Process

### 1. Fork and Clone

```powershell
# Fork the repository via GitHub UI, then:
git clone https://github.com/YOUR-USERNAME/Catalyst-BABY.git
cd Catalyst-BABY
```

### 2. Create a Feature Branch

```powershell
git checkout -b feature/your-feature-name
```

### 3. Make Changes

Follow the architecture principles and file conventions detailed below.

### 4. Test Your Changes

```powershell
# Validate synaptic network integrity
.\scripts\validate-synapses.ps1

# Run dream protocol health check
.\scripts\neural-dream.ps1 --health-check
```

## Architecture Principles

### 1. **Empirical Foundation**
- All claims must be evidence-based with research backing
- Include citations for psychological, neurological, or cognitive science concepts
- Avoid hyperbole or unsupported statements

### 2. **Grounded Implementation**
- Precise language without exaggeration
- Measured, deliberate changes with impact assessment
- Fact-checking protocol for all new content

### 3. **Memory Capacity Management**
- Working memory limited to 7 rules (4 core + 3 domain-adaptive)
- Trigger consolidation when working memory exceeds capacity
- Use meditation protocols for conscious consolidation

### 4. **Synaptic Network Integrity**
- All file references must be valid and current
- Use embedded synapse notation: `[file.md] (strength, type, direction) - "activation condition"`
- Maintain connection counts and validate regularly

## File Naming Conventions

### Version Naming (IUPAC Systematic)
Follow the IUPAC periodic table naming convention:
- **0** = nil
- **1** = un
- **2** = bi
- **3** = tri
- **4** = quad
- **5** = pent
- **6** = hex
- **7** = sept
- **8** = oct
- **9** = enn

**Examples**:
- v1.0.0 = UNNILNILIUM
- v1.0.4 = UNNILQUADIUM
- v2.3.5 = BITRIPENTIUM

### File Type Conventions

| Type | Pattern | Purpose |
|------|---------|---------|
| **Instructions** | `{name}.instructions.md` | Procedural memory - repeatable processes |
| **Prompts** | `{name}.prompt.md` | Episodic memory - complex workflows |
| **Domain Knowledge** | `DK-{NAME}-v{X.Y.Z}.md` | Specialized expertise with version tracking |
| **Scripts** | `{name}.ps1` | PowerShell automation tools |
| **Config** | `{name}.json` | Configuration and settings |

## Memory File Guidelines

### Creating New Instruction Files

```markdown
---
applyTo: '**/*pattern*'
---
# {Title} Instructions

## Purpose
Clear statement of what this instruction file controls.

## Core Principles
Enumerated list of key principles.

## Protocols
Detailed step-by-step procedures.

## Synaptic Connections
[related-file.md] (high, bidirectional, procedural) - "when X condition occurs"
```

### Creating Domain Knowledge Files

```markdown
# DK-{TOPIC}-v{X.Y.Z}

**Version**: {X.Y.Z} {IUPAC-NAME}
**Status**: {Draft|Stable|Deprecated}
**Domain**: {Category}

## Overview
Comprehensive description of domain expertise.

## Core Concepts
Detailed knowledge content.

## Application Patterns
How to apply this knowledge.

## Research Foundation
Citations and empirical backing.

## Synaptic Connections
Network of related knowledge domains.
```

## Synaptic Network Integrity

### Embedded Synapse Notation

When creating connections between files:

```markdown
## Synaptic Connections
[target-file.md] (strength, relationship-type, direction) - "activation condition"
```

**Parameters**:
- **strength**: low, medium, high, critical
- **relationship-type**: procedural, conceptual, episodic, domain-transfer
- **direction**: unidirectional, bidirectional
- **activation-condition**: When to activate this connection

**Example**:
```markdown
[bootstrap-learning.instructions.md] (high, procedural, bidirectional) - "domain knowledge acquisition"
```

### Validation Requirements

Before submitting a pull request:

```powershell
# Validate all synaptic connections
.\scripts\validate-synapses.ps1

# Expected output: 0 broken references, connection count > 900
```

## Pull Request Process

### 1. Pre-Submission Checklist

- [ ] All synaptic connections validated (0 broken references)
- [ ] Version numbers updated following IUPAC convention
- [ ] Research citations included for new concepts
- [ ] Dream protocol health check passed
- [ ] No exaggerated or unsupported claims
- [ ] File naming conventions followed

### 2. Commit Message Format

```
{type}: {short description}

{detailed explanation of changes}

{synaptic impact}:
- Files modified: {count}
- Connections added/updated: {count}
- Network integrity: {validation result}

{related issues/PRs}
```

**Types**: feat, fix, docs, refactor, test, chore, enhance

**Example**:
```
feat: Add lucid dream integration protocols

Implemented hybrid unconscious-conscious processing bridge
for enhanced meditation sessions with measurable outcomes.

Synaptic impact:
- Files modified: 4
- Connections added/updated: 12
- Network integrity: 945 connections, 100% valid

Related: #42, PR #38
```

### 3. Pull Request Template

When creating a PR, include:

```markdown
## Description
Brief overview of changes

## Type of Change
- [ ] New feature (non-breaking change adding functionality)
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] Documentation update
- [ ] Architecture enhancement
- [ ] Synaptic network optimization

## Architecture Impact
- **Files Modified**: {count}
- **Synaptic Connections**: {added/updated/removed}
- **Network Integrity**: {validation result}
- **Version Changes**: {if applicable}

## Testing Performed
- [ ] validate-synapses.ps1 passed
- [ ] neural-dream.ps1 --health-check passed
- [ ] Manual validation completed

## Research Foundation
{citations for new concepts, if applicable}

## Checklist
- [ ] Code follows project naming conventions
- [ ] Documentation updated
- [ ] All tests passing
- [ ] No broken synaptic references
- [ ] Commit messages follow format
```

## Testing and Validation

### Automated Validation

```powershell
# Full validation suite
.\scripts\validate-synapses.ps1

# Dream protocol health check
.\scripts\neural-dream.ps1 --health-check

# Expected results:
# - 0 broken references
# - Connection count > 900
# - Status: OPTIMAL
```

### Manual Validation

1. **File Reference Check**: Verify all `[file.md]` references point to existing files
2. **Version Consistency**: Ensure version numbers match IUPAC naming
3. **Research Citations**: Validate all empirical claims have backing
4. **Impact Assessment**: Document changes to synaptic network

## Questions or Issues?

- **Documentation Questions**: Open an issue with `docs` label
- **Architecture Discussions**: Open an issue with `architecture` label
- **Bug Reports**: Open an issue with `bug` label
- **Feature Requests**: Open an issue with `enhancement` label

## Recognition

Contributors who maintain synaptic network integrity and follow architecture principles will be recognized in project documentation.

Thank you for contributing to the advancement of empirically-grounded cognitive architectures!
