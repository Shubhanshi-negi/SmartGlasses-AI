_________________________________________________________________________________________________________                        
                          ASSISTIVE SMART GLASSES FOR THE BLIND AND DEAF
                      "Technology moves forward — but not always for everyone."
_______________________________________________________________________________________________________
In a world rapidly shaped by innovation, there's a section of society that technology often overlooks — those who cannot see and those who cannot hear. Acknowledging this gap, my team and I set out to build something meaningful:
AI-Powered Smart Glasses — designed with empathy, built with purpose.

These smart glasses are crafted specifically for the visually and hearing impaired, combining multiple assistive features into one wearable solution:
These glasses are designed to eventually include multiple features like object detection, navigation, sign language to speech, currency recognition, and speech-to-text. 

----------------------------------------
👁️‍🗨️ FOR BLIND INDIVIDUALS:
 OBJECT DETECTION & NAVIGATION (OBD):
Using ESP32-CAM and YOLO-based AI models, the glasses detect nearby objects and obstacles in real time.
Audio Alerts:
When an obstacle is detected, the glasses announce it through a mic embedded near the ear — guiding the user safely.

-----------------------------------------
 FOR DEAF INDIVIDUALS:
 Sign Language to Speech:
Our model captures hand landmarks via ESP32-CAM and translates sign language into audible speech — enabling two-way communication.

Speech to Text:
Converts spoken words around the user into readable text on a display, allowing the deaf to understand conversations.

Currency Recognition:
Helps users identify different currency notes accurately through visual detection.

------------------------------------------
🔧 HARDWARE INTEGRATION:
ESP32-CAM modules are embedded in the glasses.
OLED DISPLAY: The OLED display is connected to a microcontroller that receives transcribed speech from a Python-based speech recognition system. When someone speaks nearby, the system converts their voice into text using speech-to-text, and instantly sends the recognized text to the OLED via serial communication. The display then shows the message live enabling deaf users to read what’s being said around them.
Speaker: Delivers audio alerts.
Battery: power glasses for portable use

Fully wearable, low-power, and built with cost-effective hardware for accessibility.
-------------------------------------------

⚠️ This repo uses Git submodules.
> To download all parts properly, clone using this:
git clone --recurse-submodules https://github.com/Shubhanshi-negi/SmartGlasses-AI.git

If you already cloned it normally, run this:  git submodule update --init --recursive

-------------------------------------------
📁 SETUP FOR SUBMODULES

1️⃣ SignToSpeech Module:
cd SignToSpeech
pip install -r requirements.txt
📌 Important:
📁 Note:
The trained `.h5` model for SignToSpeech is not included in the repository due to size limits.  
🔗 [Download it from Google Drive](https://drive.google.com/file/d/1RoNPkZ_BzZfCE9AXmiSz6cqsDgmLKqN8/view?usp=sharing)  
After downloading, place it inside the `SignToSpeech/` directory. ( SignToSpeech/sign_language_model/ folder.)

To run:
python signtospeech.py

---------------------------------------------
2️⃣ ObjectDetectionNavigation Module:
cd ObjectDetectionNavigation
pip install -r requirements.txt
python obd.py

----------------------------------------------
🙏 FINAL NOTE-
Make sure:
1. You have a camera and mic connected
2. Your system allows camera access for OpenCV
3. Python ≥ 3.7 is recommended

-----------------------------------------------

MY CONTRIBUTION:
Currently, this repository includes the implementation of two key modules — Object Detection & Navigation and Sign Language to Speech. These were the features I developed as part of my contribution to the project.


