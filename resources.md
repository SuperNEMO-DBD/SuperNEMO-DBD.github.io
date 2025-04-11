---
layout: experiment
title: For Collaborators
---

<div class="container-fluid" id="top">
<div class="row">
<div class="col-xs-9">


<div id="intro">
    <header class="post-header">
        <h1 class="post-title text-center">For collaborators</h1>
    </header>
    
    This page is mainly for collaboration members, and provides useful resources and instructions for people working on the experiment. Some of the tools and applications listed below may require a username and password.
</div>

<div id="newsletter" style="display:none">
    <header class="post-header">
        <h1 class="post-title text-center">Newsletters</h1>
    </header>
    {% assign letters_by_date = site.newsletters | sort:"date" | reverse %}
    {% for letter in letters_by_date %}
    {% assign index = forloop.index0 %}
    {% if index == 0 %}
<div markdown="1">
## Current newsletter: {{letter.title}}
_(added on {{letter.date | date_to_long_string }})_
{{letter.text}}
</div>
{% endif %}

{% if index == 1 %}
<div markdown="1">
## Previous newsletters
</div>
{% endif %}
    {% if index > 0 %}
    <p>
    <a role="button" data-toggle="collapse" href="#{{letter.title| slugify}}" aria-expanded="false" aria-controls="{{letter.title| slugify}}">{{letter.title}}</a></p>
    {% endif %}
    <div class="collapse" id="{{letter.title| slugify}}">

<div class="well" style="overflow:auto" markdown="1">
## {{letter.title}}

_(added on {{letter.date | date_to_long_string }})_

{{letter.text}}
</div>
    </div>
    {% endfor %}
</div>




<div id="conf" style="display:none">
    <header class="post-header">
        <h1 class="post-title text-center">Upcoming conferences</h1>
    </header>
<div markdown="1">
Hello
</div>
</div>


<div id="docs" style="display:none">
    <header class="post-header">
        <h1 class="post-title text-center">Internal documentation</h1>
    </header>
<div markdown="1">

## DocDB

