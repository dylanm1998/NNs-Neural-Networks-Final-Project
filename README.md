# Greenhouse environment and electricity prediction based on the TCN (Temporal Convolutional Networks) model

Goal: 
Utilize the TCN model to predict the environment in the greenhouse based on the previous statement

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

## Kind reminder 
Caution: TensorFlow 2.10 was the last TensorFlow release that supported GPU on native-Windows. Starting with TensorFlow 2.11, you will need to install TensorFlow in WSL2, or install tensorflow or tensorflow-cpu and, optionally, try the TensorFlow-DirectML-Plugin.
 - The code was made based on Tensorflow >= 2.16. If you want to run it on a GPU, you have to use a Linux system.
   How to do:
    - python3 -m pip install 'tensorflow[and-cuda]'
    - pip install [Other utilized libraries]

 - If you want to run it in Windows native system (Win 11, Win 10, etc.). You should install Tensorflow <= 2.10; we strongly recommend that you use Anaconda.
   How to do:
   1. Create a virtual environment in Anaconda
    - conda create -n {env_name} python=3.10.16
   2. (Optional) Install Jupyter Notebook
    - conda install conda-forge::jupyter
   3. Install cudatoolkit and cudnn:
    - conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
   4. Install tendorflow 2.10.1:
    - python -m pip install "tensorflow<2.11"
 
5. Downgrade the version of Numpy:
python -m pip install "numpy<2"
## Acknowledgement
This work was carried out with the support of "Cooperative Research Program for Agriculture Science and Technology Development (Project No. RS-2021-RD010195)", Rural Development Administration, Republic of Korea.
