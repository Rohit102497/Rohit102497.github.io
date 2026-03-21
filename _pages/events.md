---
layout: page
permalink: /events/
title: Events
nav: true
nav_order: 5
---

<style>
/* ── Page intro ───────────────────────────────────────────────────────── */
.ev-intro {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 2.5rem;
  padding-bottom: 1.5rem;
  border-bottom: 2px solid var(--global-divider-color);
}
.ev-intro-text { flex: 1; min-width: 220px; }
.ev-intro-text p { color: var(--global-text-color-light); margin: 0; font-size: 0.95rem; line-height: 1.7; }
.ev-stats { display: flex; gap: 1.5rem; flex-wrap: wrap; }
.ev-stat {
  text-align: center;
  min-width: 70px;
}
.ev-stat-num {
  font-size: 2rem;
  font-weight: 800;
  color: var(--global-theme-color);
  line-height: 1;
}
.ev-stat-label {
  font-size: 0.72rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--global-text-color-light);
  font-weight: 600;
  margin-top: 0.2rem;
}

/* ── Section header ───────────────────────────────────────────────────── */
.ev-section-title {
  font-size: 0.72rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--global-text-color-light);
  margin: 0 0 1.25rem;
  display: flex;
  align-items: center;
  gap: 0.6rem;
}
.ev-section-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--global-divider-color);
}

/* ── Event cards grid ─────────────────────────────────────────────────── */
.ev-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.75rem;
  margin-bottom: 3rem;
}

.ev-card {
  border-radius: 14px;
  overflow: hidden;
  border: 1px solid var(--global-divider-color);
  background: var(--global-card-bg-color, var(--global-bg-color));
  transition: box-shadow 0.22s, transform 0.22s;
  display: flex;
  flex-direction: column;
  text-decoration: none !important;
  color: inherit !important;
}
.ev-card:hover {
  box-shadow: 0 12px 40px rgba(0,0,0,0.13);
  transform: translateY(-5px);
}

