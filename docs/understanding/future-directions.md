---
title: Future directions
description: The initial draft version (v0.1) of SLSA had a larger scope including protections against tampering with source code and a higher level of build integrity (Build L4). This page collects some early thoughts on how SLSA **might** evolve in future versions to re-introduce these notions and add other additional aspects of automatable supply chain security.
layout: specifications
---

The initial [draft version (v0.1)] of SLSA had a larger scope including
protections against tampering with source code and a higher level of build
integrity (Build L4). This page collects some early thoughts on how SLSA
**might** evolve in future versions to re-introduce those notions and add other
additional aspects of automatable supply chain security.

<section id="build-l4">

## Build track

### Build L4

A build L4 could include further hardening of the build platform and enabling
corraboration of the provenance, for example by providing complete knowledge of
the build inputs.

The initial [draft version (v0.1)] of SLSA defined a "SLSA 4" that included the
following requirements, which **may or may not** be part of a future Build L4:

-   Pinned dependencies, which guarantee that each build runs on exactly the
    same set of inputs.
-   Hermetic builds, which guarantee that no extraneous dependencies are used.
-   All dependencies listed in the provenance, which enables downstream verifiers
    to recursively apply SLSA to dependencies.
-   Reproducible builds, which enable other build platforms to corroborate the
    provenance.

</section>

<section id="source-track">

## Source track

A Source track will provide protection against tampering of the source code
prior to the build.

The current [draft version (v1.1)](source-requirements.md) describes levels
of increasing tamper resistance and ways consumers might verify properties
of source revisions using SLSA source provenance attestations.

</section>

<section id="buildenv-track">

## Build Environment track

The goal of a Build Environment track is to enable the detection of tampering
with core components of the compute environment executing builds.

The current [draft version](../draft/attested-build-env-levels.md)
of the Build Environment track includes the following requirements:

-   Generation and verification of SLSA Build Provenance for build images.
-   Validation of initial build environment system state against known good
    reference values.
-   Deployment of the hosted build platform on a compute system that supports
    system state measurement and attestation capabilities at the hardware level.

These requirements are **subject to significant change** while this track
is in draft.

</section>

<section id="build-platform-operations-track">

## Build Platform Operations track

A Build Platform Operations track could provide assurances around the hardening
of build platforms as they are operated.

The initial [draft version (v0.1)] of SLSA included a section on
[common requirements](../v0.1/requirements.md#common-requirements) that formed
the foundation of the guidance for
[verifying build systems](verifying-systems.md), which **may or may not** form
the basis for a future Build Platform Operations track:

-   Controls for approval, logging, and auditing of all physical and remote
    access to platform infrastructure, cryptographic secrets, and privileged
    debugging interfaces.
-   Conformance to security best practices to minimize the risk of compromise.
-   Protection of cryptographic secrets used by the build platform.

</section>

[draft version (v0.1)]: ../v0.1/requirements.md
