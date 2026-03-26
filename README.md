<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tushar Mahajan</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --cream: #F4F1EC;
  --paper: #FAFAF8;
  --white: #ffffff;
  --ink: #17161B;
  --ink-2: #38353F;
  --ink-3: #68656E;
  --ink-4: #9E9CA2;
  --border: #E0DCE8;
  --border-light: #ECEAF2;
  --indigo: #2A2A4A;
  --indigo-light: #EEEEF8;
  --gold: #7A5C2E;
  --gold-light: #F5EDDB;
  --serif: 'Cormorant Garamond', Georgia, serif;
  --sans: 'DM Sans', system-ui, sans-serif;
}

html { scroll-behavior: smooth; }

body {
  font-family: var(--sans);
  background: var(--paper);
  color: var(--ink);
  font-size: 15px;
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

/* NAV */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  background: rgba(250,250,248,0.92);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-light);
  padding: 0 40px;
  height: 56px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-family: var(--serif);
  font-size: 18px;
  font-weight: 400;
  color: var(--ink);
  letter-spacing: 0.01em;
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 32px;
  list-style: none;
}

.nav-links a {
  font-size: 12px;
  font-weight: 400;
  color: var(--ink-3);
  text-decoration: none;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: color 0.2s;
}

.nav-links a:hover { color: var(--ink); }

/* LAYOUT */
.container { max-width: 1080px; margin: 0 auto; padding: 0 40px; }

/* HERO */
.hero {
  padding: 140px 0 100px;
  background: var(--paper);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0; right: 0;
  width: 500px; height: 500px;
  background: radial-gradient(circle at 70% 30%, rgba(42,42,74,0.04) 0%, transparent 70%);
  pointer-events: none;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1fr 200px;
  gap: 80px;
  align-items: start;
}

.hero-eyebrow {
  font-size: 11px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--gold);
  font-weight: 500;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.hero-eyebrow::before {
  content: '';
  width: 24px; height: 1px;
  background: var(--gold);
  flex-shrink: 0;
}

.hero h1 {
  font-family: var(--serif);
  font-size: clamp(52px, 7vw, 80px);
  font-weight: 300;
  line-height: 0.95;
  color: var(--ink);
  letter-spacing: -0.02em;
  margin-bottom: 28px;
}

.hero h1 em {
  font-style: italic;
  color: var(--ink-2);
}

.hero-title {
  font-size: 11.5px;
  color: var(--ink-3);
  letter-spacing: 0.12em;
  margin-bottom: 28px;
  font-weight: 400;
  text-transform: uppercase;
}

.hero-summary {
  font-size: 16px;
  line-height: 1.75;
  color: var(--ink-2);
  max-width: 560px;
  margin-bottom: 36px;
  font-weight: 300;
}

.hero-contacts {
  display: flex;
  flex-wrap: wrap;
  gap: 6px 20px;
}

.hero-contact {
  font-size: 12px;
  color: var(--ink-3);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 6px;
  transition: color 0.2s;
}

.hero-contact:hover { color: var(--ink); }

.hero-contact::before {
  content: '';
  width: 3px; height: 3px;
  border-radius: 50%;
  background: var(--gold);
  flex-shrink: 0;
}

.hero-photo-wrap {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 20px;
  padding-top: 10px;
}

.hero-avatar {
  width: 160px;
  height: 160px;
  border-radius: 4px;
  background: var(--indigo);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--serif);
  font-size: 52px;
  font-weight: 300;
  color: rgba(255,255,255,0.6);
  letter-spacing: -0.02em;
  font-style: italic;
}

.hero-location {
  font-size: 11px;
  color: var(--ink-4);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  text-align: right;
  line-height: 1.6;
}

/* METRICS */
.metrics-band {
  background: var(--indigo);
  padding: 40px 0;
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 0;
}

.metric {
  padding: 0 24px;
  border-right: 1px solid rgba(255,255,255,0.08);
  text-align: center;
}

.metric:first-child { padding-left: 0; text-align: left; }
.metric:last-child { border-right: none; }

.metric-num {
  font-family: var(--serif);
  font-size: 34px;
  font-weight: 300;
  color: #ffffff;
  line-height: 1;
  margin-bottom: 6px;
}

.metric-label {
  font-size: 9.5px;
  color: rgba(255,255,255,0.4);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  line-height: 1.4;
}

