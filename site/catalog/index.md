---
layout: ri-default
title: Catalog
description: Catalog of known instruments, components, and related items associated with Rhythm Industries.
h1: CATALOG
abbrvs:
  Instrumentation: Instr
  Thermometer: Therm
  Liquid-in-Glass: LIG
  Bimetallic: BM
  Hydraulics: Hydra
  "Sight Indicator": Sight Ind
---

This catalog lists known instruments, components, and related items associated with Rhythm Industries.

Entries may represent:
- Items currently available through the [Parts Desk](/parts)
- Archived or reference-only items
- Records reconstructed from partial documentation

Absence from this catalog does not imply nonexistence.

<div class="ri-rule"></div>

## Index

<table class="catalog-table">
  <thead>
    <tr>
      <th>Part No.</th>
      <th>Type</th>
      <th>Category</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    {% assign items = site.catalog | sort: "title" %}
    {% for item in items %}
    <tr>
      <td>
        <a href="{{ item.url | relative_url }}"><code>{{ item.h1 }}</code></a>
      </td>
      <td>{{ item.description }}</td>
      <td class="category">
        {% assign cats = item.category | split: " · " %}
        {% for cat in cats %}
          {% if page.abbrvs[cat] %}
            <abbr title="{{ cat }}">{{ page.abbrvs[cat] }}</abbr>
          {% else %}
            {{ cat }}
          {% endif %}
          {% unless forloop.last %} · {% endunless %}
        {% endfor %}
      </td>
      <td>{{ item.status }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<p class="ri-meta">
Status indicates current desk availability or archival state at time of build.
</p>
