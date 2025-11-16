# Contributing to DLD Linux

Thank you for your interest in contributing to **DLD Linux**.  
As a Linux distribution, DLD Linux requires careful attention to quality, security, reproducibility, and licensing.  
To maintain these standards, contributors must follow the guidelines outlined below.

---

## 1. General Contribution Principles

- Contributions must maintain the stability, reliability, and security expected of a Linux distribution.
- All changes must be reproducible and traceable.
- Code and packaging changes must respect upstream projects and avoid unnecessary divergence.
- All contributions must comply with the licensing of upstream components.

DLD Linux prioritizes:
- Clean packaging  
- Transparent changes  
- Upstream compatibility  
- Minimal downstream patching unless required  

---

## 2. Ways to Contribute

- Reporting bugs  
- Improving documentation  
- Contributing packaging or build scripts  
- Assisting with desktop environment integration  
- Testing pre-release builds  
- Providing translations  
- Contributing infrastructure or tooling improvements  

---

## 3. Code Contributions

### 3.1 Pull Requests

- All code contributions must go through a pull request.  
- Pull requests must describe the purpose, technical changes, and testing performed.  
- PRs should be atomic — avoid combining unrelated changes.

### 3.2 Coding Standards

- Follow the coding style used in the relevant upstream project.  
- Avoid major stylistic rewrites unless explicitly requested.  
- Shell scripts should follow POSIX sh unless bash-specific features are required.

### 3.3 Building and Testing

Before submitting a PR:

- Ensure the system builds successfully.  
- Verify that your changes do not introduce regressions.  
- Test both installation and runtime behavior where applicable.  

---

## 4. Packaging and System Integration

### 4.1 Packaging Guidelines

- Prefer upstream Debian packaging whenever possible.  
- Avoid unnecessary forks of Ubuntu or Debian packages.  
- Patches should:  
  - Be minimal  
  - Be documented  
  - Be forwarded upstream when appropriate  

### 4.2 Snap Removal Policy

Because DLD Linux does not use Snap:

- Contributions must not reintroduce Snap or Snap dependencies.  
- Ensure `.deb` packages are available and functional.

### 4.3 Desktop Environments

For KDE Plasma, GNOME, and Cinnamon:

- Upstream defaults should be preserved whenever feasible.  
- Avoid branding changes that alter workflow or behavior.  
- Packaging must not introduce vendor lock-in or telemetry.

---

## 5. Documentation Contributions

Documentation contributions should be:

- Clear  
- Concise  
- Technically accurate  
- Written in professional language  

All major features or changes must include updated documentation.

---

## 6. Reporting Issues

When submitting an issue, please include:

- Distribution version (e.g., Alpha 0.1)  
- Desktop environment used  
- Hardware details if relevant  
- Steps to reproduce  
- Expected vs. actual behavior  
- Logs or debug output when applicable  

Issues without sufficient detail may be delayed or closed.

---

## 7. Licensing Requirements

By submitting a contribution, you agree that:

- Your contribution is licensed under **GPL-3.0** (or a GPL-compatible license).  
- You have the legal right to contribute the code.  
- You do not introduce proprietary or closed-source components incompatible with GPL-3.0.

---

## 8. Code of Conduct

All contributors must follow the project's **Code of Conduct** (`CODE_OF_CONDUCT.md`).  
This includes expectations for professional behavior, respectful communication, and constructive collaboration.

If you observe a violation, report it through the process defined in the Code of Conduct.

---

## 9. Getting Started

1. Fork the repository.  
2. Create a feature branch.  
3. Make your changes.  
4. Test thoroughly.  
5. Submit a pull request with a clear and complete description.  

If you have questions about contributing, open a GitHub Discussion or Issue.

---

Thank you for helping improve DLD Linux.  
Your contributions strengthen the distribution and the broader open-source ecosystem.

