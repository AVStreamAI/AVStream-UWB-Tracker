# AVStream-UWB-Tracker
Almost stage-ready tracking system for artists tracking and controlling DMX, PTZ, sound etc.

The main idea is to create tracking device, that can be wired in the Artist, and then this Artist walking on the stage (in the Theater for example) and DMX lighting, PTZ cameras and even Audio Monitoring or Immersive system follows this Artist. So you see the lights are moving itself and follow Artist, the sound mixing automatically in monitoring system and PTZ cameras follows Artist and making autonomous streaming or/and video recording.

Please keep in mind that you should have **phisical ESP32** from Makerfabs to make this project live.

**I don't provide any technical support on this project, so you can adjust and configure it in your own way.**

I've used as ANCHORS:
![image](https://github.com/user-attachments/assets/fb5a7468-4486-4ceb-8390-29fee5c816b5)

As TAGS:
![image](https://github.com/user-attachments/assets/100cfc5a-23b6-4f1b-8020-dc920eb33b4f)

So you can figure out where and how to buy it yourselfe.

Using Makerfabs ESP32 and Touchdesigner

![image](https://github.com/user-attachments/assets/9bab0afb-6995-4125-abd7-b03cafa6ab85)

**Install steps:**

1. Unzip (or unrar) libraries.rar
2. Install Arduino software
3. Open AVSstream_Anchor.txt and AVStream_TAG.txt in the Arduino software and copy-paste the code and convert to Arduino files
4. Install all libraries from archive libraries.rar (maybe some of them are not neccessary, but I provide the project as it works for me)

![image](https://github.com/user-attachments/assets/1638b518-eef1-4bd0-9772-225348c60a62)

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

**PTZ Setup**

It's more complicated, but you can handle it i believe.

1. Connect your PTZ camera to your local network
2. Define it's IP
3. Open your Python environment and add VISCA PAN PARSER.txt to your .py
4. Change IP address to your PTZ ip address.
5. Run the code
6. Change your PTZ pan position. You should see the numbers in HEX of your PTZ positions.
7. Move your PTZ pan from left end to right end.
8. Copy these numbers. You should get almost 4096 of these positions.
9. Paste them to any table editor (Excel) and define the centre. You need only few of them to control your PTZ.
10. Define the PTZ position you need and
11. Open AVStream_UWB_PTZ_DEMO.toe in Touchdesigner and correct the "Script3_callbacks" DAT according to your HEX's positions

![image](https://github.com/user-attachments/assets/8cf95456-80e9-48f0-98d9-3a2dca5a8082)

12. I have tested only on 2 different PTZ cameras and each of them has different PAN numbers. So before start, parse yours PTZ.
13. The same you can do with VISCA TILT PARSER.txt
14. Now do the 1-10 steps from first list above and prepare your physical TAG and ANCHORS setup
15. Connect everything to the same network and double-check all addresses.
16. Now try to move the TAG in physical world, so you will see the PTZ should move somewhere.
17. Calibrate the HEX positions, PTZ placement, ANCHORS placement to achieve correct PTZ movement.
18. Enjoy.

My tg: https://t.me/Kvanterbreher
My tg channel: https://t.me/avstream
