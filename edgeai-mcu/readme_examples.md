# Example applications

The [TI Tiny ML Model Zoo](https://github.com/TexasInstruments/tinyml-modelzoo) ships ready-to-run example configurations that cover common sensing and inference tasks on TI MCUs. Each example bundles a dataset, a tuned model, and a device-specific config - clone the repo, point the toolchain at an example's `config.yaml`, and training, quantization, and compilation happen automatically.

Examples are grouped by task type. The first row in each table is a **generic** example meant to be adapted to your own dataset; every other row is a **dedicated**, purpose-built config for that specific use case. See the [Tiny ML Model Zoo examples reference](https://github.com/TexasInstruments/tinyml-modelzoo#examples-reference) for the full, up-to-date list.

## Table of contents

- [Classification](#classification)
- [Regression](#regression)
- [Forecasting](#forecasting)
- [Anomaly Detection](#anomaly-detection)
- [Audio Classification](#audio-classification)
- [Image Classification](#image-classification)
- [Radar Point Cloud Classification](#radar-point-cloud-classification)

## Classification

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Generic time series classification](../assets/icons/new/classification-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_classification)

</td>
<td>

[Generic time series classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_classification)

Classifies synthetic sine, square, and sawtooth waveforms, the simplest signal set in the modelzoo. **Start here** to learn the toolchain end-to-end - dataset loading, feature extraction, training, quantization, and compilation - before adapting the same config.yaml structure to F28P55, MSPM0G5187, CC1352, CC1354, CC2755, or CC35X1 targets.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![DC arc fault detection](../assets/icons/new/arc-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dc_arc_fault)

</td>
<td>

[DC arc fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dc_arc_fault)

*Current* - Detects DC arc faults from current waveforms on the F28P55 MCU, using FFT-based spectral feature extraction (1024-sample frames) feeding a compact CLS_1k_NPU classifier. Config variants include DSK and DSI builds plus an on-device learning configuration for adapting the model after deployment.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![AC arc fault detection](../assets/icons/new/arc-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ac_arc_fault)

</td>
<td>

[AC arc fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ac_arc_fault)

*Current* - Detects series AC arc faults on the MSPM0G5187 MCU with integrated NPU, pairing the TIDA-010971 Rogowski-coil analog front end with FFT-based feature extraction. Targets UL 1699 compliance with over 99% detection accuracy and under 150ms end-to-end latency, including masking-load immunity for devices like vacuums and dimmers.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Motor bearing fault classification](../assets/icons/new/vibration-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/motor_bearing_fault)

</td>
<td>

[Motor bearing fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/motor_bearing_fault)

*Vibration* - Classifies 6 bearing conditions - normal operation plus 5 fault types such as contamination and erosion - from 3-axis vibration data on the F28P55 MCU. Uses FFT-based spectral binning feature extraction feeding a compact CLS_1k_NPU model, with a separate anomaly-detection config also available for the same dataset.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Blower imbalance detection](../assets/icons/new/fan-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/blower_imbalance)

</td>
<td>

[Blower imbalance detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/blower_imbalance)

*Current* - Detects blade imbalance in HVAC blower motors from 3-phase current signals on the F28P55 MCU. The pipeline applies FFT-based spectral binning across 256-sample frames (8-frame concatenation) before feeding a compact CLS_1k_NPU classifier, trained on the fan_blower_imbalance dataset.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Fan blade fault classification](../assets/icons/new/fan-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fan_blade_fault_classification)

</td>
<td>

[Fan blade fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fan_blade_fault_classification)

*Accelerometer* - Classifies 4 fan blade conditions (Normal, Blade Damage, Blade Imbalance, Blade Obstruction) from an ADXL355 accelerometer wired to the F28P55 LaunchPad over SPI, with CC1312, CC1352, CC1354, CC2755, and CC35X1 also supported. The default config reaches 100% accuracy on the provided dataset.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Gearbox fault detection](../assets/icons/new/vibration-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gearbox_fault_detection)

</td>
<td>

[Gearbox fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gearbox_fault_detection)

*Vibration* - Classifies gearbox condition as healthy or broken-tooth using 4-channel accelerometer data from the SpectraQuest Gearbox Fault Diagnostics Simulator dataset, windowed into 256-sample frames. Runs on the MSPM0G5187 NPU with 1D CNN models as small as 1.2K parameters, reaching 97-100% accuracy depending on model size.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Grid fault detection](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_fault_detection)

</td>
<td>

[Grid fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_fault_detection)

*Current* - Detects abnormal AC grid conditions for EV on-board chargers (OBCs), protecting the power stage from adverse grid events. A CNN trained on a proprietary grid-fault dataset runs directly on the F29x MCU controlling the OBC, with fault categories defined using a hybrid human- and density-clustering annotation approach.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![ECG classification](../assets/icons/new/heartbeat-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ecg_classification)

</td>
<td>

[ECG classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ecg_classification)

*ECG* - Classifies electrocardiogram signals into Normal, Mild, and Other cardiac conditions using the AFE1594 analog front end feeding the MSPM0G5187 NPU (also supported on AM13E2 and F28P55). A 55K-parameter CNN (ECG_55k_NPU) processes 2500-sample frames and reaches about 97% accuracy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PIR presence detection](../assets/icons/new/motion-sensor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/pir_detection)

</td>
<td>

[PIR presence detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/pir_detection)

*PIR* - Classifies passive infrared sensor signals into human motion, background motion, and dog motion using the TIDA-010997 EdgeAI Sensor Boosterpack on the MSPM0G5187 NPU. A ~53K-parameter CNN reduces false alarms from pets and environmental noise, reaching about 92.5% accuracy with fixed-point feature extraction on-device.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Fall detection classification](../assets/icons/new/fall-detection-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fall_detection_classification)

</td>
<td>

[Fall detection classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fall_detection_classification)

*Accelerometer* - Classifies movement as a Fall or Activity of Daily Living (ADL) using the BMI270 accelerometer on the TIDA-010997 boosterpack, trained on the SisFall dataset rescaled from 13-bit to 16-bit resolution. The CLS_6k model (~6,000 parameters) runs on the MSPM0G5187 NPU in 0.67ms with 97.65% accuracy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Dynamic hand gesture recognition](../assets/icons/new/gesture-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dynamic_hand_gesture_recognition)

