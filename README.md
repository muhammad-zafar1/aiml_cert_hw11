## What Drives the Price of a Car? 
#### Required Practical Application Assignment for AI & ML Certificate Course
Date: 5-4-25

Link to Notebook:
URL

### Target Audience
Car dealers in the U.S. interested in understanding how to maximize the sale price of used cars.

### Executive Summary

Consider the following factors when selling used-cars for your dealership --

Top charactteristics (higher price):
------------------------------------
Put vehicles for sale having these characteristics: 
- ferrari, tesla, aston-martin, porsche, rover, audi, morgan and lexus
- Type: pickup, convertible, coupe, truck.
- Having 8 or more cylinders
- Have diesel fuel type
- Cars with clean title or lien title
- Cars with these conditions offer higher prices: condition_like new
- Cars from these states: Utah, Montana, Alaska, Washingtin, North Dakota, Nevada, Kansas, Wyoming
- Year - Generally cars that are newer offer higher prices than cars that are old. However, there are exceptions for vintage cars from the 1960s or earlier that are in decent condition.


Bottom Characteristics (lower price):
------------------------------------
Avoid selling vehicles of these characteristics:
- manufacturer: saturn, kia, mitsubishi, land rover, fiat, harley-davidson
- Type: wagon, sedan, hatchback, or bus
- Cars with 3, 4 or 5 cyclinders
- Cars with missing, rebuilt, salvage or parts only title
- Cars with these conditions offer lower pricees: condition_salvage, condition_fair
- Cars from these states: Connecticut, Illinois, New York, Pennsylvania, Massachusetts, New Hampshire, Washington D.C., Oregan, Maine, Virginia


---

### Detailed Findings

```
This section provides detailed level findings from the analysis --

Buyers willing to pay the highest prices for cars from these manufacturers:

manufacturer_ferrari
manufacturer_tesla
manufacturer_aston-martin
manufacturer_porsche
manufacturer_rover
manufacturer_datsun
manufacturer_alfa-romeo
manufacturer_audi
manufacturer_morgan
manufacturer_lexus

Buyers willing to pay the lowest prices for cars from these manufacturers:

manufacturer_saturn
manufacturer_kia
manufacturer_mitsubishi
manufacturer_land rover
manufacturer_fiat
manufacturer_harley-davidson


These types of cars offer highest prices:
type_pickup
type_convertible
type_coupe
type_truck
type_van
type_offroad


These types of cars offer lower prices (in general):
type_mini-van
type_other
type_SUV
type_wagon
type_sedan
type_hatchback
type_bus


Buyers willing to pay the highest prices for cars with 8, 10 or 12 cylinders.
Cars with 3, 4 or 5 cyclinders typically have lower prices.

Cars with license plates from these states have the highest prices (generally):
state_ut
state_mt
state_ak
state_wa
state_nd
state_nv
state_ks
state_wy
state_mo
state_id

Cars with license plates from these states have the lowest prices (generally):
state_ct
state_il
state_ny
state_pa
state_ma
state_nh
state_dc
state_or
state_me
state_va

Cars with clean title or lien title offer the higest prices.
Cars with missing, rebuilt, salvage or parts only offer the lowest prices.

Generally cars that are newer offer higher prices than cars that are old. However, there are exceptions for vintage cars from the 1960s or earlier that are in decent condition.

Cars with these conditions offer higher prices: 
condition_new
condition_like new

Cars with these conditions offer lower pricees:
condition_salvage
condition_fair



```

---

### Recommendations for Used Car Dealers

Bottom Line - 
Consumers value cars that  have following characteristics --
 
- Manufacturer: ferrari, tesla, aston-martin, porsche, rover, audi, morgan and lexus
- Type: pickup, convertible, coupe, truck, with diesel fuel type, having 8 or more cylinders
- Cars with clean title or lien title
- Cars with "like new" condition
- Cars from these states: Utah, Montana, Alaska, Washingtin, North Dakota, Nevada, Kansas, Wyoming
- Generally cars that are newer offer higher prices than cars that are old. 
- However, there are exceptions for vintage cars from the 1960s or earlier that are in decent condition.


 [End of Report]

---

### Appendix Section
#### (For Technical Audience / Data Scientists)

Dataset & Methodology
- Data - 
- Car sales dataset on 426K used cars from Kaggle. Dataset Source: Kaggle (www.kaggle.com)

- Methodology - 
- Analysis used the CRISP-DM data science methodology to perform analysis on car sales dataset.
- Exploratory data analysis of car dataset in Jupyter Notebook. Further analysis using linear regression models to understand factors that maximize car sales price.

- Assumptions - 
- Car sale prices over $150K excluded from analysis. Results only apply to vehicles of value lower than $150K.
- Cars with odometer over 400,000 miles excluded from analysis. Results only apply to vehicls having odometer reading of less than 400K.
- Empty fields and NaNs replaced with 'unknown' value to facilitate building the regression model.
- Regression model dataset had 419429 rows and 14 columns. After convering categorical variables total number of columns increased to 162.
```
Index: 419429 entries, 27 to 426879
Data columns (total 14 columns):
    Column        Non-Null Count   Dtype  
---  ------        --------------   -----  
 0   price         419429 non-null  int64  (dependent variable)
 1   year          419429 non-null  float64
 2   manufacturer  419429 non-null  object 
 3   condition     419429 non-null  object 
 4   cylinders     419429 non-null  object 
 5   fuel          419429 non-null  object 
 6   odometer      419429 non-null  float64
 7   title_status  419429 non-null  object 
 8   transmission  419429 non-null  object 
 9   drive         419429 non-null  object 
 10  size          419429 non-null  object 
 11  type          419429 non-null  object 
 12  paint_color   419429 non-null  object 
 13  state         419429 non-null  object 
```

