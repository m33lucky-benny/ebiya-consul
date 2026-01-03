---
layout: page
title: Contact Us
description: Get a quote for SEO, a new website, or ongoing maintenance.
permalink: /contact/
---

<div class="contact-intro">
  <p>
    Looking to improve your search rankings, website performance, or online visibility? Get in touch using the form below or reach out via social media.

  </p>
</div>

<form
  id="contact-form"
  action="https://formspree.io/f/mykgqeew"
  method="POST"
  class="contact-form"
>
  <div class="form-group">
    <label for="name">Name <span class="required">*</span></label>
    <input type="text" id="name" name="name" required>
  </div>

  <div class="form-group">
    <label for="email">Email <span class="required">*</span></label>
    <input type="email" id="email" name="_replyto" required>
  </div>

  <div class="form-group">
    <label for="contact-method">Preferred Contact Method</label>
    <select id="contact-method" name="contact_method">
      <option value="email">Email</option>
      <option value="whatsapp">WhatsApp</option>
      <option value="instagram">Instagram</option>
      <option value="tiktok">TikTok</option>
    </select>
  </div>

  <div class="form-group">
    <label for="message">Message / Inquiry <span class="required">*</span></label>
    <textarea id="message" name="message" rows="6" required></textarea>
  </div>

  <input type="hidden" name="_subject" value="New contact from ebiya.sg">
  <input type="text" name="_gotcha" style="display:none">

  <button type="submit" class="submit-btn">Send Message</button>

  <!-- FIXED ID -->
  <div id="form-status"></div>
</form>

<style>
/* styles unchanged – safe */
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
    statusDiv.className = '';

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
        statusDiv.className = 'success';
        statusDiv.textContent = "Thank you for contacting us! We'll get back to you soon.";
        statusDiv.style.display = 'block';
        form.reset();
      })
      .catch(() => {
        statusDiv.className = 'error';
        statusDiv.textContent =
          'Oops! Something went wrong. Please try again or contact us via social media.';
        statusDiv.style.display = 'block';
      })
      .finally(() => {
        submitBtn.textContent = originalBtnText;
        submitBtn.disabled = false;
      });
  });
})();
</script>