# SNAP Analysis Methods

## Question 1: Is there an association between a household earning below the FPL and being enrolled in SNAP?

| Variables   | Description | Unit A | Unit B |
| ----------- | ----------- | ----------- | -------- |
| Exposure    | Below Poverty | Count | Percent |
| Outcome     | Enrolled in SNAP   | Count | Percent |

Population: Households that responded to the ACS Survey
    
    Unit A
    Count (Exposure) = Households that are below FPL
    Count (Outcome) = Households enrolled in SNAP
        
    Unit B
    % (Exposure) = ((Households that are below FPL)/(All Households)) * 100
    % (Outcome) =  ((Households enrolled in SNAP)/ (All Households)) * 100

GEO_IDs from ACSST5Y2019.S2201_metadata_2022-02-14T162245.cvs

    Unit A
    Count (Exposure) = Households that are below FPL = S2201_C01_021E 
    Count (Outcome) = Households enrolled in SNAP = S2201_C03_001E
    
    Unit B
    % (Exposure) = ((Households that are below FPL)/(All Households)) * 100 = ((S2201_C01_021E)/(S2201_C01_001E)) * 100
    % (Outcome) =  ((Households enrolled in SNAP)/ (All Households)) * 100 = ((S2201_C03_001E)/ (S2201_C01_001E)) * 100
    
    
## Question 2: What is the distribution of SNAP Enrollment by Race/Ethnicity?

| Variables   | Description | Unit A | Unit B |
| ----------- | ----------- | ----------- | -------- |
| Exposure    | Race/Ethnicity  | Count | Percent |
| Outcome     | Enrolled in SNAP   | Count | Percent |

![xychart SNAP](https://github.com/tiherna2/Write-Ups/blob/main/ChartSNAP.png)

Population: Households that responded to the ACS Survey

    Unit A - Count
    Count (Exposure) = Race/Ethnicity
    Count (Outcome) = Households of Race/Ethnicity enrolled in SNAP
    
    Unit B - Percent (%)
    Rate (%) = ((Number of Households of Race/Ethnicity on SNAP)/(Total Number of Households on SNAP))
    
    Repeat % calculations for each race/ethnicity and compare values via bar chart.
    
    
## Question 3: SNAP Enrollment Gap By Race/Ethnicity

Population: Households that responded to the ACS Survey

### Calculating SNAP Gap by Race/Ethnicity

    Rate of Race/Ethnicity 1 = ((number of households below FPL of Race1)/(number of households below FPL total))
