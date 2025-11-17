# Contributing to DLD Linux

Thank you for your interest in contributing to **DLD Linux**, a project under the **Linux Distribution Foundation (LDF)**.  
As a Linux distribution, DLD Linux requires a high standard of quality, security, licensing compliance, and technical transparency.  
These guidelines ensure a stable, maintainable, and upstream-aligned distribution.

---

## 1. Core Contribution Principles

All contributions must follow these principles:

- Maintain system **stability**, **reliability**, and **security**.  
- Ensure all changes are **reproducible**, **auditable**, and technically justified.  
- Respect **upstream projects**, avoiding unnecessary divergence.  
- Ensure **licensing compatibility** with GPL-3.0 and upstream components.  
- Prefer clarity, maintainability, and minimal downstream customization.

DLD Linux prioritizes:

- Clean and transparent packaging  
- Upstream consistency and vendor neutrality  
- Avoidance of downstream fragmentation  
- Limited patching unless required for functionality or security  

---

## 2. Forms of Contribution

You may contribute by:

- Reporting bugs or regressions  
- Improving documentation  
- Packaging or maintaining `.deb` packages  
- Contributing build scripts or tooling  
- Testing release images and installation flows  
- Assisting with KDE, GNOME, or Cinnamon integration  
- Localization and translation work  
- Infrastructure improvements (CI, QA, automation)  

No contribution is too small — all improvements matter.

---

## 3. Code Contributions

### 3.1 Pull Request Requirements

All code must be submitted through a pull request (PR).

Each PR must:

- Provide a clear description of the change  
- State the problem it solves  
- Include testing steps and results  
- Remain **atomic** (one purpose per PR)

Large or complex changes may require a prior GitHub Discussion.

### 3.2 Coding & Style Expectations

- Match the coding conventions of the relevant upstream project.  
- Avoid broad restyling or refactoring unless requested.  
- Shell scripts should follow POSIX `sh` unless Bash is explicitly needed.  
- Code must be maintainable, well-structured, and explainable.

### 3.3 Building & Testing Requirements

Before submitting:

- Build the affected components/packages  
- Verify installation behavior where applicable  
- Test runtime behavior and confirm no regressions  
- Ensure packaging metadata is correct and reproducible  

PRs that cannot be built or tested will be delayed or rejected.

---

## 4. Packaging & Integration Standards

### 4.1 Packaging Guidelines

- Use upstream Debian/Ubuntu packaging whenever possible.  
- Avoid unnecessary forks of packages.  
- Patches must be:  
  - Minimal  
  - Documented  
  - Forwarded upstream when appropriate  
- Do not introduce undocumented behavioral changes.

### 4.2 Snap-Free Policy

Since DLD Linux is Snap-free:

- Contributions must not reintroduce Snap or Snap dependencies.  
- Ensure `.deb` alternatives exist and operate correctly.  
- Avoid components that implicitly pull Snap into the system.

### 4.3 Desktop Environments

DLD Linux supports KDE Plasma, GNOME, and Cinnamon.

Packaging must:

- Preserve upstream defaults and workflows  
- Avoid branding changes that alter user experience  
- Not introduce telemetry, lock-in, or vendor-specific manipulation  
- Maintain compatibility with upstream theming and configuration

---

## 5. Documentation Contributions

Documentation must be:

- Accurate  
- Professional  
- Clear and concise  
- Free of ambiguous or legally risky statements  

Major changes must include documentation updates.

---

## 6. Reporting Issues

Issues should include:

- DLD Linux version (e.g., Alpha 0.2)  
- Desktop environment in use  
- Hardware details if relevant  
- Steps to reproduce  
- Expected behavior vs. actual results  
- Logs or debug output (journalctl, package logs, installer logs)

Issues lacking detail may be closed or returned for clarification.

---

## 7. Licensing & Legal Compliance

By contributing, you confirm that:

- Your contribution is licensed under **GPL-3.0 or a GPL-compatible license**.  
- You have the legal right to contribute the code or content.  
- You do not introduce:  
  - Proprietary components  
  - License-incompatible code  
  - Non-redistributable or copyright-restricted material  
- You follow all upstream license requirements and attribution rules.

These requirements protect both contributors and the distribution.

---

## 8. Code of Conduct

All contributors must follow the project's **Code of Conduct** (`CODE_OF_CONDUCT.md`), which governs:

- Professional communication  
- Respectful collaboration  
- Technical integrity  
- Enforcement and reporting procedures  

Violations may result in warnings, PR rejections, or removal from participation.

---

## 9. Getting Started

1. Fork the repository.  
2. Create a dedicated feature or fix branch.  
3. Make your changes following these guidelines.  
4. Test thoroughly (build, install, runtime).  
5. Submit a pull request with a complete description.  
6. Respond to reviewer feedback as needed.

If unsure about anything, open a GitHub Discussion or Issue first.

---

Thank you for contributing to **DLD Linux**.  
Your work strengthens the project, the LDF ecosystem, and the broader open-source community.

