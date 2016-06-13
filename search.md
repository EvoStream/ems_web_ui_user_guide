---
layout: page
title: Search Web UI User Guide
permalink: /search/
---

<p>Enter a search string then press Enter or click Search</p>

<script>
function googleSearch() {
  var searchString = document.getElementById("searchString").value;
  var prefix = "https://www.google.com/search?q=";
  var suffix = "%20site:docs.evostream.com/ems_web_ui_user_guide";
  searchURL = prefix + encodeURI(searchString) + suffix;
  window.open(searchURL);
}
</script>

<form onChange="googleSearch()">
  <input type="text" id="searchString" size="50"><br><br>
  <input type="button" onClick="googleSearch()" value="Search"><br>
</form> 
