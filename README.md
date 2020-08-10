# NeoPixel_Simulator

NeoPixel_Simulator is an Arduino library designed to simulate the
behavior of a 12x12 NeoPixel array using the Arduino serial monitor. 

In the real-world array, there are 145 pixels numbered from 0 to 144, but
pixel 0 is a sacrificial pixel used as a voltage level converter, so the
pixels in the array are numbered from 1 to 144

Written by Bryan Craker of Alorium Technology.
info@aloriumtech.com

The 12 x 12 array was created my Max Maxfield.
[Max's Cool Beans Blog](https://www.CliveMaxfield.com/coolbeans)
[Max's Cool Beans Blog YouTube Channel](https://www.youtube.com/channel/UCQVqp_L4hKqF1uZ3tNo5MDw)

-------------------------------------------------------------------------

NeoPixel_Simulator is based on the Adafruit_NeoPixel library from Adafruit
Industries which can be found here:

[https://github.com/adafruit/Adafruit_NeoPixel](https://github.com/adafruit/Adafruit_NeoPixel)

-------------------------------------------------------------------------

## NeoPixel_Simulator Usage:

NeoPixel_Simulator can be used by adding a define for the simulator and 
then adding an ifdef structure that  imports NeoPixel_Simulator and
redefines Adafruit_NeoPixel:

<pre><code>
#define SIMULATE_NEOS

#ifdef SIMULATE_NEOS
  #include <NeoPixel_Simulator.h>      
  #define Adafruit_NeoPixel NeoPixel_Simulator  
#else
  #include <Adafruit_NeoPixel.h>      
#endif
</code></pre>

-------------------------------------------------------------------------
