---
layout: page
title: Spreadsheets
permalink: /spreadsheets/
---

<style>
/* HTML for tabs */
/* code from or modified from https://www.w3schools.com/w3css/w3css_tabulators.asp */
.w3-animate-opacity{animation:opac 0.8s}@keyframes opac{from{opacity:0} to{opacity:1}}

.w3-bar{width:100%;overflow:hidden}.w3-center .w3-bar{display:inline-block;width:auto}
.w3-bar .w3-bar-item {
	float:left;width:25%;border:none;display:block;outline:0;font-weight:bold;
}
.w3-white {
	background-color:white;
	color:#dc7e8e;
}
.w3-button {
	padding:5px;
}
.w3-pink {
	background-color:#dc7e8e;
}


tab {
	background-color:#dc7e8e;
	color:white;
	font-size:10px;
	text-align: center;
	display:inline-block;
}

tab:hover {
	background-color:gray;
	color:white;
}
</style>

In this section you can search and download the spreadsheets I have set in order to develop the networks visualisations. For each network, you will find a spreadsheet containing the nodes (people) and one containing the edges (relationships).


You will also find a masterlist containing all the people involved in my spreadsheets and the [relational database](https://en.wikipedia.org/wiki/Relational_database) I have developed in order to track the spread of heresy in sixteenth-century Venice and its geographial distribution. I started by considering several Inquisition trials of heretical physicians, and I have progressively involved other people's trials (thanks to the generous collaboration of some colleagues and friends who shared their information with me). In this database, I collect information on the people involved in the trials; places mentioned as venues of heretical meetings; heretical books and heretical activities cultivated by them; etc (more in [the documentation file](/documentation/)). 


What you see in these spreadsheets is a work in progress, which requires additional archive research and that I continuosly update and revise. So please be aware of that. Moreover, please be aware that early modern sources are often incomplete and fragmented, so in some cases I had to somewhat approximate the information (see the documentation file).


Click on the tabs below to access the spreadsheets.


{% assign sections = site.data.tablesdl %}
<p>
	<div class="w3-bar w3-pink">
{% for section in sections %}
  <tab class="w3-bar-item w3-button tablink{% if section.tablink %} w3-white{% endif %}" onclick="openCity(event,'{{ section.title }}')">{{ section.title }}</tab>
{% endfor %}
</div>
</p>
{% for section in sections %}

<div id="{{ section.title }}" class="city w3-animate-opacity" style="display:{{ section.display }}">
{% if section.title %}
<h5 align="center">{% if section.visualisation %}<a href="{{ section.visualisation }}">{% endif %}{{ section.title }}{% if section.visualisation %}</a>{% endif %}</h5>


{% if section.google-id %}
<p align="center">{% if section.masterlist %}<button class="btn btn-sm"><a download href="https://docs.google.com/spreadsheets/d/{{ section.google-id }}/export?format=csv&gid={{ section.gid }}"><i class="fa fa-download"></i> CSV Download {{ section.title }}</a></button> <button class="btn btn-sm"><a download href="https://docs.google.com/spreadsheets/d/{{ section.google-id }}/export?format=xlsx&gid={{ section.gid }}"><i class="fa fa-download"></i> Excel Download {{ section.title }}</a></button></p> {% else %}<button class="btn btn-sm"><a download href="https://docs.google.com/spreadsheets/d/{{ section.google-id }}/export?format=xlsx"><i class="fa fa-download"></i> Excel Download {{ section.title }}</a></button></p>{% endif %}{% endif %}
{% endif %}

{% if section.tables %}
{% for table in section.tables %}

{% if table.name %}<p>{% if section.prefix %}{{ section.prefix }}{% endif %}{{ table.name }}
</p>
{% endif %}

{% if section.google-id %}<p>
<button class="btn btn-sm"><a download href="https://docs.google.com/spreadsheets/d/{{ section.google-id }}/gviz/tq?tqx=out:csv&sheet={{ table.name }}"><i class="fa fa-download"></i> CSV Download {{ table.name }}</a></button> <button class="btn btn-sm"><a download href="https://docs.google.com/spreadsheets/d/{{ section.google-id }}/export?format=xlsx&gid={{ table.gid }}"><i class="fa fa-download"></i> Excel Download {{ table.name }}</a></button></p>

{% endif %}
{% endfor %}
{% endif %}
</div>
{% endfor %}

<script>
	// javascript for tabs
	// code modified from https://www.w3schools.com/w3css/w3css_tabulators.asp
function openCity(evt, cityName) {
  var i, x, tablinks;
  x = document.getElementsByClassName("city");
  for (i = 0; i < x.length; i++) {
      x[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablink");
  for (i = 0; i < x.length; i++) {
      tablinks[i].className = tablinks[i].className.replace(" w3-white", "");
  }
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " w3-white";
}
</script>