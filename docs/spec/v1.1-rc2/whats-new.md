---
title: What's new
description: The changes brought by SLSA v1.1.
---

This document describes the major changes brought by SLSA v1.1
relative to the prior release, [v1.0].

## Summary of changes

-   Clarify that attestation format schema are informative and the
    specification texts (SLSA and [in-toto attestation]) are the canonical
    source of definitions.
-   Add procedure for verifying VSAs.
-   Add verifier metadata to VSA format.
-   It is now recommended that the `digest` field of `ResourceDescriptor` is
    set in a Verification Summary Attestation's (VSA) `policy` object.
-   Further refine the [threat model](threats).

<!-- Footnotes and link definitions -->

[in-toto attestation]: https://github.com/in-toto/attestation
[v1.0]: /spec/v1.0/
