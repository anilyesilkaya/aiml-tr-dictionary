---
layout: default          # uses _layouts/default.html
title: Türkçe Yapay Zeka ve Makine Öğrenmesi Sözlüğü
permalink: /       # final URL → …/sozluk/
---

<!-- Search box (client-side filter) -->
<input id="search" placeholder="Ara…" autofocus>

<ul id="terimler">
  {%- assign entries = site.terms | sort: "title" -%}
  {%- for t in entries -%}
    <li data-title="{{ t.turkish | downcase }} {{ t.english | downcase }}">
      <a href="{{ t.url | relative_url }}">
        {{ t.english | default: t.turkish }}      <!-- link shows English first -->
      </a>
      {%- if t.english %}
        <em> ({{ t.turkish }})</em>              <!-- Turkish in parentheses -->
      {%- endif -%}
      {%- if t.categories -%}
        &nbsp;&mdash;&nbsp;<small>{{ t.categories | join: ", " }}</small>
      {%- endif -%}
    </li>
  {%- endfor -%}
</ul>

<script>
const box  = document.getElementById('search');
const rows = [...document.querySelectorAll('#terimler li')];
box.addEventListener('input', e => {
  const q = e.target.value.toLowerCase();
  rows.forEach(li => {
    li.style.display = li.dataset.title.includes(q) ? '' : 'none';
  });
});
</script>