# Repository Structure

This document defines the current directory and file structure of the DLD Linux repository as it exists at the present stage of development. Only directories and files that have been explicitly created and committed to the project are included.

---

## 1. Root Directory

The root of the repository contains the following files and directories:

```
/
├── .github/
├── docs/
├── .editorconfig
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── SECURITY.md
```

---

## 2. .github Directory

The `.github` directory currently contains issue templates, ownership rules, and pull request templates.

```
.github/
├── ISSUE_TEMPLATE/
│   ├── bug_report.md
│   ├── documentation_issue.md
│   ├── feature_request.md
│   └── packaging_issue.md
├── CODEOWNERS
├── PULL_REQUEST_TEMPLATE.md
└── .gitkeep
```

---

## 3. Documentation Directory

All project documentation is located under the `docs/` directory, organized into architecture and policy subsections.

```
docs/
├── architecture/
│   ├── base_system_overview.md
│   ├── build_system_decision.md
│   └── desktop_environment_plan.md
└── policies/
    ├── coding_standards.md
    ├── packaging_policy.md
    └── repository_structure.md
```

---

## 4. Current Status

The repository structure documented above represents the complete and authoritative layout of the DLD Linux project as of the present development stage. Additional directories or files will be appended only when formally introduced through standard contribution and review procedures.
