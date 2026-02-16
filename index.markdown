---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<div class="row">
    <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
        An audio guide for Buckingham Old Gaol
    </div>
    <div class="col-lg-8 col-md-8 col-sm-12 col-xs-12">
        <div id="map" class="col-md-12" style="height: 500px;"></div>
    </div>
</div>
<hr>
<div class="row">
{% for item in site.data.recordings %}
{% if item[1].draft == "false" %}
    <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12" >
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