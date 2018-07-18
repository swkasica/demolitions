Demolitions
=======================

Data diary and notes for work toward Phil Jankowski story about demolitions, scheduled for summer 2018.

## Analysis

The analysis is in Jupyter Notebook files in the folder `/notebooks/`. There is also a [Tableau data visualization](https://public.tableau.com/profile/statcomdata#!/vizhome/Demolitions2008-2018/Mapofdemolitions) to explore the data.

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
