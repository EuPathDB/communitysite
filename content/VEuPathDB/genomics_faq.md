---
layout: plain
title: VEuPathDB Frequently Asked Questions
permalink: /VEuPathDB/faq
---
<style>
div.static-content li {
    font-size: 130%;
    margin: 1em 0;
    list-style: none;
}
div.static-content summary {
    color: #069;
}
</style>

<h1 id="FAQ">Frequently Asked Questions</h1>

<div class="static-content"> 

<div id="general">
  <h2>Frequently Asked Questions</h2>
  <ul>
    {% for item in site.data.genomics_faq %}
    {% if item.type == "general" %}
    <li><a name="{{ item.uid }}"></a>
      <details id="{{ item.uid }}">
        <summary>{{ item.question }}</summary>
        <p>
          {{ item.answer | markdownify }}
        </p>
      </details>
    </li>
    {% endif %}
    {% unless forloop.last %}{% endunless %}{% endfor %}
  </ul>
</div>

</div>

<script>
function getHashFromUrl(url){
    console.log("My url: ", url);
    var a = document.createElement("a");
    a.href = url;
    return a.hash.replace(/^#/, "");
}
function openEntry(myanchor) {
  console.log("My Anchor: ", myanchor);
  document.getElementById(myanchor).open = true;
}
document.onload = openEntry(getHashFromUrl(window.location.href));
</script>