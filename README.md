# NeoPixel_Simulator

NeoPixel_Simulator is an Arduino library designed to simulate the
behavior of a 12x12 NeoPixel array using the Arduino serial monitor. 

Written by Bryan Craker of Alorium Technology.
info@aloriumtech.com

NeoPixel_Simulator is based on the Adafruit_NeoPixel library from Adafruit
Industries which can be found here:

https://github.com/adafruit/Adafruit_NeoPixel

-------------------------------------------------------------------------

## NeoPixel_Simulator Usage:

NeoPixel_Simulator can be used by adding a define for the simulator and 
then adding an ifdef structure that  imports NeoPixel_Simulator and
redefines Adafruit_NeoPixel:

\#define SIMULATE_NEOS

\#ifdef SIMULATE_NEOS

 
\#include <NeoPixel_Simulator.h>      
\#define Adafruit_NeoPixel NeoPixel_Simulator  

\#else

\#include <Adafruit_NeoPixel.h>      

\#endif

-------------------------------------------------------------------------
