---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<div class="pub-header" id="pub-header">
  <div class="pub-stats">
    <div class="pub-stat">
      <span class="stat-num" id="stat-total">—</span>
      <span class="stat-lbl">Pubs</span>
    </div>
    <div class="pub-stat-sep"></div>
    <div class="pub-stat">
      <span class="stat-num" id="stat-years">—</span>
      <span class="stat-lbl">Years</span>
    </div>
  </div>
  <a href="https://scholar.google.com/citations?user=bRKiIQIAAAAJ" target="_blank" class="scholar-btn">
    <i class="ai ai-google-scholar"></i>&ensp;Google Scholar
  </a>
</div>

<div class="pub-filters" id="pub-filters">
  <button class="filter-btn active" data-filter="all" data-color="#555">All</button>
  <button class="filter-btn" data-filter="Book" data-color="#7b5ea7">Book</button>
  <button class="filter-btn" data-filter="Cloud Computing" data-color="#5e9e6e">Cloud Computing</button>
  <button class="filter-btn" data-filter="Haphazard Inputs" data-color="#e05c4b">Haphazard Inputs</button>
  <button class="filter-btn" data-filter="LLM" data-color="#3d7ebf">LLM</button>
  <button class="filter-btn" data-filter="NLP" data-color="#4a90a4">NLP</button>
  <button class="filter-btn" data-filter="Online Learning" data-color="#d4622a">Online Learning</button>
  <button class="filter-btn" data-filter="Time Series" data-color="#c47e17">Time Series</button>
  <button class="filter-btn" data-filter="Vision" data-color="#2e8b57">Vision</button>
</div>

<div class="publications" id="pub-list">
{% bibliography %}
</div>

<style>
/* ══════════════════════════════════════════
   INLINE STATS (moved into .post-header)
══════════════════════════════════════════ */
.post-header {
  display: flex !important;
  align-items: center !important;
  justify-content: space-between !important;
  flex-wrap: wrap !important;
  gap: 0.5rem !important;
}
.pub-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 0;
}
.pub-stats {
  display: flex;
  align-items: center;
  gap: 0.6rem;
}
.pub-stat {
  display: flex;
  flex-direction: column;
  align-items: center;
  line-height: 1;
}
.stat-num {
  font-size: 1rem;
  font-weight: 700;
  color: var(--global-theme-color);
  line-height: 1;
}
.stat-lbl {
  font-size: 0.58rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--global-text-color-light);
  margin-top: 0.15rem;
}
.pub-stat-sep {
  width: 1px;
  height: 1.4rem;
  background: var(--global-divider-color);
}
.scholar-btn {
  display: inline-flex;
  align-items: center;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  border: 1.5px solid var(--global-theme-color);
  color: var(--global-theme-color) !important;
  font-size: 0.72rem;
  font-weight: 600;
  text-decoration: none !important;
  transition: background 0.18s, color 0.18s;
  white-space: nowrap;
}
.scholar-btn:hover {
  background: var(--global-theme-color);
  color: white !important;
}

/* ══════════════════════════════════════════
   FILTER PILLS
══════════════════════════════════════════ */
.pub-filters {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 1.8rem;
  margin-bottom: 1.4rem;
}
.filter-btn {
  display: inline-block;
  padding: 0;
  border: none;
  background: none;
  font-size: 0.82rem;
  font-weight: 500;
  cursor: pointer;
  color: var(--global-text-color-light);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  padding-bottom: 1px;
  transition: color 0.15s, border-color 0.15s;
}
.filter-btn:hover {
  color: var(--global-text-color);
  border-bottom-color: var(--global-text-color);
}
.filter-btn.active {
  color: var(--btn-active-color, #555);
  border-bottom-color: var(--btn-active-color, #555);
  font-weight: 700;
}

/* ══════════════════════════════════════════
   YEAR TIMELINE HEADERS
══════════════════════════════════════════ */
h2.bibliography.year-hidden,
ol.bibliography.year-hidden {
  display: none !important;
}
h2.bibliography {
  display: flex !important;
  align-items: center !important;
  gap: 0.75rem !important;
  font-size: 0.78rem !important;
  font-weight: 700 !important;
  letter-spacing: 0.12em !important;
  text-transform: uppercase !important;
  color: var(--global-text-color-light) !important;
  border: none !important;
  padding: 0 !important;
  margin-top: 2.2rem !important;
  margin-bottom: 1.1rem !important;
}
h2.bibliography::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--global-divider-color);
  display: block;
}

/* ══════════════════════════════════════════
   ENTRY CARDS
══════════════════════════════════════════ */
.pub-entry {
  position: relative;
  padding: 1rem 1.1rem;
  margin-bottom: 0.7rem !important;
  border: 1px solid var(--global-divider-color);
  border-left: 4px solid var(--entry-accent, var(--global-theme-color));
  border-radius: 0 10px 10px 0;
  background: var(--global-card-bg-color, var(--global-bg-color));
  transition: box-shadow 0.18s, border-color 0.18s;
}
.pub-entry:hover {
  box-shadow: 0 4px 18px rgba(0,0,0,0.08);
  border-top-color: var(--entry-accent, var(--global-theme-color));
  border-right-color: var(--entry-accent, var(--global-theme-color));
  border-bottom-color: var(--entry-accent, var(--global-theme-color));
}
.pub-entry.hidden-by-filter {
  display: none !important;
}