</td>
<td>

[Dynamic hand gesture recognition](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dynamic_hand_gesture_recognition)

*Accelerometer* - Classifies 4 dynamic hand gestures (circle, wave, tap, other) from 3-axis accelerometer data captured on TI's Sensor BoosterPack, using 256-sample windows with 25% stride. A ~55K-parameter CNN (CLS_55k_NPU) runs on the MSPM0G5187 NPU and reaches 94.46% accuracy on test data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Electrical fault classification](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/electrical_fault)

</td>
<td>

[Electrical fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/electrical_fault)

*Voltage/Current* - Classifies 3-phase transmission-line faults (line-line, line-ground, and multi-conductor combinations) from six MATLAB Simulink-modeled voltage/current channels (Va, Vb, Vc, Ia, Ib, Ic), offered as 2-class (fault/no-fault) and 6-class variants. FFT-based binning (256-sample frames into 32 features) resolves the strong multicollinearity between the raw phase channels.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Grid stability prediction](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_stability)

</td>
<td>

[Grid stability prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_stability)

*Simulated grid parameters* - Classifies a simulated 4-node star power network as stable or unstable from 12 inputs (tau, p, and g parameters per node) drawn from the UCI Electrical Grid Stability dataset. The same data also supports a regression variant that predicts a continuous stability index, useful for feature-importance and PCA-based interpretability analysis.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Gas sensor classification](../assets/icons/new/sensor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gas_sensor)

</td>
<td>

[Gas sensor classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gas_sensor)

