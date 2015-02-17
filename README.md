arduino-camera-wifi
===================

This is the code for the "Wireless Camera with Arduino and the CC3000 WiFi chip" article on the Open Home Automation website. The article is about taking pictures with a JPEG camera & transmitting these pictures to your computer using the CC3000 WiFi chip.

You can find the article on the Open Home Automation website:

http://www.openhomeautomation.net/wireless-camera/


===================
- Fix: lock up on sending start_request on Arduino Uno + CC3000.
- Improvement: now code read feedback from server during uploading in case error happens.
- New function: Add capture and upload function to loop so that it capture & upload
repeatedly.

Error:
- Server sometimes send partially uploaded file error back.
- Photo sometimes can be uploaded successfully, but the jpeg appears
damaged.

TODO:
- Add increased picture number.
- Avoid bit error artifact.
