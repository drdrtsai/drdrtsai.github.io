---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<style>
  .pub-nav { font-size: 0.9rem; margin-bottom: 0.5rem; }
  .pub-nav .sep { color: #999; margin: 0 0.35rem; }
  .publications h2.bibliography { color: #555; margin-top: 1.5rem; scroll-margin-top: 4.5rem; }
  html[data-theme="dark"] .publications h2.bibliography { color: #bbb; }
  .publications ol.bibliography li { margin-bottom: 0.9rem; }
  .publications .title, .publications .author, .publications .periodical { margin-bottom: 0; }
  .publications .pub-meta { display: flex; flex-wrap: wrap; align-items: center; gap: 0.25rem 0.75rem; margin-top: 0.2rem; }
  .publications .pub-meta .links { display: flex; flex-wrap: wrap; align-items: center; gap: 0.3rem; margin: 0; padding: 0; }
  .publications .pub-meta .links a.btn { margin: 0; padding: 0 0.4rem; font-size: 0.7rem; line-height: 1.5; }
  .publications .pub-meta .badges { display: inline-flex; align-items: center; gap: 0.4rem; margin: 0; padding: 0; }
  .publications .pub-meta .badges > span { margin: 0 !important; line-height: 1; }
  .publications .preprint { font-size: 0.9rem; margin-top: 0.3rem; }
</style>

<p class="pub-nav">
  <a href="#stigma">Stigma and discrimination</a><span class="sep">|</span>
  <a href="#syndemics">Syndemics</a><span class="sep">|</span>
  <a href="#precarity">Precarity</a><span class="sep">|</span>
  <a href="#networks">Social networks</a><span class="sep">|</span>
  <a href="#policy">Policy</a><span class="sep">|</span>
  <a href="#violence">Violence and adversity</a><span class="sep">|</span>
  <a href="#ethics">Ethics</a>
</p>


<div class="publications">

<h2 class="bibliography" id="stigma">1. Stigma and discrimination</h2>
{% bibliography --query @*[topic=stigma] %}

<h2 class="bibliography" id="syndemics">2. Syndemics</h2>
{% bibliography --query @*[topic=syndemics] %}

<h2 class="bibliography" id="precarity">3. Precarity</h2>
{% bibliography --query @*[topic=precarity] %}

<h2 class="bibliography" id="networks">4. Social networks, social integration, and social norms</h2>
{% bibliography --query @*[topic=networks] %}

<h2 class="bibliography" id="policy">5. Health, economic, and social policy</h2>
{% bibliography --query @*[topic=policy] %}

<h2 class="bibliography" id="violence">6. Violence and adversity</h2>
{% bibliography --query @*[topic=violence] %}

<h2 class="bibliography" id="ethics">7. Ethics and scientific integrity</h2>
{% bibliography --query @*[topic=ethics] %}

</div>
