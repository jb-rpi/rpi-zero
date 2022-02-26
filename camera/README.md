First idea is being able to capture images and videos from the rpi zero.

We install buster-lite distribution on the sd card (requires buring with Etcher, create a blank ssh file and create the wpa_supplicant.conf).

Everything is describe here:

https://www.raspberrypi-spy.co.uk/2017/04/manually-setting-up-pi-wifi-using-wpa_supplicant-conf/

The wpa_supplicant.conf is as follows:

country=fr

update_config=1

ctrl_interface=/var/run/wpa_supplicant

network={

 scan_ssid=1
 
 ssid="Livebox-ABCD"
 
 psk="Pa55w0rd1234"
 
}


We can then log with ssh using pi/raspberry credentials.

Change the password and activate the camera with 'rapsi-config'

Install then the picamera relying on this documentation:

https://picamera.readthedocs.io/en/release-1.10/install3.html#raspbian-installation


$ sudo apt-get update

$ sudo apt-get install python3-picamera


The rpi zero is now ready.