/* SECTIONS */
section { padding: 96px 0; }
section + section { border-top: 1px solid var(--border-light); }

.section-header {
  display: flex;
  align-items: baseline;
  gap: 16px;
  margin-bottom: 56px;
}

.section-label {
  font-size: 10px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--gold);
  font-weight: 500;
  white-space: nowrap;
}

.section-rule {
  flex: 1;
  height: 1px;
  background: var(--border);
}

/* EXPERIENCE */
.exp-item {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 0;
  margin-bottom: 56px;
  padding-bottom: 56px;
  border-bottom: 1px solid var(--border-light);
}

.exp-item:last-child {
  border-bottom: none;
  margin-bottom: 0;
  padding-bottom: 0;
}

.exp-meta {
  padding-right: 36px;
  padding-top: 4px;
}

.exp-company {
  font-family: var(--serif);
  font-size: 20px;
  font-weight: 400;
  color: var(--ink);
  margin-bottom: 4px;
  letter-spacing: -0.01em;
}

.exp-role {
  font-size: 11.5px;
  font-weight: 500;
  color: var(--ink-2);
  margin-bottom: 4px;
  text-transform: uppercase;
  letter-spacing: 0.06em;
}

.exp-period {
  font-size: 11.5px;
  color: var(--ink-4);
  margin-bottom: 8px;
  line-height: 1.5;
}

.exp-badge {
  display: inline-block;
  font-size: 9.5px;
  padding: 3px 8px;
  border-radius: 2px;
  font-weight: 500;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.badge-current {
  background: var(--gold-light);
  color: var(--gold);
}

.badge-founding {
  background: var(--indigo-light);
  color: var(--indigo);
}

.exp-content { padding-top: 2px; }

.exp-tagline {
  font-size: 12.5px;
  color: var(--ink-4);
  margin-bottom: 16px;
  font-style: italic;
}

.exp-bullets { list-style: none; }

.exp-bullets li {
  font-size: 13.5px;
  color: var(--ink-2);
  line-height: 1.65;
  padding: 4px 0 4px 18px;
  position: relative;
  font-weight: 300;
}

.exp-bullets li::before {
  content: '';
  position: absolute;
  left: 0; top: 13px;
  width: 5px; height: 1px;
  background: var(--border);
}

.exp-bullets li strong {
  color: var(--ink);
  font-weight: 500;
}

/* PROFILE */
#profile { background: var(--cream); }

.profile-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 48px;
}

.profile-col-label {
  font-size: 10px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--gold);
  font-weight: 500;
  margin-bottom: 24px;
  padding-bottom: 12px;
  border-bottom: 1px solid var(--border);
}

/* Education */
.edu-item {
  padding: 14px 0;
  border-bottom: 1px solid var(--border-light);
}

.edu-item:last-child { border-bottom: none; }

.edu-degree {
  font-family: var(--serif);
  font-size: 16px;
  font-weight: 400;
  color: var(--ink);
  margin-bottom: 2px;
}

.edu-school {
  font-size: 12.5px;
  color: var(--ink-2);
}

.edu-year {
  font-size: 11px;
  color: var(--ink-4);
}

.edu-note {
  font-size: 11px;
  color: var(--gold);
  margin-top: 3px;
  font-style: italic;
}

/* Expertise */
.expertise-item {
  padding: 14px 0;
  border-bottom: 1px solid var(--border-light);
}

.expertise-item:last-child { border-bottom: none; }

.expertise-name {
  font-size: 13px;
  font-weight: 500;
  color: var(--ink);
  margin-bottom: 2px;
}

.expertise-desc {
  font-size: 11.5px;
  color: var(--ink-4);
}

/* Skills */
.skill-group { margin-bottom: 20px; }

.skill-group-label {
  font-size: 9.5px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--ink-4);
  margin-bottom: 8px;
  font-weight: 500;
}

