# DLD Linux Base System Overview

This document provides a technical overview of the foundational system architecture, development direction, and defined parameters of the DLD Linux project for the Alpha 0.1 stage. All information herein reflects current, formally established project scope and policy.

## 1. Base System Definition

DLD Linux is built on the **Ubuntu 24.04.3 LTS** base system for all Alpha releases from 0.1 through 0.5. During this phase, the distribution remains aligned with upstream Ubuntu without divergence from core system components.

Beginning with Alpha 0.6, the project will transition to an **Ubuntu 26.04 LTS** foundation. This will serve as the long‑term base for subsequent development and the eventual 1.0 stable release.

## 2. Supported Desktop Environments

DLD Linux intends to offer the following upstream desktop environments as its flagship options:

* **KDE Plasma**
* **GNOME**
* **Cinnamon**

These environments will be incorporated and evaluated during later Alpha stages focused on integration. The project has not defined any downstream modifications or behavioral adjustments to these environments at this time.

## 3. System Goals

The project’s currently defined objectives include:

* Delivering an upstream‑aligned Ubuntu‑based distribution without Snap
* Ensuring predictable and transparent system behavior
* Preserving user autonomy and avoiding vendor‑specific lock‑in
* Maintaining compatibility with Ubuntu’s official package archives

These goals form the technical and governance basis for all early development activities.

## 4. Snap Removal Policy

The sole downstream system change formally established for the Alpha phase is the removal of Snap from the distribution. No additional package removals, replacements, or behavioral alterations have been designated for implementation.

## 5. Repository and Package Sources

For Alpha 0.1, DLD Linux relies exclusively on the official Ubuntu 24.04.3 LTS package repositories. No custom DLD Linux repositories or package sources currently exist.

Active sources:

* **Ubuntu Main** (default)
* **Ubuntu Universe** (enabled as required)

The **Restricted** and **Multiverse** components remain disabled unless future policy explicitly authorizes their use.

## 6. Development Milestones

The project has defined the following development timeline:

* **Alpha 0.1** — Initial project setup and foundational infrastructure (Due Dec 1, 2025)
* **Alpha 0.2** — Begin component integration and early build structure (Due Jan 1, 2026)
* **Alpha 0.3** — Implement base system changes and validate Snap removal (Due Feb 1, 2026)
* **Alpha 0.4** — Add and refine upstream desktop environments (Due Mar 1, 2026)
* **Alpha 0.5** — Improve installer workflow and early stability (Due Apr 1, 2026)
* **Alpha 0.6** — Finalize Alpha stage with a near‑complete base system (Due May 1, 2026)
* **Beta 1** — Begin broad testing and fix major issues (Due Jun 1, 2026)
* **Beta 2** — Refine system defaults and behavior (Due Jul 1, 2026)
* **Beta 3** — Address remaining issues and prepare for release (Due Aug 1, 2026)
* **1.0 Release** — First stable DLD Linux release (Due Sep 1, 2026)

## 7. Governance and Compliance

DLD Linux operates under the governance of the Linux Distribution Foundation (LDF) and adheres to the project’s established documentation and policy framework:

* **CODE_OF_CONDUCT.md**
* **CONTRIBUTING.md**
* **SECURITY.md**

All project source code and documentation are licensed under the **GNU General Public License v3.0 (GPL‑3.0)**.

## 8. Current Status

Active system development has not yet begun. The GitHub repository, organizational structure, and project board have been created. Technical implementation of the DLD Linux base system will commence with the Alpha 0.1 milestone.
