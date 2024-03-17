---
title: 'Blog Post number 1'
date: 2024-03-15
permalink: /posts/2024/03/YoLo_Model_for_ESD_Test/
tags:
  - Yolo v8
  - vision tracking
  - machine Learning
---
=
Lean Idea: Automated ESD Test Data Logging with AI
=
Problem:

•	Traditional ESD testing requires manual recording of test level, tip type, and discharge location - inefficient and prone to errors.
Solution:

•	Visual Object Detection:
o	Implement a YOLO model to track the location of the tip in real-time and distinguish between two discharge tips a video camera.
•	Voice Recognition:
o	Integrate VOSK for voice command recognition. Automatically response to voice command like “mark”, “exit” etc. 
•	Data Logging:
o	Upon hearing "Mark", the system automatically records:
	Test level: Preset based on test configuration.
	Tip type: Identified by the YOLO model.
	Discharge location: Bounding box from the video frame.
Benefits:
•	Single-operator testing: Automates data logging, enabling one person to conduct the entire test.
•	Improved efficiency: Eliminates manual data entry and reduces errors.
•	Enhanced data accuracy: Real-time location tracking ensures precise recording.
Additional Lean aspects:
•	Focuses on core functionality: Addresses the primary issue of manual data logging.
•	Modular design: YOLO and VOSK models can be integrated with existing testing equipment.
•	Scalability: The system can be adapted to accommodate different test setups and tip variations.
Training Steps:
•	Take pictures or shoot video of the ESD gun for image training. 
•	Upload the pictures or videos to roboflow.com to start labeling 
•	Download the prepared dataset for training. 
•	Deploy the trained weight to yolo model and run on the local machine. 

Headings are cool
======

You can have many headings
======

Aren't headings cool?
------