/* ── Title ── */
.pub-entry .title {
  font-size: 0.96rem;
  font-weight: 700;
  line-height: 1.45;
  margin-bottom: 0.28rem;
}

/* ── Author ── */
.pub-entry .author {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.15rem;
}

/* ── Periodical ── */
.pub-entry .periodical {
  font-size: 0.81rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.35rem;
}

/* ── Link buttons ── */
.pub-entry .links {
  margin-top: 0.45rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.3rem;
}
.pub-entry .links a.btn {
  font-size: 0.72rem;
  font-weight: 600;
  padding: 0.17rem 0.65rem !important;
  border-radius: 20px !important;
  margin-left: 0 !important;
  letter-spacing: 0.02em;
}

/* ── Preview image ── */
.pub-entry .preview {
  width: 100%;
  border-radius: 6px;
  object-fit: cover;
}


.pub-entry .entry-tag {
  background: var(--entry-accent, var(--global-theme-color)) !important;
  color: white !important;
  border-radius: 20px !important;
  font-size: 0.72rem;
  font-weight: 600;
  padding: 0.17rem 0.65rem !important;
  margin-left: 0 !important;
  opacity: 0.9;
}
.pub-entry .entry-tag a {
  color: white !important;
  text-decoration: none;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  /* ── Move stats bar into the page title header ── */
  const postHeader = document.querySelector('.post-header');
  const pubHeader  = document.getElementById('pub-header');
  if (postHeader && pubHeader) {
    postHeader.appendChild(pubHeader);
  }

  const buttons = document.querySelectorAll('.filter-btn');
  const entries = document.querySelectorAll('.pub-entry');
  const yearHeaders = document.querySelectorAll('h2.bibliography');

  /* ── Tag → accent color map ── */
  const tagColors = {
    'Haphazard Inputs': '#e05c4b',
    'Online Learning':  '#d4622a',
    'LLM':              '#3d7ebf',
    'NLP':              '#4a90a4',
    'Vision':           '#2e8b57',
    'Time Series':      '#c47e17',
    'Book':             '#7b5ea7',
    'Cloud Computing':  '#5e9e6e'
  };

  /* ── Count tags across all entries ── */
  entries.forEach(function (entry) {
    const tags = (entry.dataset.tags || '').split('|').map(t => t.trim());

    /* Apply left-border accent from first known tag */
    for (let i = 0; i < tags.length; i++) {
      if (tagColors[tags[i]]) {
        entry.style.setProperty('--entry-accent', tagColors[tags[i]]);
        break;
      }
    }

    /* Color each individual tag chip */
    entry.querySelectorAll('span.entry-tag').forEach(function (chip) {
      const label = chip.textContent.trim();
      if (tagColors[label]) {
        chip.style.setProperty('background-color', tagColors[label], 'important');
      }
    });
  });

  /* ── Apply active colors to filter buttons ── */
  buttons.forEach(function (btn) {
    const color = btn.dataset.color;
    if (color) btn.style.setProperty('--btn-active-color', color);
  });

  /* ── Fill stats bar ── */
  const el = function (id) { return document.getElementById(id); };
  if (el('stat-total'))    el('stat-total').textContent    = entries.length;
  if (el('stat-years')) {
    const years = new Set();
    yearHeaders.forEach(function (h) {
      const m = h.textContent.trim().match(/\d{4}/);
      if (m) years.add(m[0]);
    });
    el('stat-years').textContent = years.size;
  }

  /* ── Year header visibility helper ── */
  function updateYearHeaders() {
    yearHeaders.forEach(function (h2) {
      /* The next sibling is ol.bibliography — check if it has any visible li */
      var ol = h2.nextElementSibling;
      var hasVisible = false;
      if (ol) {
        var lis = ol.querySelectorAll('li');
        for (var i = 0; i < lis.length; i++) {
          if (lis[i].style.display !== 'none') {
            hasVisible = true;
            break;
          }
        }
      }
      h2.classList.toggle('year-hidden', !hasVisible);
      if (ol) ol.classList.toggle('year-hidden', !hasVisible);
    });
  }

  /* ── Filter click handler ── */
  buttons.forEach(function (btn) {
    btn.addEventListener('click', function () {
      buttons.forEach(b => b.classList.remove('active'));
      this.classList.add('active');

      const filter = this.dataset.filter;
      entries.forEach(function (entry) {
        var li = entry.closest('li');
        if (filter === 'all') {
          entry.classList.remove('hidden-by-filter');
          if (li) li.style.display = '';
        } else {
          var tags = (entry.dataset.tags || '').split('|').map(function (t) { return t.trim(); });
          var hide = !tags.includes(filter);
          entry.classList.toggle('hidden-by-filter', hide);
          if (li) li.style.display = hide ? 'none' : '';
        }
      });

      updateYearHeaders();
    });
  });
});
</script>
