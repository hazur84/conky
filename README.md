conky-theme-hatz
=====

My first conky theme for Lubuntu 14.04 LTS

    I have optimized it for 1920x1080 resolution. You can edit it.

Installation Notes:
===================

 Package Dependencies
 
     sudo apt-get install lm-sensors,hd-temp,curl,conky-all,dmidecode

After installing above packages you need to change permission of following packages

    sudo chmod u+s /usr/sbin/hddtemp
    sudo chmod u+s /usr/sbin/dmidecode
    
*other wise don't display hardware information and data weather.
 
You need to install Poky.ttf.

Install the "Poky.ttf" font by placing it in your $HOME/.fonts folder.


Install conkyrc file:
======================

Copy or remplace "conkyrc" into the home folder.

Setting conkyrc file:
======================

Now go to http://weather.yahoo.com and search you city
you will get a zip code of your city like '1915035' into urls.
Now copy the zip code and open 'conkyrc'.

Search the section "## - WEATHER - ##" and the line:

'${exec l=116545;curl -s http://weather.yahooapis.com/forec'....

replace code numbers with yours & save the file. By defual the file set "Mexico City"


Search the section "## - NETWORK - ##" and change your network interfaces (eth0, wlan0, wla1, etc). By default the file set "eth0"
To quickly identify all available network interfaces, you can use this command as shown below:

    sudo ifconfig
    sudo iwconfig

save the file and now add conky to start up application.

How to add startup applications in lubuntu?

1.Press the Lubuntu icon on the bottom left;
2.Select "Preferences" > "Default applications for LXSession";
3.In the opened window, select the option "Autostart";
4.Now you can enable or disable the autostarted applications, check/uncheck one in the listm or set manually on the field and pressing the "Add" button.

    conky -p 6

Enjoy :)

Changelogs:
==========

v1.1  -   August 28, 2014

 + Add Local Weather Temperature (crawler from Yahoo Weather)
 + Add Date Long Format
 + Add Running Threads, Total Threads
 + Change Screenshot Readme

Screenshot:
==========
<img src='ScreenShot_v1_1.png’ alt='image' />

v1.0  -   August 27, 2014

+ First version
+ Direct Crawling Yahoo Weather

Screenshot:
==========
<img src='ScreenShot_v1_0.png' alt='image' />


