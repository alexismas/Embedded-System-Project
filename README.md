# Embedded-System-Project

cmd : 

sudo apt-get update
sudo apt-get update && apt-get upgrade -y
sudo apt-get install apache2 php
sudo apt-get install -y ssmtp mailutils mpack
apt-get install i2c-tools
sudo chmod g+w -R /var/www/ 
ls -al /var/www/html
sudo adduser www-data gpio
sudo adduser www-data users
sudo adduser www-data i2c
sudo adduser pi i2c
sudo raspi-config 
« activate i2c »
sudo reboot 
ls -l dev/i2c*
i2cdetect -y 1



chmod -R 777 /var/www/html/projet/

Upload : 

scp -r /Users/alexismassol/OneDrive/Documents/ESILV/S08/Embedded\ Systems\ \ architecture\ \&\ programming/Lab\ 5-8-9/projet pi@192.168.2.7:/var/www/html/projet


Save :

 scp -r pi@192.168.2.7:/var/www/html/projet /Users/alexismassol/OneDrive/Documents/ESILV/S08/Embedded\ Systems\ \ architecture\ \&\ programming/Lab\ 5-8-9/projet 


- I2C :

gcc final.c -o final -lwiringPi

https://www.pihomeserver.fr/2013/08/13/raspberry-pi-home-server-arduino-lier-les-deux-via-bus-i2c/

http://www.gammon.com.au/images/ArduinoUno_R3_Pinouts.png

https://docs.microsoft.com/en-us/windows/iot-core/media/pinmappingsrpi/rp2_pinout.png


- Email : 

Link : https://www.pihomeserver.fr/2015/08/13/envoyer-un-email-depuis-votre-raspberry-pi/

 sudo nano /etc/ssmtp/ssmtp.conf 

Add :

mailhub=smtp.gmail.com:587
AuthUser=. . .@gmail.com
AuthPass=. . . 
useSTARTTLS=YES
useTLS=YES

Test : 

 echo " Hello" | mail -s "This is the subject line" your email
