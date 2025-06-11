# Greenhouse environment and electricity prediction based on the TCN (Temporal Convolutional Networks) model

Goal: 
Utilize the TCN model to predict the environment and electricity in the greenhouse based on the greenhouse dataset

Data Collection：
Collect greenhouse data from 1/1/2023  00:00:00 AM to 12/31/2023  11:55:00 PM
| Abbreviation    | Full English Name                               |
|:-----------------:|:-------------------------------------:|
| datetime          | Datetime                              |
| in_temp           | Internal Temperature                   |
| in_humi           | Internal Humidity                      |
| in_co2            | Internal CO₂ Concentration             |
| out_temp          | External Temperature                   |
| wind_dir          | Wind Direction                         |
| wind_spd          | Wind Speed                             |
| solar_rad         | Solar Radiation                        |
| cum_solar_rad     | Cumulative Solar Radiation              |
| dew_point         | Dew Point Temperature                  |
| rain_sig1         | Rain Signal 1                          |
| rain_sig2         | Rain Signal 2                          |
| storm_sig         | Storm Signal                           |
| hvac              | Heating Ventilation Air Conditioning (HVAC) |
| fan               | Circulation Fan                        |
| sprayer           | Sprayer                                |
| l_win             | Left Window                            |
| r_win             | Right Window                           |
| curtain1          | Curtain 1                              |
| curtain2          | Curtain 2                              |
| tube_rail_pwr     | Tube Rail Power                        |
| fcu_pwr           | Fan Coil Unit Power                    |
| fan_pwr           | Circulation Fan Power                  |
| sprayer_pwr       | Sprayer Power                          |
| l_win_pwr         | Left Window Power                      |
| r_win_pwr         | Right Window Power                     |
| curtain1_pwr      | Curtain 1 Power                        |
| curtain2_pwr      | Curtain 2 Power                        |
To run the code
Step 1
Download the greenhouse dataset from final_project_data.csv
Step 2
The prediction model is obtained by running