*Gas sensor array* - Identifies gas type (ethyl acetate, isopropanol, or hexane at 100ppb) from 10 metal-oxide sensors sampled at 1Hz for 30 minutes, drawn from the UCI Gas Sensor Array dataset. The CLS_1k_NPU model runs in 535.59us on the F28P55x TI-NPU versus 4434.89us on CPU - roughly 8x faster.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Human activity recognition](../assets/icons/new/activity-recognition-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/human_activity_recognition)

</td>
<td>

[Human activity recognition](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/human_activity_recognition)

*Accelerometer/Gyroscope* - Recognizes activities (walking, jogging, sitting, standing, climbing stairs) from smartphone accelerometer/gyroscope data in the WISDM dataset. Showcases a residual-branch CNN (CLS_ResCat_3k, ~3.1K parameters, 93.84% accuracy) alongside simpler CLS_1k_NPU (94.92%) and CLS_13k_NPU (94.45%) models to demonstrate configurable branched architectures.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![NILM appliance usage classification](../assets/icons/new/appliance-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/nilm_appliance_usage_classification)

</td>
<td>

[NILM appliance usage classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/nilm_appliance_usage_classification)

*Voltage/Current* - Identifies which combination of fridge, washer/dryer, and tumble dryer are active from 5 power-metering variables (active power, voltage, current, reactive power, phase), refined from a 28-class Kaggle ESDA NILM dataset down to 4 well-populated classes. The CLS_13k_NPU model with TI-NPU quantization reaches 95.95% test accuracy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PLAID appliance identification](../assets/icons/new/appliance-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/PLAID_nilm_classification)

</td>
<td>

[PLAID appliance identification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/PLAID_nilm_classification)

*Voltage/Current* - Identifies 11 household appliance types (from air conditioners to washing machines) using the public PLAID dataset of voltage/current waveforms sampled at 30kHz. A 6-layer CNN (CLS_13k_NPU, ~13K parameters) with FFT-based feature extraction runs on the F28P55 and reaches 97.72% test accuracy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Wi-Fi CSI presence detection](../assets/icons/new/wifi-presence-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/wifi_csi_presence_detection)

</td>
<td>

[Wi-Fi CSI presence detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/wifi_csi_presence_detection)

*Wi-Fi CSI* - Detects human presence (including stationary occupants) from Wi-Fi Channel State Information across 52 subcarriers at 128Hz, with no body-worn sensors, running on the CC35X1 Wi-Fi MCU. A ~4.7K-parameter 2D CNN (SimpleCNN2D_BN_t) reaches 98.75-98.90% test accuracy across the two provided in-house datasets.

</td>
</tr>
</table>

## Regression

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Generic time series regression](../assets/icons/new/regression-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_regression)

</td>
<td>

[Generic time series regression](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_regression)

Hello-world introduction to time series regression on the TinyML ModelMaker toolchain, using a synthetic dataset where y = 1.2 sin(x) + 3.2 cos(x). Trains a 2k-parameter CNN (REGR_2k) for the F28P55 target, scored by RMSE and R². **Start here** to learn the regression toolchain before adapting it to your own dataset.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![BMS battery SOC estimation](../assets/icons/new/battery-soc-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/bms_soc_estimation)

</td>
<td>

[BMS battery SOC estimation](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/bms_soc_estimation)

*Voltage/Current/Temperature* - Estimates lithium-ion battery State of Charge on the MSPM0G5187's integrated NPU, trained on 4491 files of the public LG 18650HG2 charge/discharge dataset using voltage, current, temperature, and coulomb-count inputs. The 20k-parameter REGR_20k_NPU model reaches 2.56% test RMSE and R² of 0.99 in a 26KB flash footprint.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![MOSFET temperature prediction](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/mosfet_temp_prediction)

</td>
<td>

[MOSFET temperature prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/mosfet_temp_prediction)

