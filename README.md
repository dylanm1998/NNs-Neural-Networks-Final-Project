# 🌿 Greenhouse Environment Prediction based on the TCN (Temporal Convolutional Networks) Model

## 🎯 Goal

Utilize the **TCN model** to predict the environment in the greenhouse based on historical data.

---

## 📅 Data Collection

- **Period**: from `2023-01-01 00:00:00 AM` to `2023-12-31 11:55:00 PM`
- **Source**: Greenhouse sensor and control system logs

---

## 🗂️ Dataset Fields

<div align="center">

| Abbreviation    | Full English Name                               |
|:---------------:|:-----------------------------------------------|
| datetime        | Datetime                                       |
| in_temp         | Internal Temperature                           |
| in_humi         | Internal Humidity                              |
| in_co2          | Internal CO₂ Concentration                     |
| out_temp        | External Temperature                           |
| wind_dir        | Wind Direction                                 |
| wind_spd        | Wind Speed                                     |
| solar_rad       | Solar Radiation                                |
| cum_solar_rad   | Cumulative Solar Radiation                      |
| dew_point       | Dew Point Temperature                          |
| rain_sig1       | Rain Signal 1                                  |
| rain_sig2       | Rain Signal 2                                  |
| storm_sig       | Storm Signal                                   |
| hvac            | Heating Ventilation Air Conditioning (HVAC)    |
| fan             | Circulation Fan                                |
| sprayer         | Sprayer                                        |
| l_win           | Left Window                                    |
| r_win           | Right Window                                   |
| curtain1        | Curtain 1                                      |
| curtain2        | Curtain 2                                      |
| tube_rail_pwr   | Tube Rail Power                                |
| fcu_pwr         | Fan Coil Unit Power                            |
| fan_pwr         | Circulation Fan Power                          |
| sprayer_pwr     | Sprayer Power                                  |
| l_win_pwr       | Left Window Power                              |
| r_win_pwr       | Right Window Power                             |
| curtain1_pwr    | Curtain 1 Power                                |
| curtain2_pwr    | Curtain 2 Power                                |
</div>

---

## 🏗️ Our Model Architecture (Based on the configured parameters)

<div align="center">
  <img src="https://github.com/user-attachments/assets/44b194de-123d-421e-bc40-7216d315c612" alt="Model Architecture" width="35%">
</div>



## ⚠️ Kind Reminder

> **Caution:** TensorFlow 2.10 was the last release that supported GPU on native Windows.  
> Starting with TensorFlow 2.11, to run TensorFlow with GPU support, you must either use **WSL2** or install `tensorflow`/`tensorflow-cpu` with optional [TensorFlow-DirectML-Plugin](https://www.tensorflow.org/install/pip).

---

## 💻 Running Environment Guide

### 1️⃣ Linux System (Recommended for TensorFlow >= 2.16 + GPU)

If you are using **Linux** and want GPU support with TensorFlow >= 2.16:

```bash
python3 -m pip install 'tensorflow[and-cuda]'
pip install [other required libraries]
```

### 2️⃣ Native Windows System (Win 10 / Win 11) - (Recommended for TensorFlow <= 2.10 + GPU)

If you want to run it with a GPU on **native Windows**, you should use **TensorFlow <= 2.10**.  
We strongly recommend using **Anaconda** to manage your environment.

#### Step-by-step:

1. **Create a virtual environment**:

    ```bash
    conda create -n {env_name} python=3.10.16
    ```

2. **(Optional) Install Jupyter Notebook**:

    ```bash
    conda install -c conda-forge jupyter
    ```

3. **Install CUDA Toolkit and cuDNN**:

    ```bash
    conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
    ```

4. **Install TensorFlow 2.10.1**:

    ```bash
    python -m pip install "tensorflow<2.11"
    ```

5. **Downgrade NumPy version (required for compatibility)**:

    ```bash
    python -m pip install "numpy<2"
    ```

---

### 📚 More about TCN

- [TCN Proposed Paper (arXiv)](https://arxiv.org/abs/1803.01271)
- [TCN PyTorch Implementation](https://github.com/locuslab/TCN)
- [TCN Keras Implementation](https://github.com/philipperemy/keras-tcn)

---

### ✅ Notes

- The code is developed based on **TensorFlow >= 2.16**. To utilize **GPU acceleration**, it is strongly recommended to run the project on a **Linux system**.
- If you need to run it on **native Windows**, please use **TensorFlow <= 2.10**.  
  In this case, you will also need to **adjust the import statements** for Keras-related libraries to ensure compatibility.


---
     
## 🙏 Acknowledgement
This work was carried out with the support of "Cooperative Research Program for Agriculture Science and Technology Development (Project No. RS-2021-RD010195)", Rural Development Administration, Republic of Korea.
