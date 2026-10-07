# Smart Vehicle Vision System with Image Recognition and Automatic Headlight Control

## I. AI and Autonomous Systems Applications

Artificial Intelligence (AI) and Autonomous Driver Assistive Systems (ADAS) are transforming modern transportation by improving road safety, driving efficiency, visibility, and reducing human errors. These systems combine Computer Vision, Deep Learning, Image Recognition, and Machine Learning to perceive the driving environment and assist drivers in making safer decisions.

Some major applications include:

- **Object Detection and Recognition:** Detects vehicles, pedestrians, obstacles, and other road objects using computer vision.
- **Traffic Sign and Traffic Light Recognition:** Recognizes important road signs and traffic signal states to assist the driver.
- **Lane Detection and Lane Keeping Assistance:** Identifies lane boundaries and supports safer lane positioning.
- **Driver Monitoring Systems:** Uses AI-based visual analysis to identify driver attention and fatigue-related conditions.
- **Automatic Headlight Control:** Adjusts headlight operation according to road, traffic, and ambient lighting conditions.
- **Night-Time Driving Assistance:** Improves visibility by intelligently controlling headlights in low-light environments.
- **Image-Based Road Scene Understanding:** Analyzes camera images to understand the surrounding driving environment in real time.

### Limitations in the Domain

Although AI-based ADAS technologies have made significant progress, several challenges remain:

- Computer vision performance can decrease under low-light, rain, fog, and other adverse environmental conditions.
- Image recognition models require large and high-quality datasets for reliable performance.
- Real-time image processing may require significant computational resources.
- Objects such as vehicles and pedestrians can be difficult to recognize correctly in crowded or poorly illuminated scenes.
- Automatic headlight decisions may be affected by changing road conditions, glare, and varying illumination.
- AI-based systems may provide limited explainability for decisions made from visual inputs.

### Future Scope

- Integration of advanced deep learning models for improved object and road-scene recognition.
- Use of multi-sensor fusion combining cameras with LiDAR, radar, GPS, or other sensors.
- Edge AI deployment for faster real-time inference inside vehicles.
- Integration of Explainable AI (XAI) to improve transparency and user trust.
- Adaptive beam control and intelligent high-beam/low-beam switching based on detected traffic.
- Continuous learning and improved performance under low-light and adverse weather conditions.

---

# II. Proposed Project

## Project Title

**Smart Vehicle Vision System with Image Recognition and Automatic Headlight Control**

### Description

The proposed project aims to develop an intelligent vehicle vision system that continuously analyzes the driving environment using Computer Vision, Image Recognition, and Deep Learning techniques.

The system uses camera-based visual information to identify vehicles, pedestrians, obstacles, and relevant road conditions while assisting the driver during different lighting conditions.

A major component of the proposed system is **automatic headlight control**. Based on the detected ambient lighting and surrounding vehicles, the system determines an appropriate headlight state to improve road visibility and reduce unnecessary glare to other road users.

The system combines image-based perception with an intelligent decision-making mechanism to provide a practical driver assistance solution, particularly for night-time and low-light driving scenarios.

---

# III. Objectives

### Objective 1

Develop a Computer Vision and Image Recognition pipeline capable of identifying vehicles, pedestrians, obstacles, and relevant road conditions from camera input.

### Objective 2

Implement an intelligent lighting-condition detection module to determine whether the vehicle is operating under daytime, night-time, or low-light conditions.

### Objective 3

Design an automatic headlight control mechanism that selects suitable headlight operation based on ambient lighting and detected surrounding vehicles.

### Objective 4

Evaluate the system under different road and lighting scenarios and analyze its effectiveness in improving visibility and reducing unnecessary headlight glare.

---

# IV. Team Members

1. **ALURU SRI TEJASWI PRIYANK** – Roll Number: **2420030276**
2. **GAJJELLI VINEET** – Roll Number: **2420030375**
3. **VENKATA SATYA MAHIDHAR MAHADEVA** – Roll Number: **2420030756**
4. **MADDINENI ROHITH** – Roll Number: **2420030783**
5. **KARNATI SRIKAR** – Roll Number: **2420090111**

---

# V. Datasets Used

The proposed system uses two datasets to support road-scene understanding, object detection, and low-light image analysis.

## 1. BDD100K Dataset

The BDD100K dataset is used for real-world driving-scene analysis and object detection. It provides diverse road images containing vehicles, pedestrians, traffic signs, traffic lights, and other objects commonly found in driving environments.

### Dataset Link

https://www.kaggle.com/datasets/solesensei/solesensei_bdd100k

### Usage in the Project

- Vehicle detection
- Pedestrian detection
- Road-scene understanding
- Traffic-object recognition
- Object detection under driving conditions
- Analysis of different driving environments

---

## 2. ExDark Dataset

The ExDark (Exclusively Dark) dataset contains images captured under different low-light conditions. It is useful for evaluating object detection and image recognition when illumination is limited.

### Dataset Link

https://www.kaggle.com/datasets/washingtongold/exdark-dataset

### Usage in the Project

- Low-light image analysis
- Dark-environment object detection
- Vehicle detection under poor illumination
- People/pedestrian detection
- Evaluation of detection performance under dark conditions
- Testing image-processing and enhancement techniques

---

# VI. Night-Time Driving and Intelligent Headlight Control

Good visibility of the road ahead is an important requirement for safe night-time driving. During night-time, high beams can improve visibility, but improper use may cause glare and discomfort to other road users.

Therefore, an intelligent automatic headlight-control system can help determine when high beams and low beams should be used.

The proposed project uses camera-based computer vision to analyse the surrounding road environment. The system identifies vehicles, pedestrians, and other relevant objects and considers the lighting condition of the scene.

The BDD100K dataset provides diverse driving-scene images for road-scene and object detection, while the ExDark dataset provides low-light images for evaluating object recognition under challenging illumination conditions.

The combination of these datasets supports the development of a vehicle vision system capable of analysing both normal and low-light driving environments.

---

# VII. Proposed System Workflow

The proposed system follows the workflow:

**Camera Input → Image Preprocessing → Lighting Condition Detection → Object Detection → Vehicle Identification → Headlight Decision → Output**

### 1. Camera Input

The system receives images or video frames captured from a vehicle-mounted camera.

### 2. Image Preprocessing

The input image is processed using techniques such as resizing, noise reduction, normalization, and colour-space conversion.

### 3. Lighting Condition Detection

The system determines whether the scene represents:

- Daytime
- Night-time
- Low-light conditions

### 4. Object Detection

The object detection model identifies important road objects such as:

- Cars
- Buses
- Trucks
- Motorcycles
- Pedestrians
- Traffic signs
- Traffic lights

### 5. Vehicle Identification

The system determines whether detected objects are vehicles and identifies their position in the scene.

### 6. Headlight Decision

Based on the lighting conditions and detected surrounding vehicles, the system determines an appropriate headlight state.

Possible outputs include:

- **HIGH BEAM**
- **LOW BEAM**
- **AUTOMATIC / NORMAL**

### 7. Output

The final output displays detected objects, bounding boxes, confidence values, and the recommended headlight state.

---

# VIII. Automatic Headlight Control

The automatic headlight-control mechanism is one of the main components of the proposed system.

A simplified decision mechanism can be represented as:

```text
                    Input Image
                         |
                         v
                Lighting Detection
                         |
              +----------+----------+
              |                     |
           Daytime             Night / Low Light
                                    |
                                    v
                            Vehicle Detection
                                    |
                         +----------+----------+
                         |                     |
                  Vehicle Detected       No Vehicle
                         |                     |
                         v                     v
                     LOW BEAM              HIGH BEAM
