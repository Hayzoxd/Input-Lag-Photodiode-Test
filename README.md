# Input Lag Measurement System - Test Results

The input lag measurement system is a setup that utilizes an Arduino Leonardo, a photodiode, and a switch to measure the delay between the user's input and its display on the screen. This readme presents the details of the measurement system, how it works, and the test results obtained from various scenarios.

## Measurement System Overview

The measurement system consists of the following components:

### Required Equipment:
- **Arduino Leonardo**: A programmable microcontroller with digital and analog inputs/outputs.
- **Photodiode**: A light-sensitive component that generates voltage based on received brightness.
- **Switch**: Used to initiate and terminate the measurement process.

### Connection:
- The Arduino Leonardo is connected to the computer via the USB port for programming purposes.
- The photodiode is carefully placed on the computer screen, positioned to detect changes in brightness effectively.
- The switch is connected to a digital input on the Arduino, enabling control over measurement start and stop.

### Programming:
- The Arduino program is designed to measure the time between the activation of the switch and the detection of brightness changes by the photodiode.
- Upon switch activation, the Arduino records the precise time as the start time.
- The Arduino then waits for the photodiode to detect a change in brightness on the screen (in response to the user's input).
- As soon as the change in brightness is detected, the Arduino records the time again as the arrival time.
- The program calculates the elapsed time (input lag) by subtracting the start time from the arrival time.

## Performing Multiple Measurements and Averaging

For more accuracy, multiple measurements can be conducted to calculate the average input lag. By activating the switch several times, the Arduino performs corresponding measurements, and the user can record the results to compute the average.

## Test Results

The input lag measurement system was used to perform various tests, and the following scenarios were evaluated:

1. **RAM Impact on Latency**
   - Measuring input lag under different RAM configurations to observe the impact on responsiveness.

2. **Fortnite: DirectX 11 vs. DirectX 12 vs. Performance Mode**
   - Comparing input lag in Fortnite using different DirectX versions and Performance Mode settings.

3. **144 FPS vs. 288 FPS**
   - Comparing input lag between gaming scenarios at 144 FPS and 288 FPS.

## Conclusion

The obtained results represent the average time between the user's input and the screen response, providing valuable insights into the latency between actions and displayed responses. The data obtained from these tests can be used to optimize display responsiveness based on the user's specific needs and preferences.

By leveraging this measurement system and conducting various tests, users can make informed decisions about hardware, settings, and configurations to achieve the best possible gaming or application experience.
