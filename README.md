# Fade-LED

The main task is to write the program and control the intensity and brightness of a LED

Step -1:Gather the material from the IoT kit:
● 1 x ESP32
● 1 x USB Cable
● 1 x Breadboard
● 4 x Jumper wires
● 1 x LED
● 1 x Resistor

Step -2: Let’s do connections:
● Supply positive(VCC (+ve)) from the ESP 32 to breadboard terminal
● Supply negative(GND (-ve)) from the ESP 32 to breadboard negative terminal
● Insert the Led into the breadboard
● Connect the longer leg of the LED to one end of the resistor
● Connect another end of the resistor with the ESP32 PIN 32 of the Breadboard
● Connect shorter Leg of the breadboard with the GND

Step-3 Now let's write a program:

Define Pins
● define GPIO pin for LED, led_gpio =32
● define brightness =0
● define fadeAmount =5

Initialize the setup()
● ledcAttachPin function accepts two arguments. The first is the GPIO that will output the signal, and the second is the channel that will generate the signal.
● Set Channel i.e=0, frequency. i.e. 4000 and resolution i.e 8

To execute the main process write the void loop()
We need to control the LED brightness in this main function
● ledCWrite function is used to control the LED brightness, it will take two arguments channels and brightness
● Declare the variable brightness and change the brightness level using brightness and fade Amount
● Write the condition using if condition, if brightness is less than 0 and more than 255, then decrease the fadeAmount value.
● Set up delay for 30 ms

Output:
Compile and upload the program to ESP32 board using Arduino IDE
● Verify the program by clicking the Tick option
● Upload the program by clicking the arrow option

Note: If the port is not selected, insert the USB cable in Computer’s port and select the port

Go to Tools and select Serial Monitor
● See the brightness of the LED and Value
