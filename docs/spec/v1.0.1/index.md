---
title: SLSA specification
description: SLSA is a specification for describing and incrementally improving supply chain security, established by industry consensus. It is organized into a series of levels that describe increasing security guarantees. This is **version 1.0** of the SLSA specification, which defines the SLSA levels.
---

SLSA is a specification for describing and incrementally improving supply chain
security, established by industry consensus. It is organized into a set of track and series of levels that describe increasing security guarantees.

This is **version 1.0.1** of the SLSA specification, which is a reorganized version of SLSA 1.0. It includes the Build Track version 1.0.

{%- for section in site.data.nav.main %}
{%- if section.url == page.url and section.children %}

## {{ section.title }}

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
