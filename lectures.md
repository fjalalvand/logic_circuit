---
layout: page
title: Lectures
permalink: /lectures/
---
* [0-LCD](/static_files/Final/LCD-SLIDES/0-LCD.pdf)
* [1-BasicConcepts](/static_files/Final/LCD-SLIDES/1-BasicConcepts.pdf)
* [2-NumberSys](/static_files/Final/LCD-SLIDES/2-NumberSys.pdf)
* [3-1-NumberSys-Arithmetic-Add](/static_files/Final/LCD-SLIDES/3-1-NumberSys-Arithmetic-Add.pdf)
* [3-1-NumberSys-Arithmetic-Add](/static_files/Final/LCD-SLIDES/3-1-NumberSys-Arithmetic-Add.pdf)
* [3-1-NumberSys-Arithmetic-Add](/static_files/Final/LCD-SLIDES/3-1-NumberSys-Arithmetic-Add.pdf)
* [4-NumberSys-sign](/static_files/Final/LCD-SLIDES/4-NumberSys-sign.pdf)
* [5-1-NumberSys-carry](/static_files/Final/LCD-SLIDES/5-1-NumberSys-carry.pdf)
* [c5-2-NumberSys-codes](/static_files/Final/LCD-SLIDES/5-2-NumberSys-codes.pdf)
* [6-Algebra](/static_files/Final/LCD-SLIDES/6-Algebra.pdf)
* [7-switching](/static_files/Final/LCD-SLIDES/7-switching.pdf)
* [8-logicGates](/static_files/Final/LCD-SLIDES/8-logicGates.pdf)
* [910-opt-k-map](/static_files/Final/LCD-SLIDES/c10-opt-k-map.pdf)
* [11-opt-QMcCluskey](/static_files/Final/LCD-SLIDES/11-opt-QMcCluskey.pdf)
* [12-Hazard](/static_files/Final/LCD-SLIDES/12-Hazard.pdf)
* [13-CombinationalLogic](/static_files/Final/LCD-SLIDES/13-CombinationalLogic.pdf)
* [14-Encoder](/static_files/Final/LCD-SLIDES/14-Encoder.pdf)
* [15-Mux](/static_files/Final/LCD-SLIDES/15-Mux.pdf)
* [16-Adders](/static_files/Final/LCD-SLIDES/16-Adders.pdf)
* [17-Comparator](/static_files/Final/LCD-SLIDES/17-Comparator.pdf)
* [18-SequentialIntro](/static_files/Final/LCD-SLIDES/18-SequentialIntro.pdf)
* [19-FFs](/static_files/Final/LCD-SLIDES/19-FFs.pdf)
* [20-LD-SL-Register](/static_files/Final/LCD-SLIDES/20-LD-SL-Register.pdf)
* [21-LD-SL-Analysis & modeling](/static_files/Final/LCD-SLIDES/21-LD-SL-Analysis & modeling.pdf)
* [22-LD-SL-Synthesis](/static_files/Final/LCD-SLIDES/22-LD-SL-Synthesis.pdf)
* [23-LD-SL-Counters](/static_files/Final/LCD-SLIDES/23-LD-SL-Counters.pdf)
* [24-LD-SL-Simplification](/static_files/Final/LCD-SLIDES/24-LD-SL-Simplification.pdf)
* [25-LD-SL-Simplification-Incomplete](/static_files/Final/LCD-SLIDES/25-LD-SL-Simplification-Incomplete.pdf)
* [26-LD-PLD.pdf](/static_files/Final/LCD-SLIDES/26-LD-PLD.pdf)
<ul id="archive">
{% for lecture in site.lectures reversed %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if lecture.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ lecture.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ lecture.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="
            {% if lecture.slides contains '://' %}
              {{ lecture.slides }} 
            {% else %}
              {{ lecture.slides | prepend: site.baseurl }} 
            {% endif %}">{{ lecture.title }}</a>
        </span><br>

        {% if lecture.tldr %}
            <strong>tl;dr:</strong> 
            {{ lecture.tldr }}
            <br/>
        {% endif %}

        <strong>
            {% include lecture_links.html lecture=lecture %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>