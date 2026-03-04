---
title: Notes
---

<style>
  .topbar { display: flex; align-items: baseline; justify-content: space-between; gap: 16px; }
  .topbar .title { font-size: 1.6rem; font-weight: 700; margin: 0; }
  .topbar .meta { font-size: 0.95rem; opacity: 0.75; white-space: nowrap; }
  .sections { margin-top: 1rem; }
</style>

<div class="topbar">
  <div class="title">{{ site.title | default: "Notes" }}</div>
  <div class="meta">Updated {{ site.time | date: "%Y-%m-%d" }}</div>
</div>

<div class="sections">
  <ul>
    <li><a href="{{ "/BrainDump/" | relative_url }}">BrainDump</a></li>
    <li><a href="{{ "/Market_Intelligence/" | relative_url }}">Market Intelligence</a></li>
  </ul>
</div>
