---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<div class="d-flex justify-content-between align-items-center mb-3">
  <a href="https://scholar.google.com/citations?user=bRKiIQIAAAAJ" target="_blank" class="btn btn-sm" style="border: 1px solid var(--global-text-color); color: var(--global-text-color);">
    <i class="ai ai-google-scholar"></i> View Google Scholar Profile
  </a>
</div>

<div class="pub-filters mb-4">
  <button class="btn btn-sm filter-btn active" data-filter="all">All</button>
  <button class="btn btn-sm filter-btn" data-filter="Haphazard Inputs" style="background-color:#e05c4b; color:white;">Haphazard Inputs</button>
  <button class="btn btn-sm filter-btn" data-filter="Online Learning" style="background-color:#d4622a; color:white;">Online Learning</button>
  <button class="btn btn-sm filter-btn" data-filter="LLM" style="background-color:#3d7ebf; color:white;">LLM</button>
  <button class="btn btn-sm filter-btn" data-filter="NLP" style="background-color:#4a90a4; color:white;">NLP</button>
  <button class="btn btn-sm filter-btn" data-filter="Vision" style="background-color:#2e8b57; color:white;">Vision</button>
  <button class="btn btn-sm filter-btn" data-filter="Time Series" style="background-color:#c47e17; color:white;">Time Series</button>
  <button class="btn btn-sm filter-btn" data-filter="Book" style="background-color:#7b5ea7; color:white;">Book</button>
  <button class="btn btn-sm filter-btn" data-filter="Cloud Computing" style="background-color:#5e9e6e; color:white;">Cloud Computing</button>
</div>

<div class="publications">
{% bibliography %}
</div>

<style>
.pub-filters {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.filter-btn {
  border: 2px solid transparent;
  opacity: 0.75;
  transition: opacity 0.2s, border-color 0.2s;
}
.filter-btn:hover {
  opacity: 1;
}
.filter-btn.active {
  opacity: 1;
  border-color: rgba(0,0,0,0.3);
  box-shadow: 0 0 0 2px rgba(0,0,0,0.15);
}
.filter-btn[data-filter="all"] {
  background-color: #555;
  color: white;
}
.pub-entry.hidden-by-filter {
  display: none;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const buttons = document.querySelectorAll('.filter-btn');
  const entries = document.querySelectorAll('.pub-entry');
  const yearHeaders = document.querySelectorAll('h2.bibliography');

  function updateYearHeaders() {
    yearHeaders.forEach(function (h2) {
      // Collect all .pub-entry siblings until the next h2
      var sibling = h2.nextElementSibling;
      var hasVisible = false;
      while (sibling && sibling.tagName !== 'H2') {
        if (sibling.classList.contains('pub-entry') && !sibling.classList.contains('hidden-by-filter')) {
          hasVisible = true;
          break;
        }
        sibling = sibling.nextElementSibling;
      }
      h2.style.display = hasVisible ? '' : 'none';
    });
  }

  buttons.forEach(function (btn) {
    btn.addEventListener('click', function () {
      buttons.forEach(function (b) { b.classList.remove('active'); });
      this.classList.add('active');

      const filter = this.dataset.filter;

      entries.forEach(function (entry) {
        if (filter === 'all') {
          entry.classList.remove('hidden-by-filter');
        } else {
          const tags = (entry.dataset.tags || '').split('|').map(function (t) { return t.trim(); });
          if (tags.includes(filter)) {
            entry.classList.remove('hidden-by-filter');
          } else {
            entry.classList.add('hidden-by-filter');
          }
        }
      });

      updateYearHeaders();
    });
  });
});
</script>
