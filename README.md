# Advanced Driver Fatigue Detection Alert and Alarm System

## Introduction
Our system detects driver drowsiness using sensors and advanced algorithms, providing timely alerts to prevent accidents and enhance road safety.

## Motivation
Drowsy driving causes numerous accidents and fatalities. Traditional methods are ineffective; our system offers a proactive solution to save lives and reduce economic losses.

## Objectives
1. **Detect Drowsiness**: Use sensors to identify signs like eye closure and head nodding.
2. **Real-Time Monitoring**: Continuously track driver alertness.
3. **Effective Alerts**: Provide auditory, visual, and physical warnings.
4. **User-Friendly Interface**: Ensure easy interaction and customizable settings.
5. **Data Logging**: Analyze driving behavior for insights.
6. **System Integration**: Compatible with existing in-car technologies.
7. **Cost-Effective**: Affordable and scalable solution.
8. **Safety and Reliability**: Ensure robust and reliable performance.

## Product Description
### Driver Alert System for Safer Driving
- **Real-Time Monitoring**: Detects fatigue through sensor data.
- **Predictive Alerts**: Warns drivers based on driving habits.
- **Customizable Alerts**: Offers sound, vibration, and visual warnings.
- **Helpful Feedback**: Provides immediate notifications for timely breaks.
- **Easy Integration**: Works with existing fleet management tools.
- **Scalability**: Suitable for fleets of any size.

## List of Components
1. **Camera**: Monitors driver’s face for drowsiness signs.
2. **LEDs**: Visual alerts for the driver.
3. **Buzzer**: Auditory alerts.
4. **Vibration Motor**: Physical alerts through vibrations.
5. **Microcontroller**: Manages components and algorithms.
6. **Power Supply**: Powers the system.

## Installation and Usage
1. **Install Components**: Mount the camera, LEDs, buzzer, and vibration motor.
2. **Connect Microcontroller**: Interface all components.
3. **Power Up**: Ensure stable power supply.
4. **Monitor Alerts**: Respond to warnings and customize settings.
5. **Analyze Data**: Review logged data for driving patterns.

By using this system, drivers can prevent accidents caused by drowsiness and improve overall road safety.

---

# drowsiness_yawn.py Script Features

### Key Features:
1. **Real-Time Monitoring**:
   - Captures video from a webcam to monitor the driver's face and behavior.
   
2. **Drowsiness Detection**:
   - **Eye Aspect Ratio (EAR) Calculation**: Measures eye closure to detect drowsiness.
   - **Consecutive Frame Counting**: Tracks frames with low EAR to confirm drowsiness.

3. **Yawn Detection**:
   - **Lip Distance Measurement**: Measures the distance between upper and lower lips to detect yawning.
   - **Threshold Comparison**: Identifies yawns based on a predefined distance threshold.

4. **Alert Mechanisms**:
   - **Auditory Alerts**: Uses `espeak` for spoken warnings.
   - **Buzzer Alerts**: Activates a buzzer connected to a Raspberry Pi for physical alerts.
   - **Visual Alerts**: Displays warning messages on the video feed.

5. **Camera Coverage Detection**:
   - Monitors if the camera is covered and provides visual feedback if no faces are detected for a prolonged period.

6. **Facial Landmark Detection**:
   - Uses dlib's facial landmark predictor for precise eye and lip measurements.

7. **Customizability**:
   - Adjustable thresholds and parameters for detection sensitivity.

8. **Threaded Alerts**:
   - Utilizes threading to handle alerts without interrupting the main detection process.

9. **Integration with GPIO**:
   - Controls a buzzer using Raspberry Pi GPIO pins for additional alerting.

### Usage:
- **Run the Script**: `python drowsiness_yawn.py --webcam webcam_index`
- **Monitor Alerts**: Respond to auditory, visual, and physical alerts when signs of drowsiness or yawning are detected.

By following these instructions and utilizing the provided script, users can effectively monitor and respond to signs of driver drowsiness, enhancing road safety and preventing fatigue-related accidents.
