# CircuitPython and Mu

## Getting set up

For this course we will be using a microcontroller board called the [Feather M4 Express](https://www.adafruit.com/product/3857) made by Adafruit. Feather M4 Express is too long to keep typing out, so let's call it the "M4" from here on. To work with this board we will need to -

- set up an easy to use editor called Mu
- grab the files we need from Adafruit

Let's get started!

## Set up the Mu editor

Open a web browser and navigate to the [Mu](https://codewith.mu/en/download) download site. Take a moment to check out the top of this page - see the Tutorials heading? Might be handy later. Select the Mu Installer version for your operating system and click the "Download" button (*the green colored one is probably the corrrect one!*). Now just follow the installation Instructions.

## Set up the needed CircuitPython files on your computer

We need a bunch of CircuitPythin files to make things work. To keep track of things it may be best to create a new folder to contain all the files... I think my folder is called "CircuitPython". Once that is available, let's download three (3) .zip archives:
- the [Adafruit CircuitPython bundle](https://github.com/adafruit/Adafruit_CircuitPython_Bundle/releases/download/20240618/adafruit-circuitpython-bundle-9.x-mpy-20240618.zip)
- the [Adafruit CircuitPython bundle examples](https://github.com/adafruit/Adafruit_CircuitPython_Bundle/releases/download/20240618/adafruit-circuitpython-bundle-examples-20240618.zip )
- the [Adafruit CircuitPython Neopixel 9.x library](http://github.com/adafruit/Adafruit_CircuitPython_NeoPixel/releases/download/6.3.11/adafruit-circuitpython-neopixel-9.x-mpy-6.3.11.zip )

Once these are all in the folder, we can go into the folder and click the "extract here" button. Your computer should extract each .zip archive into a folder with a similar name and all the files should be there.

Whew! Glad that's all done!! Now we can move on and get the hardware working...

## Making sure the firmware on the M4 is current

We need to make sure that we are using the latest stable firmware on the M4. Let's do this!

### Get the latest stable .UF2 file
- To get the latest stable release we visit the [Feather M4 Express](https://circuitpython.org/board/feather_m4_express/) page. Here on the top right hand side we see "CircuitPython 9.x.x" and that this is the latest **stable** release the will work with the M4. Click the Download .UF2 Now button and save the file to a location you can remember.

### Connect the M4 to your computer
- Use a USB cable to connect the M4 to your computer. The type of cable will depend on the type of USB ports available on your computer.
- two things should happen:
  - the neopixel LED should light and start changing colors, and
  - a new drive should appear with the name CIRCUITPYTHON

### Transfer the new .UF2 onto the M4

To program the .UF2 file onto the M4 we need to put it in "programming mode". To do this, double click the reset button on the M4.

![image of M4 highlighting reset button](./assets/feather_M4_express_reset.jpg?raw=true)

The LED will stop cycling through colors and display a constant green. If this doesn't work the first time, don't worry... Just try again with about half a second between button clicks. Sometimes it takes a few tries to get used to the M4.

Once you are in programing mode, the drive name will change to FEATHERBOOT. Yay!

Now all we do is "drag" the .UF2 file that was downloaded onto the FEATHERBOOT icon. When you do this the M4 LEDs should blink (indicating data transfer) and then the M4 wil reset itself and after a few seconds the CIRCUITPYTHON drive will reappear.
