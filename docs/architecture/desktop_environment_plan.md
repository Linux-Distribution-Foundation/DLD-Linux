# Desktop Environment Integration Plan

This document defines the initial integration strategy for desktop environments (DEs) in DLD Linux during the Alpha development cycle. It outlines the scope, sequencing, and technical principles governing KDE Plasma, GNOME, and Cinnamon integration.

## 1. Overview

DLD Linux intends to provide three flagship desktop environments:

* **KDE Plasma**
* **GNOME**
* **Cinnamon**

All environments will be integrated in an upstream-aligned, unmodified form. No downstream branding, behavioral alterations, or vendor-specific customizations will be introduced unless required for functional correctness.

## 2. Integration Philosophy

Desktop environment integration adheres to the following principles:

* **Upstream Fidelity:** Maintain full consistency with upstream defaults, configurations, and workflows.
* **Minimal Downstream Intervention:** Avoid patches or behavioral overrides unless necessary to preserve system stability.
* **Predictable System Behavior:** Ensure that DE components interact with the base Ubuntu system without introducing divergence.
* **No Branding or Theming Changes:** DLD Linux does not apply custom themes, visual modifications, or experience-level alterations.

## 3. Integration Milestones

Desktop environment work is aligned with the defined Alpha schedule.

### Alpha 0.1

* No DE integration tasks.
* Documentation, repository structure, and foundational policies only.

### Alpha 0.2

* Begin preparing DE integration structure within Cubic build workflows.
* Identify required upstream Ubuntu 24.04.3 packages for each DE.

### Alpha 0.3

* Validate that Snap removal does not impact DE package availability or operation.
* Confirm that APT-only workflows support all target DEs.

### Alpha 0.4

* Primary DE integration milestone.
* Add KDE Plasma, GNOME, and Cinnamon as selectable environments.
* Validate session management, display manager compatibility, and core functionality.

### Alpha 0.5

* Refine installer workflows related to DE selection.
* Ensure stable installation paths for all DEs.
* Resolve integration inconsistencies.

### Alpha 0.6

* Verify all DEs under the forthcoming Ubuntu 26.04 LTS base.
* Stabilize DE availability for transition into Beta.

## 4. Desktop Environment Characteristics

This section provides a high-level technical characterization of each supported environment.

### 4.1 KDE Plasma

* Modular and highly configurable.
* Provides extensive system integration capabilities.
* Runs atop the KDE Frameworks stack.

### 4.2 GNOME

* Provides a streamlined, opinionated workflow.
* Minimal customizations permissible to preserve upstream behavior.
* Requires validation of session integration post-Snap removal.

### 4.3 Cinnamon

* Traditional desktop metaphor.
* Derived from GNOME technologies but with reduced dependency complexity.
* Lightweight integration relative to Plasma or GNOME Shell.

## 5. Packaging and Source Requirements

All desktop environments are sourced exclusively from Ubuntu 24.04.3 LTS archives during early Alpha and from Ubuntu 26.04 LTS archives beginning in Alpha 0.6.

No DLD Linux-specific repositories, overlays, or derivative packaging are used.

Enabled sources:

* Ubuntu Main
* Ubuntu Universe (as required)

Restricted and Multiverse remain disabled unless future policy dictates otherwise.

## 6. Display Manager Strategy

The project has not yet selected a definitive display manager. The following considerations apply:

* Plasma typically integrates with **SDDM**.
* GNOME typically integrates with **GDM**.
* Cinnamon typically integrates with **LightDM**.

A unified display manager policy will be defined in a later milestone.

## 7. Testing and Validation

Each DE must pass the following verification requirements before entering Beta:

* Successful installation from Cubic-generated images.
* Verified login session functionality.
* Proper interaction with system services and package sources.
* No Snap dependencies or regressions.
* Consistent behavior across hardware configurations.

## 8. Current Status

No DE integration work has begun. All desktop environment elements remain planned for future Alpha milestones, with the majority of work scheduled for Alpha 0.4.
