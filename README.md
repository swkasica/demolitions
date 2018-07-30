Demolitions
=======================

Data diary and notes for work toward Phil Jankowski story about demolitions, scheduled for summer 2018.

## Analysis

The analysis is in Jupyter Notebook files in the folder `/notebooks/`.

## Tableau interactive

There are two Tableau charts. Right now they are put together with tabs, but they could be embedded separately if we want.
* [Map of demolitions](https://public.tableau.com/profile/statcomdata#!/vizhome/Demolitions2008-2017/Mapofdemolitions)
* [Demolitions by zip](https://public.tableau.com/profile/statcomdata#!/vizhome/Demolitions2008-2017/DemolitionsbyZIP)


Embed with chart first:

``` html
<div class='tableauPlaceholder' id='viz1532362448224' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;De&#47;Demolitions2008-2017&#47;DemolitionsbyZIP&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Demolitions2008-2017&#47;DemolitionsbyZIP' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;De&#47;Demolitions2008-2017&#47;DemolitionsbyZIP&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1532362448224');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='320px';vizElement.style.maxWidth='575px';vizElement.style.width='100%';vizElement.style.height='650px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='320px';vizElement.style.maxWidth='575px';vizElement.style.width='100%';vizElement.style.height='650px';} else { vizElement.style.minWidth='320px';vizElement.style.maxWidth='575px';vizElement.style.width='100%';vizElement.style.height='650px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
```

Embed with map first:

``` html
<div class='tableauPlaceholder' id='viz1532362895495' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;De&#47;Demolitions2008-2017&#47;Mapofdemolitions&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Demolitions2008-2017&#47;Mapofdemolitions' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;De&#47;Demolitions2008-2017&#47;Mapofdemolitions&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1532362895495');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.minWidth='320px';vizElement.style.maxWidth='575px';vizElement.style.width='100%';vizElement.style.height='650px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
```

## Print graphics

Submitting two print graphics: Line chart of demolitions per year by zip code; map of areas with most demolitions 2008-2017.

### Demos by year, by zip

- Data is: `data-processed/top_demos_year_zip.csv`.
- Example: `resources/top_demos_yr_zip_example.png`.
- [Interactive example in Tableau](https://public.tableau.com/profile/statcomdata#!/vizhome/Demolitions2008-2017/DemolitionsbyZIP).

Headline: Demolition permits by ZIP code

Chatter: South and East Austin that have seen the greatest increase in residential demolitions since 2008, though other areas have seen more recently.

Source: City of Austin construction permits

### Demos map

- Data is: `data-processed/demos_by_zip.csv`
- Example map: `qgis/demos_by_zip.pdf`

This was done in QGIS to give GateHouse graphics a good file to work with. All of that is saved in `qgis`. Some files used but not tracked:

- City of Austin [Street Centerline shapefile](https://data.austintexas.gov/Locations-and-Maps/Street-Centerlines/m5w3-uea6).
- TIGER/Line Shapefiles 2017 [ZIP Code Tabulation Areas](https://www.census.gov/cgi-bin/geo/shapefiles/index.php)

Headline: South, East Austin drive demolitions

Chatter: Desirable, close-in neighborhoods have seen the most residential demolition permits since 2008. 

Source: City of Austin construction permit data

## Data diary

Main construction permits data:
https://data.austintexas.gov/Building-and-Development/Issued-Construction-Permits/3syk-w9eu/data

### 2/26/2018
Created two views on data.austintexas.gov
- https://data.austintexas.gov/Building-and-Development/demolitions-full-post2017/4d8v-cjdw
    + https://data.austintexas.gov/resource/4d8v-cjdw.json
- https://data.austintexas.gov/Building-and-Development/demolitions-partial-post2007/8qw5-9tag
    + https://data.austintexas.gov/resource/8qw5-9tag.json

The method was similar to this:
* `AppliedDate` > 2007-12-31 and `PermitType` = "BP" and `WorkClass` = 'Demolition' goes into demolitions-full-post2017.csv
* `AppliedDate` > 2007-12-31 and `PermitType` = "BP"`WorkClass` != 'Demolition' and `Description` contains 'partial demo' goes into demolitions-partial-post2007

Downloaded both of those files into data-raw.


### Notes: 3/5/2018 Julia Robbins

```
Julia Robbins
IT Data Architect, Strategic Operations
City of Austin Development Services Department
505 Barton Springs Road, 7th Floor
Austin, Texas 78704
Work: (512) 974-9236
Julia.Robbins@austintexas.gov
```

Talked with Julia about the format of the data, pitfalls, etc. Some of the things we learned:

- WorkClass = Demolition is total demolitions.
- Partial demos are hand coded by SOP in the description field by humans. There could be areas.
- She did not know if there was an official or unofficial list of terms used there.
- The WorkClass of "Addition and Remodel" was originally used for a permit where both were true. (There are also separate "Addition" and "Remodel" WorkClasses.) However, recently that class has been used for either/or, perhaps because it is difficult to change from one class to another, so they used the combined one to start. This makes tracking those individual terms more difficult.
- Expired permits are those that were issued, but no inspections were ordered before the expiration of the permit. When inspectiions are done, the status is active. We do NOT want to keep Expired in our study, but we should be aware of them.
- While there is no "sigle-wall teardown" flag, we *might* be able to use partial demo records and then compare the total/remodel/addition square footage.

### Notes: From Daniel Ward on 3/7/2018

```
Acting Plans Examiner Manager
City of Austin Development Services Department
One Texas Center, 2nd floor
505 Barton Springs Road
Office: 512-974-3341
```

“SFR” is just adopted shorthand by staff to avoid having to type out “single-family residence” over and over again- there is not any official policy on this issue.
 
The phrase “partial demo” or “partial demolition” is added to the description of work on many remodel and addition type projects that will require the removal of some element of the exterior walls or roof. For the projects you are looking for, this would be a place to start, as the “single-wall-left-standing” demolitions are typically a subset of these projects.
 
However, it is going to be very difficult to find the projects you are looking for, as in my experience, the plans seldom reflect this condition. It typically occurs during construction, after the plan review is complete. The contractor/owner/framer starts exposing the walls by removing sheetrock and exterior cladding (siding, brick, stucco, etc.) and finds less than desirable conditions, and proceeds to remove the deteriorated/sub-standard wall framing, resulting in very little or none of the existing walls remaining.


## Ideas that didn't pan out
- find permits for known single-wall demos and see what they look like
- Look at the Circa dates and see if we can quantify destruction of older homes?

Challenge here might be that the same location can have full and partial demos. Like for a house and then a garage.
