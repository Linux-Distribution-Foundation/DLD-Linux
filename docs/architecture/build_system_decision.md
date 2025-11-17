# DLD Linux Build System Decision

This document defines the build system strategy for the DLD Linux project as it enters the Alpha 0.1 development stage. All information reflects the formally established scope of the project and complies with LDF documentation standards.

## 1. Purpose

The purpose of this document is to describe the build methodology selected for DLD Linux, outline the rationale behind this choice, and establish how installation images will be produced throughout the Alpha phase.

## 2. Build System Requirements

The build system for DLD Linux must meet the following requirements:

* **Upstream Fidelity**: Maintain strict alignment with Ubuntu 24.04.3 LTS during Alpha 0.1–0.5.
* **Predictable Behavior**: Ensure consistent and reproducible build outputs.
* **Transparency**: Allow clear visibility into system changes and ISO customization.
* **Snap-Free Operation**: Prevent the inclusion of Snap or Snap-related components.
* **Practical Implementation**: Provide a manageable workflow for early distribution development.

## 3. Selected Build System

DLD Linux will use **Cubic (Custom Ubuntu ISO Creator)** as the sole build system for constructing installation images and performing all system customization activities.

Cubic provides a controlled, GUI-driven environment for modifying Ubuntu-based ISO images. It allows DLD Linux to build installation media without introducing complex or unnecessary tooling during the project’s early development stages.

## 4. Rationale for Exclusive Use of Cubic

Cubic is the chosen build system for the following reasons:

* **Upstream Image Preservation**: Cubic retains the structure and integrity of the original Ubuntu ISO.
* **Direct Customization Workflow**: All required modifications—package adjustments, system configuration, and Snap removal—can be applied directly within the Cubic environment.
* **Predictability and Repeatability**: Cubic yields consistent results across multiple builds, supporting predictable Alpha development.
* **Reduced Complexity**: Avoids the need for manual filesystem construction or specialized tooling such as debootstrap.
* **Alignment with Project Scope**: Reflects the project's limited downstream customization during early milestones.

## 5. Build System Scope for Alpha 0.1

During Alpha 0.1, the build system will be used to:

* Establish the initial Cubic-based workflow
* Validate image customization operations
* Ensure Snap removal and related cleanup can be performed reliably
* Prepare for integration work beginning in Alpha 0.2

No manual root filesystem construction or external build tooling will be used at this stage.

## 6. ISO Creation Workflow

Beginning with Alpha 0.1 and continuing throughout the Alpha series, the ISO creation workflow will consist of:

1. Importing the selected Ubuntu 24.04.3 LTS ISO into Cubic
2. Entering Cubic’s chroot customization environment
3. Applying DLD Linux system modifications (such as Snap removal)
4. Adjusting package selections and configuration where required by the milestone
5. Building the resulting ISO using Cubic’s standardized output process

This workflow provides full traceability and ensures that the final ISO remains closely aligned with upstream Ubuntu.

## 7. Future Considerations

As the project advances, Cubic may be used to support:

* Integration of KDE Plasma, GNOME, and Cinnamon
* Installer configuration adjustments
* Visual design and branding (when defined)
* Policy and default-system refinements

No alternative build systems or automated pipelines have been approved at this time.

## 8. Current Status

Cubic has been formally adopted as the exclusive build system for DLD Linux. Alpha 0.1 development will begin with the establishment of the Cubic workflow and initial ISO customization procedures.
