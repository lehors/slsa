---
title: Understanding SLSA
description: This section provides an overview of SLSA, how it helps protect against common
    supply chain attacks, and common use cases. If you're new to SLSA or
    supply chain security, start here.
layout: specifications
---

SLSA is a specification for describing and incrementally improving supply chain
security, established by industry consensus. It is organized into a set of tracks and levels that describe increasing security guarantees.

{%- for section in site.data.nav.main %}
{%- if section.url == page.url and section.children %}

{{ section.description }}

<!-- markdownlint-capture -->
<!-- markdownlint-disable MD055 MD056 -->
| Page | Description
| ---- | -----------
{%- for child in section.children %}
| [{{child.title}}]({{child.url | relative_url}}) | {{child.description}}
{%- endfor %}
<!-- markdownlint-restore -->

{%- endif %}
{%- endfor %}
