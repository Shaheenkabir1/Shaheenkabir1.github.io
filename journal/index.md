---
layout: default
title: Journal
permalink: /journal/
---

<div id="lock-screen">
  <h2>🔒 Private Journal</h2>
  <p>Enter 10-digits phone number of yours:(Only You  can view this)</p>
  <input type="password" id="passcode" maxlength="10" style="font-size:1.2em; padding:8px;">
  <br><br>
  <button onclick="unlock()">Unlock</button>
  <p id="error-msg" style="color:red;"></p>
</div>

<div id="journal-content" style="display:none;">
  <h1>Daily Journal</h1>

{% for post in site.posts %}
  {% if post.categories contains "journal" %}
### {{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}
{{ post.content }}
---
  {% endif %}
{% endfor %}

</div>

<script>
function unlock() {
  const allowed = [
    "5376804605",
    "5014884191",
    "1306790639"
  ];

  const input = document.getElementById("passcode").value;
  const error = document.getElementById("error-msg");

  if (allowed.includes(input)) {
    document.getElementById("lock-screen").style.display = "none";
    document.getElementById("journal-content").style.display = "block";
  } else {
    error.innerText = "❌ Incorrect code.";
  }
}
</script>
