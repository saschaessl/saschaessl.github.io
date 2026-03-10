---
layout: page
title: "Research Diary"
permalink: /diary/
---

<div id="lock-screen" style="text-align:center; padding: 3rem;">
  <p>🔒 Password protected</p>
  <input type="password" id="pwd" placeholder="Enter password" 
    style="padding: 0.5rem; font-size: 1rem;" />
  <button onclick="unlock()" 
    style="padding: 0.5rem 1rem; margin-left: 0.5rem; font-size: 1rem;">Enter</button>
  <p id="error" style="color:red; display:none;">Wrong password.</p>
</div>

<div id="diary" style="display:none;">

  <h2>2026-03-10 – Erster Eintrag</h2>
  <p>Hier steht der erste Eintrag.</p>

</div>

<script>
function unlock() {
  var pwd = document.getElementById("pwd").value;
  if (pwd === "Check") {
    document.getElementById("lock-screen").style.display = "none";
    document.getElementById("diary").style.display = "block";
  } else {
    document.getElementById("error").style.display = "block";
  }
}
document.getElementById("pwd").addEventListener("keypress", function(e) {
  if (e.key === "Enter") unlock();
});
</script>
