arduino-camera-wifi
===================

This is the code for the "Wireless Camera with Arduino and the CC3000 WiFi chip" article on the Open Home Automation website. The article is about taking pictures with a JPEG camera & transmitting these pictures to your computer using the CC3000 WiFi chip.

You can find the article on the Open Home Automation website:

http://www.openhomeautomation.net/wireless-camera/


===================
Modifycation:
- Fix: lock up on sending start_request on Arduino Uno + CC3000.
- Improvement: now it read feedback from server during uploading in case error happens.
- New function: add a capture and a upload function to the loop function so that it captures & uploads
repeatedly without reset.

Camera.php
- Made the feedback clear so that you can see the result by byte number directly in Apache's access_log. It is
> cat /var/log/apache2/access_log 
on my Mac OS Yosemite. 
You should see "POST /camera.php HTTP/1.1" 200" with one more number after it. 
If the number is 1, then the photo was uploaded successfully.

Error:
- Server sometimes send partially uploaded error back.
- Photo sometimes can be uploaded successfully, but the jpeg appears damaged.

TODO:
- Add increased picture number.
- Avoid bit error artifact.
