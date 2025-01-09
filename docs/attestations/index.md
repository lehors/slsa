---
title: Attestation formats
description: These pages include the concrete schemas for SLSA attestations. The
    Provenance and VSA formats are recommended, but not required by the
    specification.
layout: specifications
---

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
