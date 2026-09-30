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

Classify sine/square/sawtooth waveforms. **Start here** to learn the toolchain.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![DC arc fault detection](../assets/icons/new/arc-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dc_arc_fault)

</td>
<td>

[DC arc fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dc_arc_fault)

*Current* - Detect DC arc faults from current waveforms for electrical safety.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![AC arc fault detection](../assets/icons/new/arc-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ac_arc_fault)

</td>
<td>

[AC arc fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ac_arc_fault)

*Current* - Detect AC arc faults in electrical systems.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Motor bearing fault classification](../assets/icons/new/vibration-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/motor_bearing_fault)

</td>
<td>

[Motor bearing fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/motor_bearing_fault)

*Vibration* - Classify 5 bearing fault types + normal operation from vibration data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Blower imbalance detection](../assets/icons/new/fan-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/blower_imbalance)

</td>
<td>

[Blower imbalance detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/blower_imbalance)

*Current* - Detect blade imbalance in HVAC blowers using 3-phase motor currents.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Fan blade fault classification](../assets/icons/new/fan-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fan_blade_fault_classification)

</td>
<td>

[Fan blade fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fan_blade_fault_classification)

*Accelerometer* - Detect faults in BLDC fans from accelerometer data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Gearbox fault detection](../assets/icons/new/vibration-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gearbox_fault_detection)

</td>
<td>

[Gearbox fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gearbox_fault_detection)

*Vibration* - Classify gearbox operating conditions (healthy vs broken tooth) from vibration data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Grid fault detection](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_fault_detection)

</td>
<td>

[Grid fault detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_fault_detection)

*Current* - Detect electrical grid faults from sensor data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![ECG classification](../assets/icons/new/heartbeat-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ecg_classification)

</td>
<td>

[ECG classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/ecg_classification)

*ECG* - Classify normal vs anomalous heartbeats from ECG signals.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PIR presence detection](../assets/icons/new/motion-sensor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/pir_detection)

</td>
<td>

[PIR presence detection](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/pir_detection)

*PIR* - Detect presence/motion using PIR sensor data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Fall detection classification](../assets/icons/new/fall-detection-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fall_detection_classification)

</td>
<td>

[Fall detection classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/fall_detection_classification)

*Accelerometer* - Detect and classify Human Fall vs Activities of Daily Living (ADL).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Dynamic hand gesture recognition](../assets/icons/new/gesture-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dynamic_hand_gesture_recognition)

</td>
<td>

[Dynamic hand gesture recognition](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/dynamic_hand_gesture_recognition)

*Accelerometer* - Classify 4 dynamic hand gestures (circle, wave, tap, other) from 3-axis accelerometer data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Electrical fault classification](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/electrical_fault)

</td>
<td>

[Electrical fault classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/electrical_fault)

*Voltage/Current* - Classify transmission line faults using voltage and current (2-class and 6-class variants).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Grid stability prediction](../assets/icons/new/grid-fault-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_stability)

</td>
<td>

[Grid stability prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/grid_stability)

*Simulated grid parameters* - Predict power grid stability from node parameters.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Gas sensor classification](../assets/icons/new/sensor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gas_sensor)

</td>
<td>

[Gas sensor classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/gas_sensor)

*Gas sensor array* - Identify gas type and concentration from sensor array data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Human activity recognition](../assets/icons/new/activity-recognition-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/branched_model_parameters)

</td>
<td>

[Human activity recognition](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/branched_model_parameters)

*Accelerometer/Gyroscope* - Human Activity Recognition from accelerometer/gyroscope data.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![NILM appliance usage classification](../assets/icons/new/appliance-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/nilm_appliance_usage_classification)

</td>
<td>

[NILM appliance usage classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/nilm_appliance_usage_classification)

*Voltage/Current* - Non-Intrusive Load Monitoring - identify active appliances.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PLAID appliance identification](../assets/icons/new/appliance-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/PLAID_nilm_classification)

</td>
<td>

[PLAID appliance identification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/PLAID_nilm_classification)

*Voltage/Current* - Appliance identification using the PLAID dataset.

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

Generic regression example for continuous value prediction.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![MOSFET temperature prediction](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/mosfet_temp_prediction)

</td>
<td>

[MOSFET temperature prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/mosfet_temp_prediction)

*Temperature/Power* - Predict MOSFET temperature from electrical parameters.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PMSM torque measurement regression](../assets/icons/new/motor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/torque_measurement_regression)

</td>
<td>

[PMSM torque measurement regression](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/torque_measurement_regression)

*Voltage/Current/Speed/Temperature* - Predict PMSM motor torque from current measurements.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Induction motor speed prediction](../assets/icons/new/motor-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/induction_motor_speed_prediction)

</td>
<td>

[Induction motor speed prediction](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/induction_motor_speed_prediction)

*Voltage/Current* - Predict induction motor speed from electrical signals.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Washing machine load regression](../assets/icons/new/washing-machine-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/reg_washing_machine)

</td>
<td>

[Washing machine load regression](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/reg_washing_machine)

*Voltage/Current/Speed* - Predict washing machine load weight.

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

Generic forecasting example for time series prediction.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PMSM rotor temperature forecasting](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/forecasting_pmsm_rotor_temp)

</td>
<td>

[PMSM rotor temperature forecasting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/forecasting_pmsm_rotor_temp)

*Voltage/Current* - Forecast PMSM rotor winding temperature.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![HVAC indoor temperature forecasting](../assets/icons/new/temperature-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/hvac_indoor_temp_forecast)

</td>
<td>

[HVAC indoor temperature forecasting](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/hvac_indoor_temp_forecast)

*Temperature* - Predict indoor temperature for HVAC control.

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

Detect abnormal frequency/amplitude patterns in a synthetic waveform using an autoencoder. **Start here** to learn the anomaly detection toolchain.

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

*Audio (MFCC)* - Keyword spotting across 10 known commands plus unknown/silence, using the Google Speech Commands dataset.

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

*Image* - Classify handwritten digits (0-9) using the MNIST dataset. **Start here** to learn the image classification toolchain.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Coffee bean classification](../assets/icons/new/coffee-bean-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/coffee_bean_classification)

</td>
<td>

[Coffee bean classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/coffee_bean_classification)

*Image* - Classify coffee bean roast level from images for visual quality inspection.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Machine readable code classification](../assets/icons/new/qr-barcode-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/machine_readable_code_classification)

</td>
<td>

[Machine readable code classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/machine_readable_code_classification)

*Image* - Classify an image as a QR code, a barcode, or neither, from low-resolution 28x28 images.

</td>
</tr>
</table>

## Radar Point Cloud Classification

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Radar point cloud classification](../assets/icons/new/point-cloud-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/radar_point_cloud_classification)

</td>
<td>

[Radar point cloud classification](https://github.com/TexasInstruments/tinyml-modelzoo/tree/main/examples/radar_point_cloud_classification)

*Radar point cloud* - Detect human presence, pose, and falls from mmWave radar point-cloud frames (IWRL6432).

</td>
</tr>
</table>
