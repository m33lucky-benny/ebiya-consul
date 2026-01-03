---
layout: page 
title: Website Audit & SEO Services
description: Free tools reveal your site's issues—slow speed, SEO errors, poor rankings. Get expert fixes via contact.
permalink: /services/
---

<!-- CRITICAL CSS: Fixes render blocking (750ms savings) -->
<style>
/* Body & typography basics */
* { box-sizing: border-box; margin: 0; padding: 0; }
body { 
  font-family: system-ui, -apple-system, sans-serif; 
  line-height: 1.6; 
  color: #fff; 
  background: #0a0a0a; 
}

/* Hero */
.services-hero { 
  background: #0a0a0a; 
  padding: 3rem 1rem; 
  text-align: center; 
}
h1 { 
  font-size: 2.5rem; 
  font-weight: 700; 
  margin: 0 0 1rem 0; 
  line-height: 1.2; 
}
h2 { 
  font-size: 2rem; 
  margin: 2.5rem 0 1rem 0; 
  font-weight: 600; 
}
p { 
  font-size: 1.1rem; 
  max-width: 600px; 
  margin: 0 auto 1.5rem; 
}

/* Buttons & grid - YOUR EXISTING */
.tool-grid { 
  display: grid; 
  gap: 2rem; 
  margin: 3rem auto; 
  max-width: 1200px; 
  justify-items: center; 
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); 
}
.tool-btn { 
  background: #FF10F0; 
  color: white !important; 
  padding: 1.5rem 2rem; 
  border: none; 
  border-radius: 50px; 
  font-size: 1.3rem; 
  font-weight: bold; 
  text-decoration: none; 
  display: flex; 
  flex-direction: column; 
  align-items: center; 
  justify-content: center; 
  text-align: center; 
  box-shadow: 0 8px 25px rgba(255,16,240,0.3); 
  transition: all 0.3s; 
  width: 100%; 
  height: 140px; 
  min-height: 140px; 
}
.tool-btn small { 
  font-size: 0.85rem; 
  font-weight: normal; 
  opacity: 0.9; 
  margin-top: 0.5rem; 
}
.tool-btn:hover { 
  transform: translateY(-5px); 
  box-shadow: 0 15px 40px rgba(255,16,240,0.6); 
  color: white !important; 
}

/* CTA & Sections */
.cta-section, .clients-section {
  max-width: 800px; 
  margin: 4rem auto; 
  text-align: center; 
  padding: 0 2rem; 
}
.cta-btn { 
  background: #FF10F0; 
  color: white; 
  padding: 1.5rem 3rem; 
  border: none; 
  border-radius: 50px; 
  font-size: 1.4rem; 
  cursor: pointer; 
  transition: all 0.3s; 
  display: inline-block; 
  margin: 2rem 0; 
  font-weight: bold; 
}
.cta-btn:hover { 
  box-shadow: 0 0 30px #FF10F0; 
  transform: scale(1.05); 
}
.clients-list {
  list-style: none; 
  padding: 0; 
  max-width: 600px; 
  margin: 2rem auto; 
}
.clients-list li {
  background: rgba(255,16,240,0.1); 
  margin: 1rem 0; 
  padding: 1rem 1.5rem; 
  border-radius: 10px; 
  border-left: 4px solid #FF10F0; 
}

/* Mobile */
@media (max-width: 768px) { 
  .tool-grid { grid-template-columns: 1fr; gap: 1.5rem; } 
  .tool-btn { height: 130px; padding: 1.2rem 1.5rem; font-size: 1.15rem; } 
  .cta-section, .clients-section { padding: 0 1rem; } 
  h1 { font-size: 2rem; } 
}
</style>

<!-- Your HTML unchanged -->
<div class="services-hero">...</div>
<div class="tool-grid">...</div>
<div class="cta-section">...</div>
<div class="clients-section">...</div>
