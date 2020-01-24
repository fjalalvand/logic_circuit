---
layout: page
title: Assignments
permalink: /assignments/
---
* [LCD-HW1](/static_files/Final/syllabus/LCD-HW1.pdf)
* [LCD-HW2](/static_files/Final/syllabus/LCD-HW2.pdf)
* [LCD-HW3](/static_files/Final/syllabus/LCD-HW3.pdf)
* [LCD-HW4](/static_files/Final/syllabus/LCD-HW4.pdf)
* [LCD-HW5](/static_files/Final/syllabus/LCD-HW5.pdf)
* [LCD-HW6](/static_files/Final/syllabus/LCD-HW6.pdf)
* [LCD-HW7](/static_files/Final/syllabus/LCD-HW7.pdf)
* [LCD-HW8](/static_files/Final/syllabus/LCD-HW8.pdf)
<ul id="archive">
{% for asg in site.assignments reversed %}
      <li class="archiveposturl" style="background: transparent">
        <span><a href="{{ asg.url | prepend: site.baseurl}}">{{ asg.title }}</a></span>
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif; float:right">
<a title="Download problems (pdf)" href="{{ asg.pdf | prepend: site.baseurl }}"><i class="fas fa-file-pdf"></i></a> 
{% if asg.attachment %}
&nbsp; <a title="Download attachments (zip)" href="{{ asg.attachment | prepend: site.baseurl }}"><i class="fas fa-file-archive"></i></a>
{% endif %}
</strong> 
      </li>
{% endfor %}
</ul>




