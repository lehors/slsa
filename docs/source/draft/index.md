---
title: Source Track
description: The SLSA Source Track specification.
layout: specifications
---

{{ page.description }}

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
