---
title: Buckingham Old Gaol Audio Library
layout: audio
---
<div class="row">
        <h1>The Buckingham Old Gaol Audio Guide</h1>
</div>
<div class="row">
{% for item in site.data.recordings %}
{% if item[1].series == "audio_guide" %}
    <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12" >
        <div class="card" id="{{ item[0] }}" style="margin-bottom:5px">
            <img src="{{ item[1].image }}" class="card-img" alt="{{ item[1].heading }}">
            <h3 class="card-title" >{{ item[1].heading }}</h3>
            <p class="card-text" >{{ item[1].about }}</p>
            <audio controls>
                <source src="{{ site.baseurl }}{{ item[1].filepath }}" type="audio/mpeg">
                    Your browser does not support the audio element.
            </audio>
        </div>
    </div>
{% endif %}
{% endfor %}
</div>
<hr>
<div class="row">
        <h1>Flora Thompson at 150</h1>
</div>
<div class="row">
{% for item in site.data.recordings %}
{% if item[1].series == "flora" %}
    <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12" >
        <div class="card" id="{{ item[0] }}" style="margin-bottom:5px">
            <img src="{{ item[1].image }}" class="card-img" alt="{{ item[1].heading }}">
            <h3 class="card-title" >{{ item[1].heading }}</h3>
            <p class="card-text" >{{ item[1].about }}</p>
            <audio controls>
                <source src="{{ site.baseurl }}{{ item[1].filepath }}" type="audio/mpeg">
                    Your browser does not support the audio element.
            </audio>
        </div>
    </div>
{% endif %}
{% endfor %}
</div>