For technical notes etc, see [DocDB](http://nile.hep.utexas.edu/DocDB/). To set up an account:

- To sign up, click [here](http://nile.hep.utexas.edu/cgi-bin/DocDB/ut-nemo/public/signup)
- Go to the [main database link](http://nile.hep.utexas.edu/DocDB/)
- Select link _private NEMO documents_
- Use your name and password (created in step 1) to log in
- Add yourself as an author

Next time you log in you can upload documents! Just follow the active options. For security reasons, in about a week, we will certify all new user requests ~24 hrs to be able to upload docs. If you have problems, send an email message to [the administrator](mailto:docdb@hep.utexas.edu).

## SuperNEMO wiki

The [SuperNEMO wiki](https://nemo.lpc-caen.in2p3.fr/wiki) is hosted at LPC Caen and holds up-to-date information about the status of integration, committees, and analyses. You can get a login from [Yves](lemiere@lpccaen.in2p3.fr) or [Francois](mauger@lpccaen.in2p3.fr).

</div>
</div>

<div id="software" style="display:none">
    <header class="post-header">
        <h1 class="post-title text-center">Software and computing</h1>
    </header>
<div markdown="1">

Working with the SuperNEMO software
--------------------------------------------------

All software is available under {% include icon-github.html username=site.github_username %}
    
The main software package for offline work is [Falaise](https://github.com/SuperNEMO-DBD/Falaise).
A guide to installing Falaise on Linux and macOS platforms is available through the dedicated
[Homebrew package manager and repo](https://github.com/SuperNEMO-DBD/brew)
A starter guide to the core simulation, reconstruction and analysis tools available in Falaise
[can be found here](Falaise).
    
Please note that the documentation is always under development, so feature requests
or contributions are welcome. For installation related issues when using `brew`,
use the [SuperNEMO Brew Issue Tracker](https://github.com/SuperNEMO-DBD/brew/issues).
For all issues relating to using Falaise, or installing/developing it locally, [raise an issue on the
Falaise tracker](https://github.com/SuperNEMO-DBD/Falaise/issues)
</div>

                
<div markdown="1">
Getting an account on the CCLyon computing cluster
--------------------------------------------------
The CCLyon computing cluster is where our data and large simulation samples are stored. There are installations of the SuperNEMO software available on CCLyon. You'll need to get an account to use it.

To create your CC-IN2P3 user account, please follow the procedure below:

- read the [Charters for the use of resources](https://doc.cc.in2p3.fr/en/Daily-usage/access.html#charters) (the account creation or submission of a creation request implies acceptance of the charters),
- go to the [Identity Management Portal](https://id.cc.in2p3.fr/) and select the “Sign up” button,
- fill in the required information (using [eduGAIN](https://doc.cc.in2p3.fr/en/Daily-usage/account.html#identity-federation) will make this task easier) and follow the instructions you’ll receive by e-mail.

Once the account has been created, an access with the same identifier is provisioned on our [Helpdesk](https://doc.cc.in2p3.fr/en/Daily-usage/assistance.html#cc-helpdesk).


</div>

<div markdown="1">
If your CCLyon account is expiring
----------------------------------

Periodically, you will receive a notification inviting you to confirm the information associated to your profile. To extend your account activity, please follow the steps below:

- click on the link provided on the red banner in your [Identity Management Portal](https://id.cc.in2p3.fr/) profile,
- follow the procedure to verify your e-mail address and click on the link you will receive by e-mail,
- verify that the information associated with your account (if necessary, update it) and confirm that you have read the [Charters concerning the use of resources](https://doc.cc.in2p3.fr/en/Daily-usage/access.html#charters).

</div>
<div markdown="1">
CCLyon support
--------------

For any support, contact our computing tsar, <a href="mailto:lemiere@lpccaen.in2p3.fr">Yves</a>.

Useful links :
-  <https://doc.cc.in2p3.fr/en-index.html>
- <https://portail.cc.in2p3.fr>
- <https://support.cc.in2p3.fr/#login>

</div>

<div markdown="1">
Using CCLyon
-------------

[Here](https://doc.cc.in2p3.fr/en:utiliser_le_systeme_batch_ge_depuis_le_centre_de_calcul) are some instructions for logging onto CCLyon and getting started with the batch system that enables you to submit large jobs to the distributed computing cluster.

</div>
<div markdown="1">
Website development
--------------------------------------------------
This site uses [GitHub Pages](https://pages.github.com) to create a static website. It uses the following tools and techniques:
    
- [Jekyll](https://jekyllrb.com) as the site generation engine
- [GitHub Pages](https://pages.github.com) for hosting
- [GFM](https://guides.github.com/features/mastering-markdown/) and [Kramdown](https://kramdown.gettalong.org) for writing/parsing text
- [MathJax](https://www.mathjax.org) for rendering math
    
### Building locally
The website generated by Jekyll can be built and served locally to test changes without making commits upstream. Note that GitHub Pages has a soft limit of 10 rebuilds per hour. Provided you have an install of Ruby 2 or better, including the development headers and library, the workflow is:
    
```console
$ git clone https://github.com/supernemo-dbd/supernemo-dbd.github.io
$ cd supernemo-dbd.github.io
$ ./snjekyll serve
```
    
The last command will download and setup the local Jekyll instance, and start a local isolated webserver at `http://127.0.0.1:4000`. Simply point your favoured browser to this address to view the generated site.
    
The server runs in the foreground and watches the site sources for changes (for example, `index.md`). When a file changes, the server will rebuild the    site automatically, so simply refresh your browser to see the resultant    regenerated site. For example, try making some changes to `index.md`. The server may be shutdown at any point using `Ctrl-C`.
    
Further information on tasks available from `snjekyll` can be seen by running

```console
$ ./snjekyll help
```

Alternately, if you already have a custom Ruby install, e.g. with Home/Linuxbrew you can do

```console
$ git clone {{ site.github.repository_url }}
$ cd {{ site.github.repository_name }}
$ gem install bundler
$ bundle install
$ bundle exec jekyll serve
```
    
In both workflows, the `xz` package installed by Home/Linuxbrew is not compatible with the `nokogiri` gem required by Jekyll, and will cause compiliation of the gem to fail. `snjekyll` will issue a warning about this, but will not take further action. To work around this issue, either do `brew unlink xz` or remove Home/Linuxbrew settings from your environment. The latter may not be possible if you have Homebrew installed in `/usr/local`


### Can we use MathJax and $$\LaTeX$$?

MathJax can support inline math, e.g. $$ 1/x^2 $$, and block equations:

$$
e^{i\pi} + 1 = 0
$$

like the above. Numbered equations, using the AMS math environment:

$$
\begin{equation}
E = mc^2
\label{einstein}
\end{equation}
$$

This should allow a reference (see Equation $$\eqref{einstein}$$) to be inserted.


### Can we use code blocks?
Here's C++:

```cpp
#include <iostream>
  
int main() {
std::cout << "Hello World\n";
}
```
    
and some Python:
    
```python
import os
print('Hello World')
```

        
### Support or Contact
Having trouble with Pages? Check out our [documentation](https://help.github.com/pages) or [contact support](https://github.com/contact) and we’ll help you sort it out.
</div>




</div>

<div id="ops" style="display:none">
<header class="post-header">
<h1 class="post-title text-center">Operations</h1>
</header>
<div markdown="1">
Working at LSM
-------------

![The view from LSM]({{"assets/modane.jpg"| relative_url }})

As we prepare to take data, everyone is welcome and needed at [LSM](http://www.lsm.in2p3.fr). You'll also all need to come here for your first shift! Here are some hints to ensure your trip is drama-free. If you have questions travel to LSM, contact <a href="mailto:chauveau@lp2ib.in2p3.fr">Manu</a> or <a href="mailto:andrea@lapp.in2p3.fr">Andrea</a>.

### Before you travel
- Read the LSM user guide in [English](https://nile.hep.utexas.edu/DocDB/ut-nemo/docs/0059/005988/002/LSMUserGuide_v4.pdf) or [French](https://nile.hep.utexas.edu/DocDB/ut-nemo/docs/0059/005988/002/LSM_Guide_Utilisateurs_V4.pdf). This includes details of the documents that any non-CNRS users need to send to <a href="mailto:admin@lpsc.in2p3.fr">LSM admin</a>, including a scan of an ID document and a stamped and signed [employer declaration](https://nile.hep.utexas.edu/cgi-bin/DocDB/ut-nemo/private/ShowDocument?docid=5621).
- Read, sign and date the [Code of conduct](https://nile.hep.utexas.edu/DocDB/ut-nemo/docs/0059/005988/002/20240715-CodeofConduct_2024_signed.pdf%20-%20Box.pdf) and send it to <a href="mailto:scorza@lpsc.in2p3.fr">Silvia Scorza</a>
- Make sure <a href="mailto:chauveau@lp2ib.in2p3.fr">Manu</a> and <a href="mailto:andrea@lapp.in2p3.fr">Andrea</a> know when you are coming and which days you will be able to go underground **at least 1 week in advance**, so that they can add you to the LSM calendar and arrange for a driver. If you would like to eat lunch underground, let them know - but it can't be guaranteed, as it depends on driver schedules.




### Going underground
The cars going to the underground lab leave at **8:30am** each day, so be sure to arrive at the surface lab on time. If you plan to stay all day, bring your own lunch - there's a fridge, microwave, kettle and espresso machine underground, as well as clean drinking water (in bottles). You'll need an approved driver to stay with you, so if no SuperNEMO driver will stay underground, you will need to negotiate with LSM. 

If you are not eating lunch underground, you will leave for lunch on the surface by 11:30am. If returning to the tunnel for the afternoon, departure will be **1:30pm** from the surface lab.

If you're staying late, you'll need to get permission from the lab management - your driver should be able to help you. The LSM drivers normally leave the underground lab for the evening at around 4:30 or 5pm, but if you have a SuperNEMO driver, you might be able to stay later.

### Training
Before you go underground for the first time, you will need to do some basic safety training, in case there is an emergency in the tunnel. Jean-Lou of LSM leads this training, and you will be able to do it very quickly in the morning before you go underground. You will also need to receive some security paperwork. To get all of this set up, let <a href="mailto:valerie.favre@lsm.fr">Valerie Favre</a> know that you will be going underground for the first time.

### Staying in Modane
You have a few options for accommodation in Modane. The cheapest option is to stay in the LSM dorms. There are 4 rooms in the basement of the surface lab. Each one has its own shower and toilet, and there is a shared kitchen which is stocked with basic cooking equipment. The dorm rooms cost EUR19 per night. To find out about availability and book a room, contact <a href="mailto: booking- lsm@lpsc.in2p3.fr">LSM</a>. 

Alternatively, people choose to stay in Modane itself (walking distance to the lab) or in the nearby ski resort of Aussois, a 10-15 minute drive from the lab. Some hotels we have tried:
- [Hotel Le Commerce](http://www.hotel-le-commerce.net) in Modane
- [Les Voyageurs](https://www.booking.com/hotel/fr/les-voyageurs-modane.en-gb.html) in Modane
- [Les Mottets](http://www.hotel-lesmottets.com) in Aussois
- [Hotel du Soleil](https://www.hotel-du-soleil.com/en) in Aussois

If a few people are travelling together outside peak vacation season, it may be possible to rent a chalet in Aussois - speak to Manu if you are interested.

Modane and Aussois both have restaurants, although some of them will be closed in the non-tourist season. Modane's gastronomic district (such as it is) is the street by the railway station. A few we like:
- [Il Peppuccio](https://www.tripadvisor.co.uk/Restaurant_Review-g661682-d2002414-Reviews-Il_Peppuccio-Modane_Savoie_Auvergne_Rhone_Alpes.html) Pizzeria in Modane. No trip to LSM is complete without a Peppuccio pizza. Veggie options available. Gluten-free possible but limited.
- [L'Echappee](https://www.tripadvisor.co.uk/Restaurant_Review-g661682-d3681609-Reviews-L_Echappee-Modane_Savoie_Auvergne_Rhone_Alpes.html) A little more expensive, with French food including Alpine specialities. Go there when you want to celebrate.
- [Pulcinella](http://www.pizzeriapulcinella.fr) A pizzeria that is not Peppuccio. Sometimes open when Peppuccio is closed.
- [Le Perce Neige](http://www.hotel-leperceneige.com) Traditional food of the Savoie region. Lots of cheese. Feels like somebody's living room.
- [L'international](http://www.savoie-mont-blanc.com/en/offre/fiche/restaurant-international/4840124) Turkish food. Exotic by Modane standards!
- [Hotel de la Gare](https://www.hoteldelagare-modane.com) Sells crepes and galettes, among other things.

### Getting to Modane
The easiest way to get to Modane is probably to fly to either Geneva or Lyon St-Exupery, and rent a car. It's around a 2.5-hour drive to the lab from either of these, mostly on motorways, although the travel time can vary significantly with traffic. There is parking at the lab and street parking near the hotels, though finding spaces in downtown Modane can be annoying.

The TGV from Paris Gare-de-Lyon to Turin stops in Modane, but the trains are not frequent. It's about a 4-hour ride from Paris. For more flexibility in timing, you can consider changing at Chambery and using a local train for the Alpine part of the trip. There is also a TGV from the Lyon airport - again, infrequent - if you don't want to drive. To get to Geneva airport by public transit, take the train to Chambery and then either a Flixbus direct to the airport, or train changing in Geneva central. You can book the trains on the SNCF website or app.

### Things to consider
It is warm in the tunnel! Choose comfortable and cool clothing. Be sure to stay hydrated. (There is drinking water available underground.) 

When you are underground, you must wear closed-toed shoes. No sandals!

There is no wi-fi underground, but you can connect to the internet using an ethernet cable (in the break room). You should turn off your phone or put it in airplane mode when you are underground, to protect other experiments in the lab.

</div>
</div>
            
            <div id="analysis" style="display:none">
                <header class="post-header">
                    <h1 class="post-title text-center">Data and analysis</h1>
                </header>
<div markdown="1">
Analysis code
-------------
A work-in-progress collection of SuperNEMO and NEMO-3 analysis code is available in the [AllAnalyses](https://github.com/SuperNEMO-DBD/AllAnalyses) repository under {% include icon-github.html username=site.github_username %}.

## SuperNEMO Analysis wiki

The [SuperNEMO Analysis wiki page](https://nemo.lpc-caen.in2p3.fr/wiki/NEMO/SuperNEMO/Analysis) is hosted at LPC Caen and holds up-to-date information about the status of analyses, as well as links to helpful tools and documents to get you started analysing SuperNEMO data.  It also has links to the minutes of all our internal analysis meetings. You can get a login from [Yves](lemiere@lpccaen.in2p3.fr) or [Francois](mauger@lpccaen.in2p3.fr).

</div>
            </div>

<div id="mtg" style="display:none">
    <header class="post-header">
        <h1 class="post-title text-center">Future meetings</h1>
    </header>


<p>All the information you need about the upcoming collaboration meetings</p>
{% assign meetings_by_date = site.meetings | sort:"startdate" |  reverse %}
<div class="container-fluid">
  {% for meeting in meetings_by_date %}
  <div class="row">
    <div class='col-xs-7'>
     {% if meeting.remoteurl %}<a href="{{ meeting.remoteurl }}" target="_blank">{% endif%}  
     <h2>{{ meeting.location }}</h2>
     {% if meeting.remoteurl %}</a> {% endif%} 
   <p> 
   {% if meeting.startdate %}
    {% if meeting.enddate %}{{ meeting.startdate | date: "%A %-d %B " }} to  {{ meeting.enddate | date: "%A %-d %B, %Y" }} 
    {% else %} Week of {{ meeting.startdate | date: "%A %-d %B, %Y" }} {% endif%} 
     (Week {{ meeting.startdate | date: "%U" }})
    <br/>

    {% endif%} 
      <i>{{meeting.abstract}}</i>
      </p>
    </div>
    <div class='col-xs-5'>
      {% if meeting.remoteurl %}<a href="{{ meeting.remoteurl }}" target="_blank">{% endif%}  
      <img src="{{meeting.thumbnail}}" class="img-thumbnail" alt="{{ meeting.location}} ">
      {% if meeting.remoteurl %}</a> {% endif%} 
    </div>
  </div>
  {% endfor %} 
</div>

</div>
</div>

<div class="col-xs-3">
    
<div class="square" style="background-color:var(--first-color);" id="conf_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Upcoming Conferences
</div>
</div>
</div>
</div>

<div class="square" style="background-color:var(--second-color);" id="docs_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Internal Documentation
</div>
</div>
</div>
</div>

<div class="square" style="background-color:var(--third-color);" id="software_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Software and computing
</div>
</div>
</div>
</div>

<div class="square" style="background-color:var(--fourth-color);" id="ops_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Operations
</div>
</div>
</div>
</div>

<div class="square" style="background-color:var(--fifth-color);" id="analysis_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Data and analysis
</div>
</div>
</div>
</div>

<div class="square" style="background-color:var(--sixth-color);" id="mtg_btn">
<div class="content">
<div class="table">
<div class="table-cell">
Future meetings
</div>
</div>
</div>
</div>

</div>

</div>
</div>





