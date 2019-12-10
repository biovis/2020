---
layout: map_page
logo: ieee.svg
title: BioVis at IEEE VIS (BioVis@VIS)
location: Salt Lake City, USA
date: October 2020
main_venue_rln: In conjunction
main_venue: IEEE VIS 2020
main_venue_url: http://ieeevis.org/
permalink: /ieeevis/
---

<!--<br>
<div style="background-color: #f2f2f2; border-style: solid; border-color: #009e9d; padding: 5px;">
Biovis@VIS will be held during the main IEEE VIS 2019 program on Thursday October 24th, 2019, over two consecutive sessions: 9:00AM to 10:30 AM and again from 10:50 AM to 12:20 PM.
</div>-->

<div class="row center-align">

    <div class="col m6 s12 event-page-menu-block">
        <i class="material-icons large">create</i>
        <h3>BioVis Challenges</h3>
        <a class="btn waves-effect waves-light disabled" href="{{site.baseurl}}/biovisChallenges_vis" type="submit" name="action">View Details</a>
    </div>

    <div class="col m6 s12 event-page-menu-block">
        <i class="material-icons large">list</i>
        <h3>Program</h3>
        <a class="btn waves-effect waves-light disabled" href="{{site.baseurl}}/program_ieee" type="submit" name="action">View Details</a>
    </div>
</div>

<br/>
<br/>

<div class="row left-align">
    <div class="col s12 m6">
        <h4>Important Dates</h4>
        <p>Workshop date: {{@site.IEEEconferencedate}}</p>
    </div>

    <div class="col s12 m6">
        <h4>Latest News</h4>
        <ul class="post-list">
         {% for post in site.posts %}
           {% capture category %}{{post.event}}{% endcapture %}
            {% if category == "ieee" %}
            <li class="post-list-item-event">
               <span class="date">{{ post.date | date: "%-d %b %Y" }}</span>
               <span class="post-list-title">
                 <a class="post-list-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
               </span>
               <p class="post-list-excerpt">
                 {{ post.excerpt }}
               </p>              
             </li>
            {% endif %}
           {% endfor %}
         </ul>
    </div>
</div>
