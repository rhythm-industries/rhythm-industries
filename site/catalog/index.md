---
layout: ri-default
title: Catalog
description: Catalog of known instruments, components, and related items associated with Rhythm Industries.
h1: CATALOG
---

This catalog lists known instruments, components, and related items associated with Rhythm Industries.

Entries may represent:
- Items currently available through the [Parts Desk](/parts)
- Archived or reference-only items
- Records reconstructed from partial documentation

Absence from this catalog does not imply nonexistence.

<div class="ri-rule"></div>

## Index

<table>
  <thead>
    <tr>
      <th>Part No.</th>
      <th>Description</th>
      <th>Category</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    {% assign items = site.data.catalog %}
    {% for item in items %}
    <tr>
      <td>
        <a href="{{ item.url | relative_url }}"><code>{{ item.part }}</code></a>
      </td>
      <td>{{ item.description }}</td>
      <td>{{ item.category }}</td>
      <td>{{ item.status }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<p class="ri-meta">
Status indicates current desk availability or archival state at time of build.
</p>
