---
layout: page
title: Contact Us
description: Get a quote for SEO, a new website, or ongoing maintenance.
permalink: /contact/
---

<div class="contact-wrap">
  <!-- your existing HTML stays exactly the same -->
  <div class="contact-intro">
    <p>
      Looking to improve your search rankings, website performance, or online visibility?
      Send a message below and we'll reply within 1–2 business days.
    </p>

    <p class="contact-note">
      Fields marked <span class="required" aria-hidden="true">*</span>
      <span class="sr-only">are required</span>.
    </p>
  </div>

  <form id="contact-form" action="https://formspree.io/f/mykgqeew" method="POST" class="contact-form" novalidate>
    <!-- your existing form fields stay exactly the same -->
    <div class="form-row">
      <div class="form-group">
        <label for="name">
          Name <span class="required" aria-hidden="true">*</span>
          <span class="sr-only">required</span>
        </label>
        <input type="text" id="name" name="name" autocomplete="name" required>
      </div>
      <div class="form-group">
        <label for="email">
          Email <span class="required" aria-hidden="true">*</span>
          <span class="sr-only">required</span>
        </label>
        <input type="email" id="email" name="_replyto" autocomplete="email" required>
      </div>
    </div>

    <div class="form-group">
      <label for="contact-method">Preferred contact method</label>
      <select id="contact-method" name="contact_method">
        <option value="email">Email</option>
        <option value="whatsapp">WhatsApp</option>
        <option value="instagram">Instagram</option>
        <option value="tiktok">TikTok</option>
      </select>
    </div>

    <div class="form-group">
      <label for="message">
        Message <span class="required" aria-hidden="true">*</span>
        <span class="sr-only">required</span>
      </label>
      <textarea id="message" name="message" rows="7" required></textarea>
    </div>

    <input type="hidden" name="_subject" value="New contact from ebiya.sg">
    <input type="text" name="_gotcha" style="display:none">

    <div class="form-actions">
      <button type="submit" class="submit-btn">Send message</button>
      <div id="form-status" class="form-status" role="status" aria-live="polite"></div>
    </div>
  </form>
</div>

<style>
/* Your existing styles + NEW BUTTON STYLES at the end */

/* ... [keep all your existing .contact-wrap through .sr-only styles unchanged] ... */

/* NEW: Neon pink submit button matching your theme vars */
.contact-form .submit-btn {
  padding: 0.9rem 2rem;
  border: 2px solid var(--primary, #FF10F0);  /* Your neon pink */
  border-radius: 999px;
  background: transparent;
  color: var(--primary, #FF10F0);
  font-weight: 700;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.contact-form .submit-btn:hover:not(:disabled) {
  background: var(--primary, #FF10F0);
  color: var(--dark1, #0a0a0a);
  box-shadow: 
    0 0 20px var(--primary, #FF10F0),
    0 0 40px var(--secondary, #FF006E);
  transform: translateY(-2px);
}

.contact-form .submit-btn:active {
  transform: translateY(0);
}

.contact-form .submit-btn[disabled] {
  opacity: 0.5;
  cursor: not-allowed;
  box-shadow: none;
}

/* UPDATED: Center button */
.contact-form .form-actions {
  display: flex;
  justify-content: center;  /* NEW: Centers button */
  align-items: center;
  gap: 0.75rem;
  margin-top: 1rem;
}

/* Your existing script stays exactly the same */
</style>

<script>
/* Your existing script stays exactly the same */
(function () {
  // ... unchanged
})();
</script>
