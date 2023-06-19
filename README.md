# Zonai Watch Face for Wear OS
Tears of the Kingdom Zonai themed Wear OS facewatch. This project is to be used by everyone for free.

This facewatch was created using Samsung's Watch Face Studion.

The reason this watch face was not published on Play Store is because is a fee to create an account for publishing items there, so I'll be providing a "maybe not so correct" step by step instructions on how it was created and how to get it to your smartwatch. **This process requires enabling the "DEVELOPER OPTIONS" on your Wear OS smartwatch**, instructions can be followed here: https://developer.android.com/training/wearables/get-started/debugging.

I have no prior experience with this type of project, but this is a simple one that looked pretty good and I want to share it with people.

![zonai](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/4d7b2d7c-e42a-4514-a8c1-dc9ac69a9264)

In case you don't want to go over the creation process, please use the Zonai.WFS file provided in this repository as a starting point and go to the "How to get it to your smartwatch" step.

## How to create it

1. Ensure you donwload and install the Watch Face Studio app from the link https://developer.samsung.com/watch-face-studio/download.html;

2. Download the amazing font "THE WILD BREATH OF ZELDA" from the link https://zeldauniverse.net/media/fonts/ or from https://www.fontspace.com/the-wild-breath-of-zelda-font-f25653, and install it in your system;

3. Download the two images in this repository, bg-black.png and ZeldaTOAK-OuroborosLogo-1200x1104.png.

4. Open Watch Face Studio, import both images into the project. At the top, click the "Add Component", select "Digital Clock > Time", repeate the process for "Digital Clock > Date" and for "Text" (which will be used to display the battery charge). Spend some time organizing and resizing everything, you should have something like this:

![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/98d2d7bc-f3c9-420e-a58c-c17feff1ec3b)


5. Now to configure the components:
   - Click the TEXT component, go to its properties tab and, under the text field, add "[BATT_PER]%" without the quotes, and select a color for it (I selected #E0FFF7).
![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/c5d8cd70-b77e-4d67-9de7-9c00bff7df02)
   - Click the image for the Zonai green ourobouros dragon. Find the ROTATE option under properties, click on the "TAGS" button that shows up when you hover the input field. Add the text "-6*[SEC_MSEC]" without quotes, this will make it so the ourobouros does a full rotation every minute.
     - If you want it to rotate at a different speed, you'll need some extra math to ensure it does exactly a full rotation every cycle, or it will suddenly reset to the starting position before getting to it. You might have to use some other TAGS for it.
![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/f65fa26e-f8c6-4528-92d0-236d0628c14c)
   - For the DATE and TIME components, you'll need to update the font. Click on them, scroll down a bit on the properties tab and look for the "text appearance" option. Click on the font, click on ADD FONT. Select the .TTF version of the font downloaded here, and then select it at the top of the list.
![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/37c480a3-348b-454a-8cdb-f1eee70500b9)
     - If you want a custom text for the date, you can rearange the tags a little bit. Mine is "([DAY_WEEK_S]) ([DAY_1_31_Z]) ([MON_S])" which only puts a space between the tags.
  - **At the top of your components, click the "ALWAYS ON" tab. In it, hide the Zonai green ourobouros image, otherwise it will complain about "too many bright pixels" for the "always on" mode.**
![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/b38f77a2-1da0-43d5-a7bb-03a459f31ce6)
   - With everything ready, save it as a .WFS file.
    
## How to get it to your smartwatch

First of all, you need the developer options enabled on your smartwatch, to do that, follow the steps here: https://developer.android.com/training/wearables/get-started/debugging.

With developer options ready, connect to the same network your device with Face Watch Studio is connected, access "developer options", search for "debugging over WiFi" or "debugging over wireless" and enable this option. It will show you an IP address and PORT, take note of that. On that same screen, there should be an option to pair with a new device, it'll give you a verification code and another IP address + PORT combination, take note on that code and port number.

Go back to Face Watch Studio, click on "Run on Device" at the top right corner of the window, click on the PLUS "+" button and add the first IP Address, the first PORT, the CODE and the SECOND PORT.

![image](https://github.com/Nujaka/ZonaiWatchFace/assets/9707452/55f1dcdc-8c6c-4a69-a6c2-9bfddaaf806a)

Clicking OK and clicking "Scan Devices" should show your watch there. With that, you can not click on it, wait a few minutes and have the facewatch you just created on your smartwatch!

## DISCLAIMER

I am aware this is my first project developing and sharing a watch face for smartwatches, and I might not be following the best practices. I do not intend on paying to create a Google Play developer account to publish a single item, and my decision was to make it available on GitHub. Any suggestions for improving this repository or deploying this facewatch for free to everyone in a better way is welcome.
