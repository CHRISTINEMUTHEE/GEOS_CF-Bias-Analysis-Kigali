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


