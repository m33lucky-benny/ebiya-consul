---
layout: page
title: Contact Us
description: Get a quote for SEO, a new website, or ongoing maintenance.
permalink: /contact/
---

<div class="contact-wrap">
  <div class="contact-intro">
    <p>
      Looking to improve your search rankings, website performance, or online visibility?
      Send a message below and we’ll reply within 1–2 business days.
    </p>

    <p class="contact-note">
      Fields marked <span class="required" aria-hidden="true">*</span>
      <span class="sr-only">are required</span>.
    </p>
  </div>

  <form
    id="contact-form"
    action="https://formspree.io/f/mykgqeew"
    method="POST"
    class="contact-form"
    novalidate
  >
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
/* A small, page-native layout that won’t fight Minima too much */
.contact-wrap {
  max-width: 720px;
  margin: 0 auto;
}

.contact-intro p {
  margin: 0 0 0.75rem 0;
}

.contact-note {
  font-size: 0.95rem;
  opacity: 0.85;
}

.contact-form {
  margin-top: 1.25rem;
  padding: 1.25rem;
  border: 1px solid rgba(0,0,0,0.10);
  border-radius: 12px;
  background: rgba(0,0,0,0.02);
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.9rem;
}

@media (max-width: 720px) {
  .form-row { grid-template-columns: 1fr; }
}

.form-group {
  margin: 0 0 0.9rem 0;
}

label {
  display: block;
  font-weight: 600;
  margin: 0 0 0.35rem 0;
}

input, select, textarea {
  width: 100%;
  box-sizing: border-box;
  padding: 0.7rem 0.8rem;
  border-radius: 10px;
  border: 1px solid rgba(0,0,0,0.18);
  background: #fff;
}

input:focus, select:focus, textarea:focus {
  outline: 2px solid rgba(0,0,0,0.35);
  outline-offset: 2px;
}

.required { color: #b00020; }

.form-actions {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-top: 0.25rem;
}

.submit-btn {
  padding: 0.7rem 1rem;
  border: 1px solid rgba(0,0,0,0.2);
  border-radius: 999px;
  background: #111;
  color: #fff;
  cursor: pointer;
}

.submit-btn[disabled] {
  opacity: 0.65;
  cursor: not-allowed;
}

.form-status {
  display: none;
  padding: 0.6rem 0.75rem;
  border-radius: 10px;
  font-size: 0.95rem;
}

.form-status.success {
  display: block;
  background: rgba(0,128,0,0.10);
  border: 1px solid rgba(0,128,0,0.25);
}

.form-status.error {
  display: block;
  background: rgba(176,0,32,0.10);
  border: 1px solid rgba(176,0,32,0.25);
}

/* Screen-reader-only helper */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
</style>

<script>
(function () {
  const form = document.getElementById('contact-form');
  const statusDiv = document.getElementById('form-status');

  if (!form || !statusDiv) return;

  form.addEventListener('submit', function (e) {
    e.preventDefault();

    const formData = new FormData(form);
    const submitBtn = form.querySelector('.submit-btn');
    const originalBtnText = submitBtn.textContent;

    submitBtn.textContent = 'Sending...';
    submitBtn.disabled = true;

    statusDiv.style.display = 'none';
    statusDiv.className = 'form-status';
    statusDiv.textContent = '';

    fetch(form.action, {
      method: 'POST',
      body: formData,
      headers: { 'Accept': 'application/json' }
    })
      .then(response => {
        if (!response.ok) throw new Error('Form failed');
        return response.json();
      })
      .then(() => {
        statusDiv.className = 'form-status success';
        statusDiv.textContent = "Thank you—message received. We'll get back to you soon.";
        statusDiv.style.display = 'block';
        form.reset();
      })
      .catch(() => {
        statusDiv.className = 'form-status error';
        statusDiv.textContent =
          'Something went wrong. Please try again, or contact us via social media.';
        statusDiv.style.display = 'block';
      })
      .finally(() => {
        submitBtn.textContent = originalBtnText;
        submitBtn.disabled = false;
      });
  });
})();
</script>
