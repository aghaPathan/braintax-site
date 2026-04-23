---
layout: page
title: TikTok OAuth Callback
permalink: /auth/tiktok/callback/
sitemap: false
robots: noindex
---

This page receives the TikTok OAuth authorization code for the BrainTax publishing tool. It is **not** a user-facing feature.

<noscript>
<p><strong>JavaScript is required to read the authorization code.</strong></p>
</noscript>

<div id="status">Reading authorization code from URL…</div>

<pre id="code-box" style="display:none;"></pre>

<p id="instructions" style="display:none;">
Copy the values above and paste them into the BrainTax publishing tool's OAuth setup prompt.
</p>

<p id="error-box" style="display:none;"></p>

<script>
(function() {
  var params = new URLSearchParams(window.location.search);
  var code = params.get('code');
  var state = params.get('state');
  var scopes = params.get('scopes');
  var error = params.get('error');
  var errorDesc = params.get('error_description');

  var statusEl = document.getElementById('status');
  var codeBox = document.getElementById('code-box');
  var instr = document.getElementById('instructions');
  var errBox = document.getElementById('error-box');

  if (error) {
    statusEl.textContent = 'TikTok returned an error:';
    errBox.style.display = 'block';
    errBox.textContent = error + (errorDesc ? ' — ' + errorDesc : '');
    return;
  }

  if (!code) {
    statusEl.textContent = 'No authorization code found in the URL.';
    return;
  }

  statusEl.textContent = 'Authorization code received. Copy these values:';
  var lines = ['code=' + code];
  if (state) lines.push('state=' + state);
  if (scopes) lines.push('scopes=' + scopes);
  codeBox.textContent = lines.join('\n');
  codeBox.style.display = 'block';
  instr.style.display = 'block';
})();
</script>
