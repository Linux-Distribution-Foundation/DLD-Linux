# DLD Linux Packaging Policy

This document defines the authoritative packaging requirements, constraints, and workflow conventions for DLD Linux. All packaging-related work must adhere to these policies to ensure consistency, upstream alignment, and long-term maintainability.

## 1. Policy Scope

This policy governs all packaging activities performed within the DLD Linux project, including:

* Modification of Ubuntu packages
* Introduction of new packages
* Removal or disabling of packages
* Maintenance of downstream package configurations
* Packaging-related documentation and review procedures

This policy applies to all Alpha, Beta, and Stable development phases.

## 2. Upstream Alignment Requirements

DLD Linux is an upstream-aligned distribution. Therefore:

* **Ubuntu package sources must be used unmodified** unless a technical deviation is formally justified.
* Deviations from Ubuntu packaging must remain minimal, documented, and review-approved.
* Downstream patches must follow Debian/Ubuntu patch management conventions (e.g., `debian/patches` with proper metadata).
* Packages must retain compatibility with Ubuntu archives.

No package may be introduced that interferes with upstream ABI, API, or dependency expectations.

## 3. Snap Removal Constraints

DLD Linux enforces a strict Snap-free policy:

* All Snap-related packages, services, and dependencies must be removed or disabled.
* Packages introducing Snap as a dependency must be rejected unless an alternative is available.
* No package may re-enable Snap functionality directly or indirectly.

Snap removal must not compromise base system stability.

## 4. Repository and Archive Usage

During Alpha 0.1–0.5, all packaging work must use:

* **Ubuntu 24.04.3 LTS** as the immediate package source
* **Main** enabled by default
* **Universe** enabled only when required

Restricted and Multiverse remain disabled unless explicitly approved by governance.

No custom DLD Linux package repository exists at this stage.

## 5. Packaging Modifications

Any modifications to existing packages must:

* Maintain structural compatibility with upstream Debian/Ubuntu packaging standards
* Use standard packaging tools (e.g., `dpkg-source`, `debhelper`, `apt`)
* Include correct versioning using `~dld1` suffixes for downstream variants
* Provide explicit documentation in the package’s `debian/` directory when changes are applied

Unnecessary or cosmetic changes are not permitted.

## 6. Introduction of New Packages

New packages may only be added when:

* They address a defined system requirement
* Their licensing is compatible with GPL-3.0
* They introduce no Snap or proprietary dependencies
* Their inclusion does not duplicate upstream package functionality unless justified

All new packages must undergo a packaging review prior to acceptance.

## 7. Removal or Disabling of Packages

Packages may be removed only when:

* They include Snap-related functionality
* They are incompatible with DLD Linux’s system design
* Their presence introduces conflicts, instability, or unresolvable dependency behavior

Package removals must include technical rationale and regression analysis.

## 8. Build System Integration

All packaging activities must remain compatible with the distribution’s build methodology:

* ISO images are built exclusively using **Cubic**
* Packaging work must not require custom build frameworks or external infrastructure
* All package modifications must preserve the ability to produce stable, reproducible installation images

Any packaging process incompatible with Cubic is prohibited.

## 9. Documentation and Review

All packaging work must be documented clearly and must:

* Include rationale, expected behavior, and implementation details
* Follow the repository’s Markdown formatting conventions
* Align with the Coding Standards and CONTRIBUTING guidelines

All packaging changes must be reviewed and approved prior to merging.

## 10. Compliance and Enforcement

Non-compliant packaging submissions will be rejected. The Linux Distribution Foundation (LDF) maintains this policy and may revise it as DLD Linux evolves.

All contributors are responsible for understanding and applying this policy in its entirety.