.skill-pills {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.skill-pill {
  font-size: 11px;
  color: var(--ink-2);
  background: var(--white);
  border: 1px solid var(--border);
  padding: 3px 10px;
  border-radius: 2px;
  transition: border-color 0.2s, color 0.2s;
}

.skill-pill:hover {
  border-color: var(--indigo);
  color: var(--indigo);
}

/* FOOTER */
footer {
  background: var(--ink);
  padding: 48px 0;
}

.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-name {
  font-family: var(--serif);
  font-size: 22px;
  font-weight: 300;
  color: rgba(255,255,255,0.8);
  letter-spacing: -0.01em;
}

.footer-contacts {
  display: flex;
  gap: 24px;
}

.footer-contact {
  font-size: 12px;
  color: rgba(255,255,255,0.4);
  text-decoration: none;
  letter-spacing: 0.04em;
  transition: color 0.2s;
}

.footer-contact:hover { color: rgba(255,255,255,0.8); }

.footer-copy {
  font-size: 11px;
  color: rgba(255,255,255,0.25);
  letter-spacing: 0.06em;
}

/* REVEAL */
.reveal {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* MOBILE */
@media (max-width: 768px) {
  nav { padding: 0 20px; }
  .nav-links { display: none; }
  .container { padding: 0 24px; }
  .hero { padding: 100px 0 64px; }
  .hero-grid { grid-template-columns: 1fr; gap: 40px; }
  .hero-photo-wrap { flex-direction: row; align-items: center; }
  .hero-avatar { width: 90px; height: 90px; font-size: 32px; }
  .hero h1 { font-size: 48px; }
  .metrics-grid { grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .metric { border-right: none; padding: 0; text-align: left; }
  section { padding: 64px 0; }
  .exp-item { grid-template-columns: 1fr; gap: 12px; }
  .exp-meta { padding-right: 0; }
  .profile-grid { grid-template-columns: 1fr; gap: 40px; }
  .footer-inner { flex-direction: column; gap: 20px; text-align: center; }
  .footer-contacts { flex-direction: column; gap: 8px; align-items: center; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">TM</a>
  <ul class="nav-links">
    <li><a href="#experience">Experience</a></li>
    <li><a href="#profile">Profile</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="top">
  <div class="container">
    <div class="hero-grid">
      <div class="hero-text reveal">
        <div class="hero-eyebrow">Institutional Markets Leader</div>
        <h1>Tushar<br><em>Mahajan</em></h1>
        <p class="hero-title">Equities &nbsp;&middot;&nbsp; Derivatives &nbsp;&middot;&nbsp; Capital Markets</p>
        <p class="hero-summary">Senior capital markets leader with 20+ years building and scaling institutional equities, derivatives, and prime services businesses across top-tier global financial firms. Track record of growing P&amp;L from ground up, leading high-performance trading teams, and driving product innovation in complex derivatives and structured products across India and global markets.</p>
        <div class="hero-contacts">
          <a href="mailto:tushar.mahajan@gmail.com" class="hero-contact">tushar.mahajan@gmail.com</a>
          <a href="tel:+919324854020" class="hero-contact">+91 93248 54020</a>
          <a href="https://linkedin.com/in/tushar-mahajan-113519" target="_blank" class="hero-contact">linkedin.com/in/tushar-mahajan</a>
          <span class="hero-contact">Mumbai, India</span>
        </div>
      </div>
      <div class="hero-photo-wrap reveal" style="transition-delay:0.15s">
        <div class="hero-avatar">TM</div>
        <div class="hero-location">Mumbai<br>India</div>
      </div>
    </div>
  </div>
</section>

<!-- METRICS -->
<div class="metrics-band">
  <div class="container">
    <div class="metrics-grid">
      <div class="metric reveal">
        <div class="metric-num">20+</div>
        <div class="metric-label">Years in capital markets</div>
      </div>
      <div class="metric reveal" style="transition-delay:0.05s">
        <div class="metric-num">60%</div>
        <div class="metric-label">Revenue CAGR — 3 successive years</div>
      </div>
      <div class="metric reveal" style="transition-delay:0.1s">
        <div class="metric-num">INR 7BN+</div>
        <div class="metric-label">Portfolio transactions</div>
      </div>
      <div class="metric reveal" style="transition-delay:0.15s">
        <div class="metric-num">$3–4MM</div>
        <div class="metric-label">Offshoring savings identified</div>
      </div>
      <div class="metric reveal" style="transition-delay:0.2s">
        <div class="metric-num">50+</div>
        <div class="metric-label">Team built &amp; led</div>
      </div>
    </div>
  </div>
</div>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-label">Experience</span>
      <div class="section-rule"></div>
    </div>

    <!-- Centrum Capital -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">Centrum Capital</div>
        <div class="exp-role">Head, Institutional Equities &mdash; Trading</div>
        <div class="exp-period">Nov 2018 &mdash; Present<br>Mumbai</div>
        <span class="exp-badge badge-current">Current</span>&nbsp;
        <span class="exp-badge badge-founding">Founding Member</span>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Institutional Equities &middot; Founded and scaled the business from ground up</p>
        <ul class="exp-bullets">
          <li>As <strong>founding member</strong> of the Institutional Equities team, responsible for overall scale-up and growth of the business</li>
          <li><strong>Built out the trading team from ground up</strong> — including trading technology, execution systems, risk management, and trading/quant research</li>
          <li>Actively involved in defining the strategy of the group — identifying key focus areas, senior hires, resource allocation, and profitability</li>
        </ul>
      </div>
    </div>

    <!-- Nomura -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">Nomura International</div>
        <div class="exp-role">Head, Listed Futures &amp; Options</div>
        <div class="exp-period">Feb 2010 &mdash; Nov 2018<br>8+ yrs &middot; Mumbai</div>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Prime Services &middot; India P&amp;L ownership</p>
        <ul class="exp-bullets">
          <li>As head of the desk, responsible for the <strong>overall P&amp;L of prime services business for India</strong></li>
          <li>Built out offshore derivative trading for Nomura — futures on swaps, access products, and the full <strong>Delta-1 product suite</strong></li>
          <li>Coordinated with regional sales teams and product partners to expand reach for India product and mine into existing global firm relationships for <strong>derivatives and prime services</strong></li>
        </ul>
      </div>
    </div>

    <!-- Edelweiss -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">Edelweiss Capital</div>
        <div class="exp-role">Head, Alternative Investments &amp; Derivatives</div>
        <div class="exp-period">Mar 2006 &mdash; Feb 2010<br>4 yrs &middot; Mumbai</div>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Derivatives desk &middot; P&amp;L &middot; Team of 50</p>
        <ul class="exp-bullets">
          <li>As head of the desk, responsible for overall P&amp;L, organisational development, and <strong>leading a team of 50 people</strong></li>
          <li>Managed a <strong>60% CAGR in revenues for three successive years</strong> — through client relationship management, new client development, and growing market share across institutional client categories</li>
          <li>As business head, drove key initiatives across technology, cost rationalisation, business development, and product enhancement</li>
          <li>Pioneered innovation in untapped derivatives opportunities — structured products, risk arbitrage, proprietary volatility index, mid-cap portfolio hedging</li>
        </ul>
      </div>
    </div>

    <!-- AmEx -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">American Express Financial Advisors</div>
        <div class="exp-role">Analyst, Business Analytics Group</div>
        <div class="exp-period">May 2004 &mdash; Feb 2006<br>2 yrs &middot; USA</div>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Internal Consulting &middot; Strategic transformation</p>
        <ul class="exp-bullets">
          <li>Part of AEFA's Internal Consulting Group — involved in <strong>strategic transformation initiatives</strong> across business units and staff groups</li>
          <li>Partnered with the business head of Brokerage &amp; Managed Products to identify cost savings and revenue opportunities — recommendations led to <strong>~15% positive bottom-line impact</strong></li>
          <li>Examined fund accounting processes for offshoring feasibility — developed sensitivity-analysis financial model estimating <strong>USD 3&ndash;4MM in savings</strong></li>
        </ul>
      </div>
    </div>

    <!-- ICICI Bank -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">ICICI Bank</div>
        <div class="exp-role">Assistant Manager, Credit Risk Management</div>
        <div class="exp-period">May 2003 &mdash; May 2004<br>1 yr &middot; Mumbai</div>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Credit ratings &middot; Portfolio analysis &middot; Securitisation</p>
        <ul class="exp-bullets">
          <li>Assigned credit ratings to transactions and companies across real estate, auto channel, and healthcare — total value greater than <strong>INR 5BN</strong></li>
          <li>Analysed loan portfolios for selection and pricing across three securitisation and portfolio buy-out transactions — total value greater than <strong>INR 7BN</strong></li>
        </ul>
      </div>
    </div>

    <!-- Cadbury -->
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-company">Cadbury India</div>
        <div class="exp-role">Intern, Sales &amp; Distribution</div>
        <div class="exp-period">Apr 2002 &mdash; Jun 2002<br>Mumbai</div>
      </div>
      <div class="exp-content">
        <p class="exp-tagline">Distribution strategy &middot; Channel development</p>
        <ul class="exp-bullets">
          <li>Independently managed and executed a pilot for an <strong>alternate distribution channel</strong> for low-price sugar confectionery — appointing seven new distributors across five cities in Madhya Pradesh</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- PROFILE -->
<section id="profile">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-label">Profile</span>
      <div class="section-rule"></div>
    </div>
    <div class="profile-grid">

      <!-- Col 1: Education -->
      <div class="reveal">
        <div class="profile-col-label">Education</div>
        <div class="edu-item">
          <div class="edu-degree">PGDM &mdash; Finance</div>
          <div class="edu-school">IIM Bangalore</div>
          <div class="edu-year">2001 &ndash; 2003 &middot; 3.18 / 4.00</div>
          <div class="edu-note">Specialisation: Investments, M&amp;A, Financial Derivatives</div>
        </div>
        <div class="edu-item">
          <div class="edu-degree">B.E. Engineering</div>
          <div class="edu-school">Punjab Engineering College, Chandigarh</div>
          <div class="edu-year">1997 &ndash; 2001 &middot; 72.01%</div>
          <div class="edu-note">College Colour — highest all-round student award</div>
        </div>
      </div>

      <!-- Col 2: Core Expertise -->
      <div class="reveal" style="transition-delay:0.1s">
        <div class="profile-col-label">Core Expertise</div>
        <div class="expertise-item">
          <div class="expertise-name">Institutional Equities</div>
          <div class="expertise-desc">Trading, execution &amp; team build</div>
        </div>
        <div class="expertise-item">
          <div class="expertise-name">Derivatives &amp; Structured Products</div>
          <div class="expertise-desc">Delta-1, futures, options, volatility</div>
        </div>
        <div class="expertise-item">
          <div class="expertise-name">Prime Services</div>
          <div class="expertise-desc">P&amp;L ownership &amp; client coverage</div>
        </div>
        <div class="expertise-item">
          <div class="expertise-name">Business Building</div>
          <div class="expertise-desc">0&rarr;1 desk &amp; team establishment</div>
        </div>
        <div class="expertise-item">
          <div class="expertise-name">Risk Management</div>
          <div class="expertise-desc">Systems, frameworks &amp; oversight</div>
        </div>
        <div class="expertise-item">
          <div class="expertise-name">Strategic Consulting</div>
          <div class="expertise-desc">Internal advisory &amp; transformation</div>
        </div>
      </div>

      <!-- Col 3: Skills -->
      <div class="reveal" style="transition-delay:0.2s">
        <div class="profile-col-label">Skills &amp; Domains</div>
        <div class="skill-group">
          <div class="skill-group-label">Markets</div>
          <div class="skill-pills">
            <span class="skill-pill">Equities</span>
            <span class="skill-pill">Futures &amp; Options</span>
            <span class="skill-pill">Delta-1</span>
            <span class="skill-pill">Structured Products</span>
            <span class="skill-pill">Volatility</span>
            <span class="skill-pill">Credit Risk</span>
            <span class="skill-pill">Securitisation</span>
          </div>
        </div>
        <div class="skill-group">
          <div class="skill-group-label">Business</div>
          <div class="skill-pills">
            <span class="skill-pill">P&amp;L Management</span>
            <span class="skill-pill">Team Leadership</span>
            <span class="skill-pill">Client Coverage</span>
            <span class="skill-pill">Business Development</span>
            <span class="skill-pill">Technology Build</span>
            <span class="skill-pill">Cost Optimisation</span>
          </div>
        </div>
        <div class="skill-group">
          <div class="skill-group-label">Analytics</div>
          <div class="skill-pills">
            <span class="skill-pill">Quant Research</span>
            <span class="skill-pill">Financial Modelling</span>
            <span class="skill-pill">Portfolio Analysis</span>
            <span class="skill-pill">Market Strategy</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- FOOTER -->
<footer id="contact">
  <div class="container">
    <div class="footer-inner">
      <div class="footer-name">Tushar Mahajan</div>
      <div class="footer-contacts">
        <a href="mailto:tushar.mahajan@gmail.com" class="footer-contact">tushar.mahajan@gmail.com</a>
        <a href="tel:+919324854020" class="footer-contact">+91 93248 54020</a>
        <a href="https://linkedin.com/in/tushar-mahajan-113519" target="_blank" class="footer-contact">LinkedIn</a>
      </div>
      <div class="footer-copy">Mumbai, India</div>
    </div>
  </div>
</footer>

<script>
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>

</body>
</html>