*Temperature/Power* - Predicts switch case temperature on F29H85x devices by pairing a linear ARMA thermal model with an AI model (REGR_3k, an MLP) that corrects its residual error, using 20 past points each of NTC temperature and power loss plus ambient/coolant conditions. Useful where direct junction-temperature sensing is impractical.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PMSM torque measurement regression](../assets/icons/new/motor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/torque_measurement_regression)

</td>
<td>

[PMSM torque measurement regression](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/torque_measurement_regression)

*Voltage/Current/Speed/Temperature* - Predicts PMSM motor torque from 10 electrical and thermal channels (currents, voltages, speed, and winding temperatures) in the Paderborn University motor dataset, sampled at 2 Hz. With a 128-sample window, the model reaches test R² of 0.98 (RMSE 9.40) on the F28P55x target.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Induction motor speed prediction](../assets/icons/new/motor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/induction_motor_speed_prediction)

</td>
<td>

[Induction motor speed prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/induction_motor_speed_prediction)

*Voltage/Current* - Predicts three-phase induction motor speed (RPM) from a 15,000-sample simulated dataset covering voltage, current, frequency, power factor, poles, and load torque. The REGR_1k model (TINIE-accelerator compatible) runs on the F29H85x in 9.45 microseconds using just 4.3KB flash and 128B SRAM.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Washing machine load regression](../assets/icons/new/washing-machine-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/washing_machine_load_weighing)

</td>
<td>

[Washing machine load regression](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/washing_machine_load_weighing)

*Voltage/Current/Speed* - Predicts washing machine load weight (0-900g, 100g precision) from 6 motor drive signals (d/q-axis voltage and current, reference current, speed), eliminating the need for a mechanical weight sensor. The 13k-parameter REGR_13k model achieves 25.78g RMSE float and 31.23g partially quantized on the F28P55.

</td>
</tr>
</table>

## Forecasting

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Generic time series forecasting](../assets/icons/new/forecast-trend-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_forecasting)

</td>
<td>

[Generic time series forecasting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_forecasting)

Hello-world introduction to time series forecasting on the TinyML ModelMaker toolchain, using a simulated thermostat dataset where a heater cycles on below 20C and off above 24C. Configures SimpleWindow framing (frame_size 32, 2-step forecast horizon) for the F28P55. **Start here** to learn the forecasting toolchain before adapting it to your own dataset.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PMSM rotor temperature forecasting](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/forecasting_pmsm_rotor_temp)

</td>
<td>

[PMSM rotor temperature forecasting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/forecasting_pmsm_rotor_temp)

*Voltage/Current* - Forecasts permanent-magnet surface temperature in a PMSM one step ahead, using only ambient and coolant temperature, d/q-axis voltage, and phase current magnitude as inputs (no direct magnet sensor). Early warning matters because magnets permanently lose strength above roughly 150C and motor life can halve for every 10C of overheating.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![HVAC indoor temperature forecasting](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/hvac_indoor_temp_forecast)

</td>
<td>

[HVAC indoor temperature forecasting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/hvac_indoor_temp_forecast)

*Temperature* - Forecasts indoor temperature one step ahead from 5-sample histories of compressor frequency, outdoor temperature, and indoor temperature, enabling predictive HVAC control instead of reactive thresholding. The 611-parameter FCST_LSTM10 model reaches 0.30% SMAPE (R² 0.997) in float and 0.80% SMAPE after NPU quantization.

</td>
</tr>
</table>

## Anomaly Detection

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Generic time series anomaly detection](../assets/icons/new/anomaly-detection-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_anomalydetection)

</td>
<td>

[Generic time series anomaly detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/generic_timeseries_anomalydetection)

Detects abnormal frequency and amplitude shifts in a synthetic sine/cosine waveform using a 17k-parameter autoencoder (AD_17k) trained only on normal data and tested against 4 anomaly types. A 100-sample window - one full cycle at 1 Hz - is needed to tell faster or slower cycles from noise. **Start here** to learn the anomaly detection toolchain.

</td>
</tr>
</table>

## Audio Classification

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Google Speech Commands keyword spotting](../assets/icons/new/audio-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/google_speech_command)

