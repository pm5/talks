title: Lowiki project
author:
  name: Pomin Wu
  twitter: pm5
  url: https://lowiki.org/
output: index.html
theme: sudodoki/reveal-cleaver-theme

--

# ???
## How we adapt LocalWiki and OSM tools for our work

--

Pomin Wu [@pm5](https://www.openstreetmap.org/user/pm5)

OSM since 2012

[g0v.tw](http://g0v.tw/), [openstreetmap.tw](http://openstreetmap.tw/)

[pm5.github.io/talks](https://pm5.github.io/talks/)

--

### 4 parts in this talk

1. About Lowiki project
1. LocalWiki
1. OSM Tasking Manager
1. Future

--

## Lowiki

[lowiki.org](https://lowiki.org/)

*A crowdsourcing platform for disaster-related knowledge*

--

### Crowdsourcing

* ...to collect local knowledge.
* ...to include governemnt as one of the "contributors".

In other word, we use crowdsourcing process to build collaborations between **government** and **local people**.

--

![](images/lowiki-page0_c.png)

--

![](images/lowiki-page1_c.png)

--

![](images/lowiki-page2_c.png)

--

![](images/lowiki-page3_c.png)

--

Information is co-edited by NCDR and the community.

<div class="footnote">NCDR stands for National Science and Technology Center for Disaster Reduction.</div>

--

In order to achieve this with a relatively small team, we adapted several open source tools for our purpose.

<div class="footnote">Our team consists of 8 people, including 2 developers.  All of us work part-time on this project.</div>

--

... and we leverage OSM and its community.

--

## LocalWiki

[localwiki.org](https://localwiki.org/)

*A grassroots effort to collect, share and open the world's local knowledge*

--

![](images/localwiki_c.png)

--

![](images/localwiki-region0_c.png)

--

### LocalWiki main features

* Regions
* Pages
* Tags
* Maps
* Templates

I'll talk about how we (Lowiki) uses **tags**, **maps**, and **templates**.

--

### Tag

* We use a 5 tags through out Lowiki:
  - community/apartment complex
  - shelter
  - resource center
  - social facility
  - gas/water station
* Users can use any tag they deem adequate as well.
* This way we have tag views with **integrated maps**.

--

![](images/lowiki-tagviewmap_c.png)

--

### Map

1. We enhanced the "import from OSM" feature.
2. We added disaster information from government WMS service.

--

![](images/lowiki-mapask_c.png)

--

XXX

![](images/lowiki-mapedit_c.png)

--

XXX

![](images/lowiki-wms_c.png)

--

![](images/lowiki-map_c.png)

--

![](images/lowiki-mapwms0_c.png)

--

![](images/lowiki-mapwms1_c.png)

--

### Template

* We use structral templates (tables) for the 5 default tags.
* The structral information can be exported as CSV, TXT, or KML.
* LocalWiki also has built-in JSON-based RESTful API.
* The data structure (tables) is defined directly in templates, so users can change them as needed.

--

![](images/lowiki-templatetable_c.png)

--

![](images/lowiki-exportcsv_c.png)

--

![](images/lowiki-exportkml_c.png)

--

In other word, **text-base descriptions** are made **structral** by providing users with better tools to organize them, much like tag system in OpenStreetMap.

--

### Summary on LocalWiki

* From the domain knowledge of disaster experts, we identify at least 5 **core facilities** in disaster relief.
* LocalWiki is flexible enough for us to **build a crowdsourcing process** around these core facilities, using tags, maps, and templates.
* A set of simple template of tables helps us make the information **structral**.

--

## OSM Tasking Manager

--

![](images/osmtm_c.png)

--

### Bootstrap with official data

* Government Open Data such as [data.gov.tw](https://data.gov.tw/) has a lot of information.
* Not only do they have polygons, but also attributes such as addresses, phone numbers, operator names, opening hours, etc.
* A lot of that are not on OpenStreetMap yet.

--

### Import

We don't import data frequently because:

* Community discussion and review is a lot of work.
* Import itself is stressful.
* Keeping data up-to-date is hard.

--

![](images/osmtm-importaed_c.png)

However, there are now 8194 records of defibrillator in the [offician data](http://tw-aed.mohw.gov.tw/SearchPlace.jsp?Action=Search&City=&Area=&Type=&PlaceType=&Key=&intPage=260).

--

### Collaborate on data import/synchronization

Doing this with OSM Tasking Manager would be:

* Easier.
* Less stressfull.
* Many of the works can be automated.

--

![](images/osmtm-project_c.png)

--

### "Dataset" in OSMTM

We modified OSMTM so that one can:

* Upload a dataset to a Tasking Manager project.
* Split the dataset by tasks.
* Automatically validate tasks that has no new data.
* Automatically invalidate *only* the tasks having new data.
* Coordinate import works with Tasking Manager workflow.
* Visualize progress.

--

![](images/osmtm-projectdataset_c.png)

--

![](images/osmtm-task_c.png)

--

![](images/id-taskdata_c.png)

--

![](images/josm-taskdata_c.png)

--

![](images/osmtm-done_c.png)

--

### Results

* Clearly-defined roles and goals.
* Automated diffing and saves works.
* Visualized progress to encourage collaborations.

--

## Future

*Some ideas we are having in mind*

--

### Data pipeline from Open Data

Automatically update government Open Data to OSMTM.

```
Open Data ⇒ OSMTM ⇒ OSM
```

--

### Data pipeline from LocalWiki

What we have now:

```
OSM ⇒ LocalWiki import
```

What we can do:

```
LocalWiki export ⇒ OSMTM ⇒ OSM
```

--

### Issues report

* Report OSM issues from LocalWiki.
* [watermap.teia.tw](https://watermap.teia.tw/)

```
LocalWiki ⇒ OSM Note ⇒ OSM
```

--

### (Slightly more) structured OSM notes

* With hashtag (`#lowiki`) and `key=value` pairs.
* Build **issue tracking tools** on OSM notes.

--

![](images/watermap_c.png)

--

![](images/watermap-form_c.png)

--

![](images/watermap-note_c.png)

--

![](images/watermap-issue_c.png)

--

### Apply to other domains

* localwiki.tw (temporarily suspended)
