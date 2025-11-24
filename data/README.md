
📘 **Dataset Description**
1. Title of Database

Wall-Following Navigation Task with Mobile Robot SCITOS-G5

2. Sources
(a) Creators

Ananda Freire, Marcus Veloso, Guilherme A. Barreto
Department of Teleinformatics Engineering
Federal University of Ceará
Fortaleza, Ceará, Brazil

(b) Donors

Ananda Freire — anandalf@gmail.com

Guilherme Barreto — guilherme@deti.ufc.br

(c) Date Received

August 2010

3. Past Usage

Freire, A. L., Barreto, G. A., Veloso, M., & Varela, A. T. (2009).
“Short-Term Memory Mechanisms in Neural Network Learning of Robot Navigation Tasks: A Case Study.”
Proceedings of the 6th Latin American Robotics Symposium (LARS 2009),
Valparaíso, Chile, pp. 1–6.
DOI: 10.1109/LARS.2009.5418323

4. Relevant Information

Data were collected while the SCITOS-G5 mobile robot navigated a room in a clockwise wall-following pattern for four full laps.

The robot uses 24 ultrasonic sensors mounted around its body in a circular configuration.

Sensor numbering begins at the front of the robot and proceeds clockwise.

Sampling rate: 9 Hz (9 readings per second).

Provided Datasets

The archive contains 3 synchronized datasets:

(1) sensor_readings_24.data

Raw values from all 24 ultrasonic sensors, plus class label.

(2) sensor_readings_4.data

“Simplified distances”:

SD_front

SD_left

SD_right

SD_back

Each is the minimum sensor reading within a 60° sector.

(3) sensor_readings_2.data

Only SD_front and SD_left + class label.

All datasets have identical row counts (same time steps).

Purpose of Data Collection

This dataset was designed to evaluate the hypothesis that wall-following is a non-linearly separable classification problem.
Key findings:

Linear models (e.g., Perceptron) cannot reliably learn collision-free control.

Nonlinear neural networks (e.g., MLP) succeed in learning the task.

Short-term memory (e.g., using past sensor readings) dramatically improves performance:

Even the Perceptron becomes competent with temporal context.

Elman recurrent networks achieve competitive accuracy using fewer hidden units.

Input Variation

Multiple versions (24-sensor, 4-sensor, 2-sensor) were created to analyze how classifier performance depends on input dimensionality.

5. Number of Instances

5,456 samples

6. Number of Attributes

sensor_readings_24.data: 24 real-valued features + label

sensor_readings_4.data: 4 real-valued features + label

sensor_readings_2.data: 2 real-valued features + label

7. Attribute Information
File: sensor_readings_24.data
Sensor	Description	Angle
US1	Ultrasound at front	180°
US2	Ultrasound	–165°
US3	Ultrasound	–150°
US4	Ultrasound	–135°
US5	Ultrasound	–120°
US6	Ultrasound	–105°
US7	Ultrasound	–90°
US8	Ultrasound	–75°
US9	Ultrasound	–60°
US10	Ultrasound	–45°
US11	Ultrasound	–30°
US12	Ultrasound	–15°
US13	Ultrasound at back	0°
US14	Ultrasound	15°
US15	Ultrasound	30°
US16	Ultrasound	45°
US17	Ultrasound	60°
US18	Ultrasound	75°
US19	Ultrasound	90°
US20	Ultrasound	105°
US21	Ultrasound	120°
US22	Ultrasound	135°
US23	Ultrasound	150°
US24	Ultrasound	165°
Class	Target action	—

Class labels:

Move-Forward

Slight-Right-Turn

Sharp-Right-Turn

Slight-Left-Turn

File: sensor_readings_4.data

SD_front — minimum reading in front 60° arc

SD_left — minimum reading in left 60° arc

SD_right — minimum reading in right 60° arc

SD_back — minimum reading in back 60° arc

Class (same 4 behaviors as above)

File: sensor_readings_2.data

SD_front

SD_left

Class

8. Missing Values

None (all attributes fully observed)

9. Class Distribution

Move-Forward: 2205 samples (40.41%)

Sharp-Right-Turn: 2097 samples (38.43%)

Slight-Right-Turn: 826 samples (15.13%)

Slight-Left-Turn: 328 samples (6.01%)

🔗 Reference

This dataset is publicly available from the UCI Machine Learning Repository:

UCI Machine Learning Repository: Sensor Readings from a Wall-Following Robot
Creator: Ananda Freire
https://archive.ics.uci.edu/ml/datasets/Wall-Following+Robot+Navigation+Data
