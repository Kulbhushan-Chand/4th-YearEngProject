making a change in github and see change in osf 
 
 test from laptop

[![DOI](https://zenodo.org/badge/93779121.svg)](https://zenodo.org/badge/latestdoi/93779121)


# Fourth-Year Engineering Project

#### Monitoring of Arduino-based PPG and GSR Signals through an Android Device


The following is a fourth-year engineering project at Carleton University, for the study period 2015 – 2016...


##### Abstract

  The purpose of this project is to provide heart rate readings and to monitor the influence of biological stress (as indicated by skin conductance) on the heart rate. The developed system monitors and processes PhotoPlethysmoGraph (PPG) and Galvanic Skin Response (GSR) signals. A PPG sensor is used to estimate a person’s heart rate, and a GSR sensor is used to detect the person’s skin conductance. An Arduino microcontroller is paired with an Android device via a Bluetooth Low Energy (BLE) wireless connection, to monitor the signals received from the Arduino microcontroller. Such a system could be used in hospitals, for home-care, or by athletes, students, and people suffering from heart diseases. However, the primary audience is vulnerable people who need home-care.


##### Background

  Medical and engineering worlds are highly related nowadays. Most of the technologies used in hospitals are established by engineers. Developers have always been working to put Android and iOS devices into better use [1]. Health applications have become a stock feature in both Android and iOS devices, and some existing applications claim to measure heart rate [1]. Despite the large number of existing technologies and/or applications, estimating reliable heart rate readings has always been an issue in the medical world [2]. There are many technologies that have been developed to estimate heart rate, but they are rather expensive. Nonetheless, there are many factors that could affect someone’s heart rate such as motion, emotions, and stress.
 
  Currently, the growth of flexible electronics, smart materials, low-power computing, and networking have reduced the barriers to technology accessibility, integration, and cost [2]. Specifically, wearable sensor technology is continually advancing and applying significant improvements to personalized healthcare [2]. There has been a surge in the usages of wearable sensors, especially in the medical field, where there are many different applications in monitoring physiological activities [3].  In the medical field, it is possible to monitor a patient’s body temperature, heart rate, brain activity, muscle motion, and other critical parameters [3]. It is important to have very light sensors that could be worn on the body to perform standard medical monitoring [3]. In the area of athletics there is an increasing trend of using various wearable sensors [3]. For instance, the measurement of sweat rate was possible only in the laboratory based system a few years back, and is now possible using wearable sensors [3]. 
 
  The use of wearable sensors has made it possible to have the necessary treatment at home for patients suffering from heart-attacks, sleep apnea, and Parkinson disease [3]. After an operation, patients usually go through a recovery/rehabilitation process where they must follow a strict routine [3]. All the physiological signals as well as physical activities of the patient could be monitored with the help of wearable sensors [3]. During the rehabilitation stage the wearable sensors may provide audio feedback, virtual reality images, or other rehabilitative services [3]. The system can be tuned to the requirements of an individual patient [3]. The whole activity can be monitored remotely by doctors, nurses, or caregivers [3]. Reliably detecting and alerting wearers and/or caregivers to abnormal physiological conditions with sufficiently high sensitivity will be critical in order to achieve a wider spread of adoption, and acceptance of semi-automated or closed-loop systems [2]. 
 
 
##### Solution
 
  Recent studies have shown that changes in the levels of biological stress influence the heart rate [4]. In fact, the pumping process of the heart and in turn the blood flow throughout the body may be affected by changes in physiological stress [4]. One way to measure the heart rate of a person is through analyzing a PPG signal. PPG is a procedure that determines the change in blood volume pulse (usually in the soft tissues of the body) using the direct relationship between variations in volume and the absorption, reflection, and scattering of the light from a photo-emitter and then recorded by the photo-receptor [4]. The changes in the pulsatile flow of the arterial blood are then represented in a PPG waveform, which can then be used to extract useful information such as a person’s heart rate. The modern way of estimating physiological stress is through the changes in skin conductance. GSR is a technique used to measure the changes in the skin conductance, usually to indicate an estimate of the level of biological stress [5]. Both PPG and GSR sensors can be used to indicate how stress affects the heart rate by a simultaneous analysis of their corresponding waveforms. 
  
  With regards to our proposed solution, a PPG sensor and a GSR sensor are interfacing with a 3.3/5 volts Arduino microcontroller to acquire the required signals. The GSR sensor is used for detecting the stress level, while the PPG sensor is used for estimating the heart rate. An Android (4.3+) application is developed to monitor the PPG and the GSR signals. The Arduino microcontroller interacts with the Android device through a wireless serial BLE connection. Standard algorithms for deriving parameters from PPG and GSR signals are available [6], [7]. These algorithms are adapted to the acquired signals, and converted into the Android application. The derived parameters can be used to help in finding a correlation between PPG and GSR signals. 
  
  
##### Description

  The project is divided into two parts, the Arduino circuitry and the Android application. Hence, the system consists of two subsystems; the first subsystem is composed of an Arduino microcontroller and two sensors (i.e. PPG and GSR sensors), while the second subsystem is composed of an Android monitoring application. Generally speaking, all signal acquisition will be done within the Arduino microcontroller subsystem. Android (4.3+) is the platform used to develop the application, while the Android device is simply a receiver and a sender. It receives the PPG and GSR sensor readings along with the heart rate as it sends the start/stop command for the acquisition of each signal to the Arduino microcontroller. The Android application then plots the corresponding waveforms, and processes them to extract related parameters. The inter-communication between the Arduino microcontroller and the Android device is established through a BLE connection. The figure below shows a higher level diagram of the system.
  
  ![alt tag](https://github.com/Itaf/4th-YearEngProject/blob/master/TheBigPicture.png)
  
  The two sensors are connected to a Grove shield that is mounted on top of an Arduino microcontroller. The GSR sensor that is used has Grove connectors, thus a Grove shield is needed for pairing it with the Arduino microcontroller. The Grove shield identifies the corresponding pins of the Arduino microcontroller, and allows the connection of additional sensors and/or other shields.
  
  
##### Accomplishments
  
  The milestones of the project are as follows: 
  
    ● Requirements Elicitation and Analysis 
        ○ Brainstorming ○ Researching and Reading
        
    ● System Design 
        ○ Block Diagram 
        ○ Circuit Diagram 
        ○ UML Diagrams 
        
    ● Implementation and Development 
        ○ Develop a working circuit using Arduino UNO, a PPG sensor, a GSR sensor, and a BLE module 
        ○ Create an Arduino sketch/code(s) to link with the Arduino board 
        ○ Adapt the Arduino sketch/code(s) to identify the on-board pins properly 
             ■ Wiring code (in C) 
        ○ Acquire PPG and GSR signals from the Arduino board 
        ○ Write algorithms to process the acquired PPG and GSR signals 
             ■ Processing code (in C) 
        ○ Extract parameters from the PPG and GSR signals and analyse them to find any possible correlation between the signals 
        ○ Create an Arduino sketch/code to send the acquired signals via BLE 
        ○ Establish a BLE connection between Arduino and an Android device 
             ■ Client-Server application (in Java) 
        ○ Develop an Android application to monitor the acquired signals and extracted parameters 
             ■ GUI (in XML) 
             ■ Functionality (in Java) 
        ○ Modify the application to invoke a notification for irregular heart rates  
        ○ Add extra useful features to the application 
        
    ● Verification and Validation of the System 
        ○ Test the system on human subjects
  
  The team was able to accomplish all of the proposed milestones. A working circuit consisting of an Arduino UNO microcontroller, a PPG sensor, a GSR sensor, and a BLE module was developed. The Graphical User Interface (GUI) of the Android application was developed, and the application’s functionalities were implemented. Also, both PPG and GSR signals were successfully displayed on the developed application. Application users would now be able to register multiple patients’ profiles, connect to the Arduino microcontroller, monitor the PPG and GSR signals, and share information with a selected emergency contact (preferably a doctor). Furthermore, the team performed an analysis on the acquired signals by extracting statistical parameters and conducting various experiments for the verification and validation of the product. 
  
  
##### Impact

  Every year, over 15 million people worldwide suffer from heart attacks, and nearly 6 million people die [8]. A heart attack can also lead to disabilities such as paralysis, and loss of speech [8]. Globally, heart attacks are the second leading cause of death in people above the age of 60 years old, and the fifth leading cause of death in people aged 15 to 59 years old [8]. On the other hand, heart attacks are less common in people under 40 years old, although it does occur [8]. It would be very helpful if those people’s heart rate could be monitored on a daily basis. If stress is left unmanaged, it can lead to emotional, psychological, physical problems, heart disease, high blood pressure, chest pains, or irregular heartbeats [9]. The general motivation of this project is to estimate heart rate variability in conjunction with stress levels as indicated by skin conductance. Nonetheless, most medical devices are very expensive and not affordable by a group of people in our community [10]. The developed system facilitates medical attention, care, and support to the vulnerable population of elderly and/or disabled people, monitors heart rate variability, and irregular heartbeats (i.e. Arrhythmia). The developed system helps in the early detection of heart diseases’ symptoms, and post heart attack or stroke recovery.
  
  
##### References

  [1] F. Wahab ,2014. Are Heart Rate Monitoring Apps Really Accurate? We Put Them To The Test [Online]. Available: http://www.addictivetips.com/ios/are-heart-rate-monitoring-apps-really-accurate-we-put-them-to-the-test/  

  [2] M. M. Rodgers, et al. (eds.), “Recent Advances in Wearable Sensors for Health Monitoring,” in IEEE Sensors Journal, VOL. 15, NO. 6, June 2015. 

  [3] S. C. Mukhopadhyay, “Wearable Sensors for Human Activity Monitoring: A Review,” in IEEE Sensors Journal, VOL. 15, NO. 3, March 2015. 
  
  [4]  J. G. Webster and J. W. Clark, et al. (eds.), Medical instrumentation: application and design, 4th ed. Hoboken, NJ: John Wiley & Sons, 2010. 
  
  [5] M. V. Villarejo, et al. (eds.), “A Stress Sensor Based on Galvanic Skin Response (GSR) Controlled by ZigBee,” in Sensors Journal, 2012, 6075-6101.  
  
  [6] Biopac, “Heart Rate Variability,” in Application Note 129 [Online]. Available: https://www.biopac.com/wp-content/uploads/app129.pdf. 
  
  [7]  J. H.D.M. Westerink, et al. (eds.), “Computing Emotion Awareness through Galvanic Skin Response and Facial Electrography,” in Probing Experience, 149-162  [Online]. Available: http://eprints.eemcs.utwente.nl/20853/01/Westerink08-Computing_emotional_awareness.pdf  
  
  [8] K. Skaarhoj, 2015. Stroke - The global burden of stroke [Online]. Available: http://www.world-heartfederation.org/cardiovascular-health/stroke/.  
  
  [9] M. C. Stöppler. Heart Disease and Stress [Online]. Available: http://www.medicinenet.com/stress_and_heart_disease/article.htm.
  
  [10] J. Tozzi, 2014. How Much Do Medical Devices Cost? Doctors Have No Idea [Online]. Available: http://www.bloomberg.com/news/articles/2014-01-23/how-much-do-medical-devices-cost-doctors-have-no-idea.