/* ── Browser mockup preview ───────────────────────────────────────────── */
.ev-preview {
  position: relative;
  height: 170px;
  overflow: hidden;
  flex-shrink: 0;
}
.ev-browser-bar {
  position: absolute;
  top: 0; left: 0; right: 0;
  z-index: 3;
  background: rgba(0,0,0,0.35);
  backdrop-filter: blur(4px);
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.45rem 0.8rem;
}
.ev-browser-dots { display: flex; gap: 5px; }
.ev-browser-dot {
  width: 9px; height: 9px;
  border-radius: 50%;
}
.ev-dot-r { background: #ff5f57; }
.ev-dot-y { background: #febc2e; }
.ev-dot-g { background: #28c840; }
.ev-browser-url {
  flex: 1;
  background: rgba(255,255,255,0.18);
  border-radius: 5px;
  padding: 0.15rem 0.6rem;
  font-size: 0.63rem;
  color: rgba(255,255,255,0.85);
  font-family: 'SF Mono', 'Fira Code', monospace;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.ev-preview-screenshot {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
  display: block;
  padding-top: 30px;
}

/* ── Card body ────────────────────────────────────────────────────────── */
.ev-body {
  padding: 1.2rem 1.35rem 1.35rem;
  display: flex;
  flex-direction: column;
  flex: 1;
}
.ev-badges {
  display: flex;
  gap: 0.4rem;
  flex-wrap: wrap;
  margin-bottom: 0.7rem;
}
.ev-badge {
  font-size: 0.62rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.07em;
  padding: 0.18rem 0.55rem;
  border-radius: 20px;
}
.ev-badge-organizer { background: rgba(181,9,172,0.1); color: var(--global-theme-color); border: 1px solid rgba(181,9,172,0.25); }
.ev-badge-upcoming  { background: rgba(16,185,129,0.1); color: #059669; border: 1px solid rgba(16,185,129,0.3); }
.ev-badge-past      { background: rgba(100,116,139,0.1); color: #64748b; border: 1px solid rgba(100,116,139,0.25); }
.ev-badge-workshop  { background: rgba(59,130,246,0.1); color: #2563eb; border: 1px solid rgba(59,130,246,0.25); }
.ev-badge-conference{ background: rgba(245,158,11,0.1); color: #b45309; border: 1px solid rgba(245,158,11,0.25); }

.ev-title {
  font-size: 1.05rem;
  font-weight: 700;
  margin: 0 0 0.45rem;
  line-height: 1.35;
  color: var(--global-text-color);
}
.ev-meta {
  font-size: 0.8rem;
  color: var(--global-text-color-light);
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin-bottom: 0.7rem;
}
.ev-meta span { display: flex; align-items: center; gap: 0.3rem; }
.ev-desc {
  font-size: 0.83rem;
  color: var(--global-text-color-light);
  line-height: 1.6;
  margin: 0 0 0.85rem;
  flex: 1;
}
.ev-topics {
  display: flex;
  flex-wrap: wrap;
  gap: 0.35rem;
  margin-bottom: 1rem;
}
.ev-topic {
  font-size: 0.65rem;
  padding: 0.18rem 0.55rem;
  border-radius: 20px;
  background: var(--global-divider-color);
  color: var(--global-text-color-light);
  font-weight: 600;
}
.ev-link {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  font-size: 0.78rem;
  font-weight: 600;
  padding: 0.35rem 0.9rem;
  border-radius: 20px;
  border: 1.5px solid var(--global-theme-color);
  color: var(--global-theme-color) !important;
  text-decoration: none !important;
  transition: background 0.18s, color 0.18s;
  align-self: flex-start;
  margin-top: auto;
}
.ev-link:hover {
  background: var(--global-theme-color);
  color: white !important;
}

/* ── Mini timeline (for smaller events) ──────────────────────────────── */
.ev-mini-list {
  list-style: none;
  padding: 0;
  margin: 0 0 3rem;
  position: relative;
}
.ev-mini-list::before {
  content: '';
  position: absolute;
  left: 10px; top: 6px; bottom: 6px;
  width: 2px;
  background: var(--global-divider-color);
}
.ev-mini-item {
  display: flex;
  gap: 1.25rem;
  padding-left: 2rem;
  margin-bottom: 1.1rem;
  position: relative;
}
.ev-mini-item::before {
  content: '';
  position: absolute;
  left: 2px; top: 5px;
  width: 18px; height: 18px;
  border-radius: 50%;
  background: var(--global-theme-color);
  border: 3px solid var(--global-bg-color);
  box-shadow: 0 0 0 2px var(--global-theme-color);
}
.ev-mini-year {
  min-width: 50px;
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--global-text-color-light);
  padding-top: 2px;
  flex-shrink: 0;
}
.ev-mini-body { flex: 1; font-size: 0.88rem; line-height: 1.6; }

@media (max-width: 576px) {
  .ev-grid { grid-template-columns: 1fr; }
  .ev-mini-year { display: none; }
  .ev-stats { gap: 1rem; }
  .ev-stat-num { font-size: 1.6rem; }
}
</style>

<!-- ── Page intro ─────────────────────────────────────────────────────── -->
<div class="ev-intro">
  <div class="ev-intro-text">
    <p>Workshops, conferences, and community events I have organized or co-organized — spanning AI research, life sciences, and early-career researcher development.</p>
  </div>
  <div class="ev-stats">
    <div class="ev-stat">
      <div class="ev-stat-num">7</div>
      <div class="ev-stat-label">Events</div>
    </div>
<div class="ev-stat">
      <div class="ev-stat-num">2</div>
      <div class="ev-stat-label">Upcoming</div>
    </div>
  </div>
</div>

<!-- ── Featured Events ────────────────────────────────────────────────── -->
<p class="ev-section-title"><i class="fa-solid fa-star fa-xs"></i> Featured Events</p>

<div class="ev-grid">

  <!-- Bioscopy 2026 -->
  <div class="ev-card">
    <div class="ev-preview">
      <div class="ev-browser-bar">
        <div class="ev-browser-dots">
          <div class="ev-browser-dot ev-dot-r"></div>
          <div class="ev-browser-dot ev-dot-y"></div>
          <div class="ev-browser-dot ev-dot-g"></div>
        </div>
        <div class="ev-browser-url">3dnanoscopy.com/bioscopy-conference</div>
      </div>
      <img class="ev-preview-screenshot" src="https://image.thum.io/get/width/640/crop/350/https://www.3dnanoscopy.com/bioscopy-conference/" alt="Bioscopy Conference 2026 website preview" loading="lazy">
    </div>
    <div class="ev-body">
      <div class="ev-badges">
        <span class="ev-badge ev-badge-organizer"><i class="fa-solid fa-person-chalkboard fa-xs"></i> Organizer</span>
        <span class="ev-badge ev-badge-conference">Conference</span>
        <span class="ev-badge ev-badge-upcoming">Upcoming</span>
      </div>
      <div class="ev-title">Bioscopy Conference 2026</div>
      <div class="ev-meta">
        <span><i class="fa-solid fa-calendar-days fa-xs"></i> Jun 15–17, 2026</span>
        <span><i class="fa-solid fa-location-dot fa-xs"></i> UiT Tromsø, Norway (69°N)</span>
      </div>
      <p class="ev-desc">"Organized by young researchers for young researchers" — an interdisciplinary conference bridging Life Sciences and Advanced Imaging, celebrating authentic research journeys including setbacks and negative results.</p>
      <div class="ev-topics">
        <span class="ev-topic">Advanced Imaging</span>
        <span class="ev-topic">AI for Biology</span>
        <span class="ev-topic">Quantitative Biology</span>
      </div>
      <a href="https://www.3dnanoscopy.com/bioscopy-conference/" target="_blank" rel="noopener noreferrer" class="ev-link">
        <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> Visit Website
      </a>
    </div>
  </div>

  <!-- AI4Fertility 2026 -->
  <div class="ev-card">
    <div class="ev-preview">
      <div class="ev-browser-bar">
        <div class="ev-browser-dots">
          <div class="ev-browser-dot ev-dot-r"></div>
          <div class="ev-browser-dot ev-dot-y"></div>
          <div class="ev-browser-dot ev-dot-g"></div>
        </div>
        <div class="ev-browser-url">bioailab.org/ai4fertility</div>
      </div>
      <img class="ev-preview-screenshot" src="https://image.thum.io/get/width/640/crop/350/https://www.bioailab.org/ai4fertility" alt="AI4Fertility Workshop website preview" loading="lazy">
    </div>
    <div class="ev-body">
      <div class="ev-badges">
        <span class="ev-badge ev-badge-organizer"><i class="fa-solid fa-person-chalkboard fa-xs"></i> Organizer</span>
        <span class="ev-badge ev-badge-workshop">Workshop</span>
        <span class="ev-badge ev-badge-upcoming">Upcoming</span>
      </div>
      <div class="ev-title">1st Workshop on AI in Fertility Science</div>
      <div class="ev-meta">
        <span><i class="fa-solid fa-calendar-days fa-xs"></i> Apr 18, 2026</span>
        <span><i class="fa-solid fa-location-dot fa-xs"></i> Tromsø, Norway</span>
      </div>
      <p class="ev-desc">The first workshop dedicated to the intersection of artificial intelligence and fertility science — bringing together AI researchers and reproductive biologists to explore computational approaches to fertility diagnostics and treatment.</p>
      <div class="ev-topics">
        <span class="ev-topic">AI in Medicine</span>
        <span class="ev-topic">Fertility Science</span>
        <span class="ev-topic">Computer Vision</span>
        <span class="ev-topic">Embryology</span>
      </div>
      <a href="https://www.bioailab.org/ai4fertility" target="_blank" rel="noopener noreferrer" class="ev-link">
        <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> Visit Website
      </a>
    </div>
  </div>

  <!-- CHOMPS 2025 -->
  <div class="ev-card">
    <div class="ev-preview">
      <div class="ev-browser-bar">
        <div class="ev-browser-dots">
          <div class="ev-browser-dot ev-dot-r"></div>
          <div class="ev-browser-dot ev-dot-y"></div>
          <div class="ev-browser-dot ev-dot-g"></div>
        </div>
        <div class="ev-browser-url">chomps2025.github.io</div>
      </div>
      <img class="ev-preview-screenshot" src="https://image.thum.io/get/width/640/crop/350/https://chomps2025.github.io/" alt="CHOMPS 2025 website preview" loading="lazy">
    </div>
    <div class="ev-body">
      <div class="ev-badges">
        <span class="ev-badge ev-badge-organizer"><i class="fa-solid fa-person-chalkboard fa-xs"></i> Organizer</span>
        <span class="ev-badge ev-badge-workshop">Workshop</span>
        <span class="ev-badge ev-badge-past">Past</span>
      </div>
      <div class="ev-title">CHOMPS 2025: Confabulation, Hallucinations &amp; Overgeneration in Multilingual and Practical Settings</div>
      <div class="ev-meta">
        <span><i class="fa-solid fa-calendar-days fa-xs"></i> Dec 23, 2025</span>
        <span><i class="fa-solid fa-location-dot fa-xs"></i> Mumbai, India · AACL-IJCNLP</span>
      </div>
      <p class="ev-desc">Advances in hallucination mitigation in practical situations: multilingual and precision-critical domains. Featuring four keynote speakers, a shared task (SHROOM-CAP), and a panel on language and domain-specific hallucinations.</p>
      <div class="ev-topics">
        <span class="ev-topic">LLM Hallucinations</span>
        <span class="ev-topic">Factuality</span>
        <span class="ev-topic">Multilingual NLP</span>
        <span class="ev-topic">Shared Task</span>
      </div>
      <a href="https://chomps2025.github.io/" target="_blank" rel="noopener noreferrer" class="ev-link">
        <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> Visit Website
      </a>
    </div>
  </div>

  <!-- LLM Workshop 2023 -->
  <div class="ev-card">
    <div class="ev-preview">
      <div class="ev-browser-bar">
        <div class="ev-browser-dots">
          <div class="ev-browser-dot ev-dot-r"></div>
          <div class="ev-browser-dot ev-dot-y"></div>
          <div class="ev-browser-dot ev-dot-g"></div>
        </div>
        <div class="ev-browser-url">bioailab.org/arcticllmworkshop2023</div>
      </div>
      <img class="ev-preview-screenshot" src="https://image.thum.io/get/width/640/crop/350/https://www.bioailab.org/arcticllmworkshop2023" alt="Arctic LLM Workshop website preview" loading="lazy">
    </div>
    <div class="ev-body">
      <div class="ev-badges">
        <span class="ev-badge ev-badge-organizer"><i class="fa-solid fa-person-chalkboard fa-xs"></i> Organizer &amp; Moderator</span>
        <span class="ev-badge ev-badge-workshop">Workshop</span>
        <span class="ev-badge ev-badge-past">Past</span>
      </div>
      <div class="ev-title">Large Language Model Workshop</div>
      <div class="ev-meta">
        <span><i class="fa-solid fa-calendar-days fa-xs"></i> Oct 27–28, 2023</span>
        <span><i class="fa-solid fa-location-dot fa-xs"></i> Tromsø, Norway · UiT</span>
      </div>
      <p class="ev-desc">A two-day workshop co-organized by Bio-AI Lab, NORA, and DLN — bringing together researchers from across Norway to explore in-context learning, fine-tuning, RLHF, and the future of large language models.</p>
      <div class="ev-topics">
        <span class="ev-topic">Large Language Models</span>
        <span class="ev-topic">In-context Learning</span>
        <span class="ev-topic">RLHF</span>
        <span class="ev-topic">Fine-tuning</span>
      </div>
      <a href="https://www.bioailab.org/arcticllmworkshop2023" target="_blank" rel="noopener noreferrer" class="ev-link">
        <i class="fa-solid fa-arrow-up-right-from-square fa-xs"></i> Visit Website
      </a>
    </div>
  </div>

</div>

<!-- ── Other Events ────────────────────────────────────────────────────── -->
<p class="ev-section-title"><i class="fa-solid fa-calendar fa-xs"></i> Other Events</p>

<ul class="ev-mini-list">
  <li class="ev-mini-item">
    <span class="ev-mini-year">2025</span>
    <div class="ev-mini-body">
      <strong>Volunteer</strong> &mdash; <a href="https://drive.google.com/file/d/1qT49D-iKS5w3H2Cc-JT9MPEgszaPlNpn/view?usp=sharing" target="_blank">IEEE CCGrid 2025</a> Conference
    </div>
  </li>
  <li class="ev-mini-item">
    <span class="ev-mini-year">2024</span>
    <div class="ev-mini-body">
      <strong>Organizer</strong> &mdash; Panel Discussion <em>&ldquo;Bridging the Gap: Expectations and Realities in Supervision&rdquo;</em> &mdash; <a href="https://drive.google.com/file/d/1reNTLM8_pMOwruo4XCQ0Jt-oDDrF8Egn/view?usp=sharing" target="_blank">DLN Conference 2024</a>, Oct 15, 2024
    </div>
  </li>
  <li class="ev-mini-item">
    <span class="ev-mini-year">2024</span>
    <div class="ev-mini-body">
      <strong>Organizer</strong> &mdash; <em>&ldquo;Navigating the Future: Strategic Career Planning for Young Researchers&rdquo;</em>, Tromsø &mdash; Sep 13, 2024
    </div>
  </li>
</ul>
