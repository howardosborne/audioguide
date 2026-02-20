---
title: Buckingham Old Gaol Audio Library
layout: audio
---
<div class="row">
        <h2>Audio Guided Tour</h2>
</div>

{% for item in site.data.recordings %}
{% if item[1].series == "audio_guide" %}
<div class="row">
    <div class="card" id="{{ item[0] }}" style="margin-bottom:5px">
        <h5 class="card-title" >{{ item[1].heading }}</h5>
        <p class="card-text" >{{ item[1].about }}</p>
        <audio controls>
            <source src="{{ site.baseurl }}{{ item[1].filepath }}" type="audio/mpeg">
                Your browser does not support the audio element.
        </audio>
    </div>
</div>
{% endif %}
{% endfor %}

<hr>
<div class="row">
        <h2>Flora Thompson at 150</h2>
</div>

{% for item in site.data.recordings %}
{% if item[1].series == "flora" %}
<div class="row">
    <div class="card" id="{{ item[0] }}" style="margin-bottom:5px">
        <h5 class="card-title" >{{ item[1].heading }}</h5>
        <p class="card-text" >{{ item[1].about }}</p>
        <audio controls>
            <source src="{{ site.baseurl }}{{ item[1].filepath }}" type="audio/mpeg">
                Your browser does not support the audio element.
        </audio>
    </div>
</div>
{% endif %}
{% endfor %}