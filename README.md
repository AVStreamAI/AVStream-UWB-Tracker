# AVStream-UWB-Tracker
Almost stage-ready tracking system for artists tracking and controlling DMX, PTZ, sound etc.

Using Makerfabs ESP32 and Touchdesigner

![image](https://github.com/user-attachments/assets/9bab0afb-6995-4125-abd7-b03cafa6ab85)

**Install steps:**

1. Unzip (or unrar) libraries.rar
2. Install Arduino software
3. Open AVSstream_Anchor.txt and AVStream_TAG.txt in the Arduino software and copy-paste the code and convert to Arduino files
4. Install all libraries from archive libraries.rar
5. In the TAG file there are ajustable parameters in the top of the code, such are: Wifi Credentials, udpAddress, UDP Port, Calibration settings, floating distance, UWB configuration, Display configuration. Also don't forget to define TAG_ADDress.
6. In the ANCHOR file you only need to define your ANCHOR_ADD that will match your phisical device
![image](https://github.com/user-attachments/assets/fc1b9137-90b2-45cb-b729-33a5ea438197)

![image](https://github.com/user-attachments/assets/e10a0134-a3dd-436f-8e35-bd6098a6995e)

7. Then connect TAG to your USB and compile the Arduino code and upload it to the TAG.
8. Now connect each of ANCHOR to your USB, compile the code and upload it to the TAG.
9. Connect TAG and AHCNOR to the power sources (such as powerbanks) and place ANCHORS in 2 meters away for testing.
10. Turn on the TAG and wait for WiFi connection. On the TAG screen you shall see the distances to your ANCHORS in realtime.
11. Open Touchdesigner file and connect it to your local network on defined UDP port and Host.
12. You shall see the ANCHORS numbers, distances and RX power.

![image](https://github.com/user-attachments/assets/4739abfd-4ecd-4495-a934-6e80cddb3c12)

13. Feel free to edit "Script2_callbacks" of any of DAT Script to achieve your ANCHOR's numbers.
14. Check the "Position_script" DAT and set a1_a2 distance to yours real measured distance.

![image](https://github.com/user-attachments/assets/57c57ca4-8b32-4dd2-8ecd-f9988319568c)

15. Not you should see the TAG Position X and Y in Touchdesigner and also live changing MIDI outputs.
16. Please, configure your MIDI outputs commands to achieve your setup goals.
17. Now, try to move the TAG in real world and see the magic.
18. Now you can do whatever you want with these changing numbers in Touchdesigner and create your tracking installations via DMX.
19. Also you can always change DMX to any number of Audio_outputs and create multichannel automatic monitoring system where the volume, delay and equalization will changing on the fly.