</td>
<td>

[Google Speech Commands keyword spotting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/google_speech_command)

*Audio (MFCC)* - Keyword spotting across 10 known commands (yes, no, up, down, stop, go, left, right, on, off) plus unknown and silence, using the Google Speech Commands v0.02 dataset. Audio is converted to 10-coefficient MFCCs over 40 mel bins at 16kHz, then classified with a depthwise-separable CNN (DSCNN) sized for efficient NPU inference.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Cough detection](../assets/icons/new/cough-detection-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/cough_detection)

</td>
<td>

[Cough detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/cough_detection)

*Audio* - Binary classification (cough vs. other sounds) running fully on-device on the LP-MSPM0G5187 LaunchPad using the TinyEngine NPU, with no cloud, OS, or external ML framework required. Audio is captured via TI Edge AI Studio and classified with a TCDS-ResNet model trained on LPC-based features; the training pipeline reached 100% cough recall in validation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Glass break detection](../assets/icons/new/glass-break-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/glass_break_detection)

</td>
<td>

[Glass break detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/glass_break_detection)

*Audio (FFT)* - Detects glass-breaking acoustic signatures on the MSPM0G5187 microcontroller's integrated NPU for security and home-automation systems, combining FFT-based feature extraction with a lightweight DSCNN model (~6K parameters, ~8KB flash). Targets under 100ms response time and over 95% detection accuracy for always-on, battery-powered deployment.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Wake word detection](../assets/icons/new/wake-word-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/wake_word_detection)

</td>
<td>

[Wake word detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/wake_word_detection)

*Audio* - Listens continuously on-device for the wake word "OK Kilby," triggering downstream voice-command processing only when it's detected, so no audio ever leaves the device. Runs a filterbank-plus-TCDS-ResNet model with 2-bit quantized residual blocks on the MSPM0G5187 NPU, targeting under 200ms end-to-end detection latency for always-on, low-power listening.

</td>
</tr>
</table>

## Image Classification

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![MNIST handwritten digit classification](../assets/icons/new/vision-camera-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/MNIST_image_classification)

</td>
<td>

[MNIST handwritten digit classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/MNIST_image_classification)

*Image* - Classify handwritten digits (0-9) using the MNIST dataset on the MSPM0G5187 microcontroller, running a classic LeNet-5 CNN (~60K parameters) that reaches about 99% accuracy after INT8 quantization. **Start here** to learn the image classification toolchain.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Coffee bean classification](../assets/icons/new/coffee-bean-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/coffee_bean_classification)

</td>
<td>

[Coffee bean classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/coffee_bean_classification)

*Image* - Classify coffee bean roast level from images for visual quality inspection, running on the MSPM0G5187 microcontroller. Training uses a lightweight MobileNetV1 variant (MobileNetV1_28k_NPU, ~28K parameters) trained for 30 epochs, sized to fit NPU-based deployment on a resource-constrained MCU.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Machine readable code classification](../assets/icons/new/qr-barcode-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/machine_readable_code_classification)

</td>
<td>

[Machine readable code classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/machine_readable_code_classification)

*Image* - Classify an image as a QR code, a barcode, or neither, from low-resolution 28x28 1-channel binary images. The dataset is synthetically generated (3,000 images per class) using the Python `qrcode` and `python-barcode` libraries, so the model learns visual structure rather than decoding the codes.

</td>
</tr>
</table>

## Radar Point Cloud Classification

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Radar point cloud classification](../assets/icons/new/radar-point-cloud-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/radar_pose_and_fall_detection)

</td>
<td>

[Radar point cloud classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/radar_pose_and_fall_detection)

*Radar point cloud* - Classify human posture and falls into five classes (standing, sitting, lying, walking, falling) from mmWave point-cloud frames captured on the IWRL6432. Each frame windows together track height, velocity, and acceleration with per-point distance, height, and signal-to-noise-ratio values from the radar's point-cloud tracker output.

</td>
</tr>
</table>
