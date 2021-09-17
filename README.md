# MLCompetetion - Pump It Up

Repo - https://github.com/mkhmaduwantha/MLCompetetion.git

## Features in the Dataset and applied feature Engineering technique

### 1. Similar Columns
#### This data set contains lot of features that has similar information 
---
* `scheme_management` - Who operates the waterpoint
* `management` - How the waterpoint is managed
* `management_group` - How the waterpoint is managed
##### here all 3 features has the same information since `scheme_management` contains null values and `management_group` contains less uique values, we can drop both these columns
---
* `quantity` - The quantity of water
* `quantity_group` - The quantity of water
##### both are similar here we can remove `quantity_group`
---
* `source` - The source of the water
* `source_type` - The source of the water
* `source_class` - The source of the water
##### remove `source_type` and `source_class` because all are similar
---
* `water_quality` - The quality of the water
* `quality_group` - The quality of the water
##### remove `quality_group` because both are similar
---
* `payment` - What the water costs
* `payment_type` - What the water costs
##### remove `payment_type`because both are similar
---
* `extraction_type` - The kind of extraction the waterpoint uses
* `extraction_type_group` - The kind of extraction the waterpoint uses
* `extraction_type_class` - The kind of extraction the waterpoint uses
##### `extraction_type` has more unique values than `extraction_type_group` but there are values with very small amounts. Also, `extraction_type_class` contains less unique values. So, `extraction_type_group` is chosen to keep.
---
* `waterpoint_type` - The kind of waterpoint
* `waterpoint_type_group` - The kind of waterpoint
##### remove `waterpoint_type_group` because both are similar
---
* `region` - Geographic location
* `region_code` - Geographic location (coded)
* `lga` - Geographic location
* `ward` - Geographic location
* `subvillage` - Geographic location
##### all above columns contain ge location data so we can drop others only keeping  `region`

* `amount_tsh` - Total static head (amount water available to waterpoint)
* `date_recorded` - The date the row was entered
* `funder` - Who funded the well
* `gps_height` - Altitude of the well
* `installer` - Organization that installed the well
* `longitude` - GPS coordinate
* `latitude` - GPS coordinate
* `wpt_name` - Name of the waterpoint if there is one
* `num_private` -
* `basin` - Geographic water basin
* `district_code` - Geographic location (coded)
* `population` - Population around the well
* `public_meeting` - True/False
* `recorded_by` - Group entering this row of data
* `scheme_name` - Who operates the waterpoint
* `permit` - If the waterpoint is permitted
* `construction_year` - Year the waterpoint was constructed








## Models Used - Random Forest, XGBoost
