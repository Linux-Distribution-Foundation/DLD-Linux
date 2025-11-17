# DLD Linux Coding Standards

This document defines the authoritative coding, packaging, and repository conventions for the DLD Linux project. All contributors must adhere to these standards to ensure consistency, maintainability, and technical correctness across the distribution.

## 1. General Principles

* All development must align with the project’s goals of transparency, predictability, and upstream compatibility.
* Contributions must avoid introducing unnecessary complexity or divergence from Ubuntu unless explicitly approved.
* All changes must comply with the project’s GPL‑3.0 licensing requirements.

## 2. Repository Structure and Conventions

* All files must use UTF-8 encoding.
* Directory and file names must use **lowercase with underscores** (e.g., `base_system`, `installer_config`, `coding_standards.md`).
* Underscore‑based naming is the authoritative convention for DLD Linux and is required for all new files and directories.
* Hyphens must not be used for internal project structure unless required by an upstream component.
* Markdown documentation must follow a consistent hierarchy using `#` for top‑level titles and incrementally deeper headings.
* Configuration files must be placed in directories that reflect their functional purpose.

## 3. Shell Scripting Standards

* Scripts must target POSIX sh unless a specific shell is explicitly required.
* All scripts must start with an appropriate shebang (`#!/bin/sh` or `#!/usr/bin/env bash`).
* Indentation must use two spaces—tabs are not permitted.
* Scripts must include inline comments where functionality is non‑obvious.
* Error handling must be explicit; silent failures are not permitted.

## 4. Packaging Standards

* All packaging work must follow Ubuntu’s Debian packaging conventions unless otherwise defined.
* Packages must not conflict with upstream dependencies unless a technical justification exists.
* Snap dependencies must not be introduced under any circumstances.
* Any downstream patches must be minimal, documented, and approved through repository governance.

## 5. Documentation Requirements

* All new features, architectural decisions, and configuration changes must include accompanying documentation.
* Technical documentation must use a formal, precise tone consistent with LDF standards.
* Example commands or configuration snippets must be validated before inclusion.
* Each document must begin with a clear, descriptive heading.

## 6. Commit and Code Review Requirements

All code submissions must adhere to strict commit and review standards to ensure technical correctness, traceability, and alignment with DLD Linux project policies.

### 6.1 Commit Requirements

* Commits must be **atomic**, addressing one logical change per commit.
* Commit messages must follow this structure:

  * **Title:** A concise summary not exceeding 72 characters
  * **Body:** A clear, technically descriptive explanation of the change, including rationale when applicable
* Commit messages must not include ambiguous language or unexplained behavioral changes.
* All commits must comply with GPL-3.0 licensing requirements.

### 6.2 Pull Request Requirements

Pull requests must conform to the structure defined in `PULL_REQUEST_TEMPLATE.md`, including:

* A clear description of the change and its purpose
* Explicit classification of the change type (bug fix, feature, packaging, documentation, refactor, etc.)
* References to related issues or discussions when applicable
* A description of tests performed to validate functionality
* An assessment of potential impact on:

  * System stability
  * Packaging
  * Desktop environments
  * Installer or build processes (when relevant)
* Confirmation that the change follows all CONTRIBUTING.md and coding standards requirements

### 6.3 Code Review Standards

* All pull requests must undergo at least one peer review before merging.
* Reviewers must verify:

  * Compliance with coding standards and repository structure rules
  * GPL-3.0 licensing compatibility
  * Correctness, clarity, and maintainability of code
  * Alignment with upstream Ubuntu behavior unless deviation is explicitly approved
  * Absence of Snap dependencies
* Review feedback must be technically specific and actionable.

### 6.4 Approval Criteria

A pull request may be approved only when:

* All required checklist items are completed
* Documentation has been updated as necessary
* Tests verify correct behavior and no regressions
* The reviewer confirms alignment with DLD Linux goals of transparency, predictability, and upstream consistency

## 7. Compliance and Enforcement. Compliance and Enforcement

* All contributors must follow these standards as part of the contribution process.
* Non‑compliant submissions will require revision before merging.
* The Coding Standards are maintained by the Linux Distribution Foundation (LDF) and will be updated as the project advances.
