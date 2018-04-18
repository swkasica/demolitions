Demolitions data diary
======================

## Data sources

### Permits
Looking at [Issued-Contruction-Permits](https://data.austintexas.gov/Permitting/Issued-Construction-Permits/3syk-w9eu) on Austin data portal:

So, I downloaded files using the following filters:
* `AppliedDate` > 2007-12-31 and `PermitType` = "BP" and `WorkClass` = 'Demolition' goes into demos-full.csv
* `AppliedDate` > 2007-12-31 and `PermitType` = "BP"`WorkClass` != 'Demolition' and `Description` contains 'partial demo' goes into demos-partial.csv

the API endpoint is:
https://data.austintexas.gov/resource/x9yh-78fz.json

https://data.austintexas.gov/resource/x9yh-78fz.json?PermitType=BP&WorkClass=Demolition&$limit=10

https://data.austintexas.gov/resource/x9yh-78fz.json?$where work_class = 'Demolition'


GET https://data.austintexas.gov/resource/x9yh-78fz?$where=permittype = 'BP' and work_class = 'Demolition' and calendar_year_issued > '2008'

GET https://data.austintexas.gov/resource/x9yh-78fz?$limit=10&$where=permittype = 'BP' and work_class = 'Demolition' and calendar_year_issued = '2008'


### Example endpoint:
{
    "applieddate": "2009-07-09T00:00:00.000",
    "calendar_year_issued": "2009",
    "completed_date": "2009-10-05T00:00:00.000",
    "condominium": "No",
    "council_district": "5",
    "day_issued": "MONDAY",
    "description": "New 2 Stry SF Condo w att'ed garage  cov'rd porch  Patio",
    "electrical_valuation": "0",
    "expiresdate": "2009-10-05T00:00:00.000",
    "fiscal_year_issued": "2009",
    "housing_units": "1",
    "issue_date": "2009-07-13T00:00:00.000",
    "issue_method": "Permit Center",
    "issued_in_last_30_days": "No",
    "jurisdiction": "AUSTIN FULL PURPOSE",
    "latitude": "30.16640396",
    "link": "https://www.austintexas.gov/devreview/b_showpublicpermitfolderdetails.jsp?FolderRSN=10307783",
    "location": {
        "type": "Point",
        "coordinates": [-97.826629, 30.166404]
    },
    "longitude": "-97.82662945",
    "number_of_floors": "2",
    "original_address1": "1624 ROCKLAND DR",
    "original_city": "AUSTIN",
    "original_state": "TX",
    "original_zip": "78748",
    "permit_class": "C- 101 Single Family Houses",
    "permit_location": "1624 ROCKLAND DR",
    "permit_number": "2009-074412 EP",
    "permit_type_desc": "Electrical Permit",
    "permittype": "EP",
    "project_id": "10307783",
    "status_current": "Final",
    "tcad_id": "0432210501",
    "total_new_add_sqft": "1931",
    "work_class": "New"
}


## combining demos and partials

`deomlitions.ipynb` has the script that puts these files together. 

### Plan reviews
We also received the file `Demo and Partial Demo Plan Review Applications since 2005.xlsx` and the following note: Attached is the spreadsheet associated with Plan Review applications for Partial and Total demos that have been received since 2005.  We did not start using the AMANDA database until about half way through 2007, so data starting in 2008 will be more consistently formatted.

Sylvia A confirmed that I can use the `Building Permit` as the parent permit for all demolitions.

Sylvia said the database changed in 2007, so data from 2008 forward would be most consistent, to that's what we are going with for now.





