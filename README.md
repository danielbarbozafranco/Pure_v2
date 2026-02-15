## "Pure" firmware for BeagleBone

![image](https://user-images.githubusercontent.com/33607921/111271068-c02b6e00-8641-11eb-98d7-ee5cf3860a91.png)


Audio endpoint for NAA, RAAT, UPNP, AirPlay, LMS, Spotify Connect, TidalConnect and multicast
streaming. This firmware supports three types of output - USB, I2S and SPDIF. The Botic7 driver settings
for the I2S bus are located in the /boot/uEnv.txt file in the “optargs =” line. For more detailed information on driver
parameters, you can refer to the official driver support page - http://bbb.ieero.com
The launch is possible both from SD and from internal eMMC memory. When the system is fully booted, all LEDs will turn off.

This firmware has standard user settings via the web interface http://pure.local \
Shell access - root/root \
Support for this firmware - https://t.me/pure_os

### Build firmware 

./make_pure.sh 

After successful compilation, the SD image will be located in buildroot/output/images/Pure_XX_XX_202X.gz. 

To organize your own rsync update server, you need to replace the /opt/update file with your own script.


### Notes from https://puredsd.ru/

1. Download [Pure.gz](https://puredsd.ru/Pure.gz)
2. Use [Balena Etcher](https://www.balena.io/etcher) to write this file to SD (the gz archive does not need to be unpacked)
3. Insert SD to BBB.
4. Press and hold S2.
5. Connect power to BeagleBone.
6. When all four LEDs come on, release S2.
7. After a few seconds, Linux will start.
8. Connect to BBB via any webbrowser and push buttom "Copy SD to eMMC". When copying is completed, the BBB will automatically turn off.

The firmware provides automatic assignment of IP addresses using DHCP.
You can find the new IP address on your home router or run the advanced-ip-scanner program.
BeagleBone will be listed as Texas Instruments manufacturer.
Or just open http://pure.local in your web browser.

