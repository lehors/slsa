---
title: SLSA Specification
description: A one-page rendering of all that is included in the SLSA spec.
noindex: true
---
{%- comment -%}
A single page containing all the following files as different sections
This file needs to be processed last so make sure its filename is last in
alphabetical order (that seems to do the trick with Jekyll).
{%- endcomment -%}

{%- capture files %}
{%- include onepage-files.liquid %}
{%- endcapture %}
{% assign filenames = files | strip %}

{% include onepage.liquid dir=page.dir filenames=filenames %}
