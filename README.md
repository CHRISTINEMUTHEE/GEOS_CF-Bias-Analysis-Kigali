# GEOS_CF-Bias-Analysis-Kigali
This project describes the data cleaning, validation and bias analysis that was undertaken for Low Cost Sensor data in Kigali.
This data was used to correct bias in NASA's GEOS-CF Air Quality Global Forecast outputs to generate station level, bias corrected forecasts.
The data was extracted from The Rwanda Environemtal Management Authorities Air quality data management system.
### Understaning Data from REMA 
Low Cost Sensor Data is from Mt.Kigali, Kimihurura, Gikomero and Gacuriro.
The reference Grade data is from Gitega site.
#### <Features within Data.>
1. Time Stamp - This is the period of data collected. We have one year of data from 5 sites in Kigali.
2. O3- Ozone Gaseous values in ppbv 
3. PM25- Fine particulate Matter with a diameter of less than <2.5> ug/m3
4. CO - Carbon Monoxide in ppbv
5. PM10- Particulate Matter with a diameter less than <10> ug/m3
### Data Structure before Cleaning.

| **Location** | **Type of Equipment** | **Timeline**                                    | **Parameters**  | **Calibration Status** |
|--------------|-----------------------|-------------------------------------------------|-----------------|------------------------|
| Mt.Kigali    | Low Cost Sensors      | 1st July 2021 0000hrs - 30th June 2022 2300hrs. | O3,PM25,CO,PM10 | Calibrated             |
| Kimihurura   | Low Cost Sensors      | 1st July 2021 0000hrs - 30th June 2022 2300hrs. | O3,PM25,CO,PM10 | Calibrated             |
| Gacuriro     | Low Cost Sensors      | 1st July 2021 0000hrs - 31st July 2022 2300hrs. | O3,PM25,CO,PM10 | Calibrated             |
| Gikomero     | Low Cost Sensors      | 1st July 2021 0000hrs - 30th June 2022 2300hrs. | O3,PM25,CO,PM10 | Calibrated             |
| Gitega       | Reference Grade Monitor| 1st July 2021 0000hrs - 30th June 2022 1200hrs. | O3,PM25,CO,PM10 | Calibrated            |

## Data Cleaning and Validation Protocol.
Air Quality data generation has grown rapidly with demand for monitoring data emanating from governments,research organizations, Citizen scientist, the media etc.The cost of deploying reference grade montors has limited investments into air quality data generation. Recent investments in Low Cost Sensors has stired a rapid uptake of air quality data in varying institutions and governments in the need to expand the data networks and spatial coverage in monitoring. This however comes at a cost of noisy data from Low Cost Sensors. Data generated from Low Cost Sensors requires a higher degree of scruitiny due to the greater uncertainity expected.
The Development of a QA/QC protocol is therefore paramount to generate "Data of Known Quality/Conformance".
The same criteria of determining conformance, depending on the area of application was applied to LCS used for GEOS-CF bias correction.
### Factors considered in analyzing the quality of the data from Kigali.

1. **Representativeness**- qualitative  measurement  that  describes  how  well  the field data characterizes the area of concern, the expected outputs eg. Time stamps, Site Naming, Coordinates etc. Data from Reference Grade colocated with the Sensors was analyzed to assess deviation and instances of spike data (outliers). 
2. **Accuracy** - the agreement between an observed value and an accepted reference or  true  value. The report can be seen in the Link attached.
3. **Precision** - we assessed the closeness of agreement, or degree of dispersion, between the series of measurements to detect outliers and correlation of parameters in variation throughout the year, despite the heterogeinity in environmental conditions.
4. **Completeness** - quantitative  measure  that  is  used  to  evaluate  how  many valid  data were obtained in comparison to the amount that was planned. We budgeted for one year of full data from each site.

### Results and Discussions.
Data was merged into a single dataframe for analysis.We had only 0.33% of missing values for the CO paramter which could be attributed to the values from Gitega station. This is fit for analysis as  such an margin is unlikely to cause changes in the variation of the data in the entire dataset.
## Daily Average.
### 1. Gacuriro.
* This site has constant values for PM10 and PM2.5 indicative of equipment failure or single value logging in the month of May 2022 to Mid- July 2022.
* An instance of an outlier spike in Ozone concentration was detected in May 2022.
* An anomaly characterized by a drop and immediate spike level of CO was detetected in May to July. This could be attributed to outlier values within the hourly logs or a sudden pollution activity at around the same time.

### 2. Gitega.
* Irregular patterns,characterized by graphs ehich discrete patterns, unlike what is expected of continous values. The partpetual pattern seems to be in all pollutant values. Indicating instances of equioment failure, iregular logs and errors in numeical conversions.

### 3. Kimihurura.
* PM10 concentration has a steady variation abd a singkle spike event in June 2022. The outlier values peak from <100 ugm3 to > 600 ug/m3. This is indicative of a single pollution event or error in the value log.
* From a steady pattern of CO concentration, there is an instance of a sudden drop in June 2022.
