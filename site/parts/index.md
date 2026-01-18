---
layout: ri-default
title: Parts Desk
description: Surplus instruments, components, and equipment handled through the Rhythm Industries Parts Desk.
h1: PARTS DESK
no_top_rule: true
---


<div class="ri-bar ri-meta">
  <span>Voicemail inquiries:
    <a href="tel:+15134003849" style="color:var(--ink); font-weight:600">(513) 400-3849</a>
  </span>
  <span>DESK STATUS: <span class="ri-stamp"  style="color:var(--ink)">OPEN</span></span>
</div>

<!--
<div class="ri-notice">
  <span class="ri-tag">SHIPPING</span>
  <strong>Shipping is currently limited to FedEx and USPS.</strong>
</div>
-->

## Available Items

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
    {% assign items = site.catalog | sort: "title" | where: "status", "Available" %}
    {% for item in items %}
    <tr>
      <td>
        <a href="{{ item.url | relative_url }}"><code>{{ item.h1 }}</code></a>
      </td>
      <td>{{ item.description }}</td>
      <td class="category">
        {% assign cats = item.category | split: " · " %}
        {% for cat in cats %}
          {% if site.data.abbrvs[cat] %}
            <abbr title="{{ cat }}">{{ site.data.abbrvs[cat] }}</abbr>
          {% else %}
            {{ cat }}
          {% endif %}
          {% unless forloop.last %} · {% endunless %}
        {% endfor %}
      </td>
      <td>{{ item.status }}</td>
    </tr>
    {% endfor %}
    <tr>
      <td><code>SHOP-TRUCK</code></td>
      <td>2005 Toyota Tacoma 2WD V6</td>
      <td>Vehicle</td>
      <td>Available</td>
    </tr>
  </tbody>
</table>

<p class="ri-meta">
Additional items may be listed under <a href="/catalog/">Catalog</a>.
</p>

## Sought

<ol>
  <li>Casio SK-1 Sampling Keyboard · Any condition</li>
  <li>Aiwa CA-DW7 Portable Component System / Boombox</li>
  <li>Sharp GF-4700 Boombox · Black (not silver)</li>
</ol>

<div class="ri-rule"></div>

## Notice

- Items shown are available unless marked otherwise.
- Descriptions are accurate to the best information available.
  <br>&nbsp;
- Listings may appear elsewhere; inquiries are handled through this desk only.
- Messages sent via third-party platforms are not monitored.
  <br>&nbsp;
- Voicemail inquiries only.
- Incomplete inquiries may receive no response.
- Responses are issued by the next business day.
