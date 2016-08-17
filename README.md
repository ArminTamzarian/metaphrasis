# Metaphrasis

A library for converting RGBA image buffer to various Wii texture formats

Metaphrasis is a static conversion class for transforming RGBA image buffers into various GX texture formats for Wii homebrew development. Metaphrasis is written in C++ and makes use of a community standard and newly developed algorithms for conversion of 32-bit RGBA data buffers into various GX texture formats common to both the Gamecube and Wii platforms.

This library was developed in-full by Armin Tamzarian with the support of developers in #wiidev on EFnet, [Chaosteil](http://wiibrew.org/wiki/User:Chaosteil) of [libwiisprite](http://wiibrew.org/wiki/Libwiisprite), and [DrTwox](http://wiibrew.org/wiki/User:DrTwox) of [GRRLIB](http://grrlib.santo.fr/wiki/wikka.php?wakka=HomePage).

## Documentation

Full Doxygen API documentation can be found at https://armintamzarian.github.io/metaphrasis for assistance with program integration.

## Installation (Source Code)

1. Extract the Metaphrasis archive.
2. Copy the contents of the src directory into your project's development path.
3. Include the Metaphrasis header file in your code using syntax such as the following:
```c
#include "Metaphrasis.h"
```

## Installation (Library)

1. Extract the Metaphrasis archive.
2. Copy the contents of the lib directory into your devKitPro/libogc directory.
3. Include the Metaphrasis header file in your code using syntax such as the following:

```c
#include "Metaphrasis.h"
```

## Usage

* Create a buffer full of 32-bit RGBA values noting both the pixel height and width of the buffer.
* Call one of the many conversion routines from within your code. (Note: All methods within the Metaphrasis class are static and thus no class instance need be allocated)

```c
uint32_t* rgba8Buffer = Metaphrasis::convertBufferToRGBA8(rgbaBuffer, bufferWidth, bufferHeight);
```

* Free your temporary RGBA value buffer if you no longer need said values.

Currently supported conversion routines are as follows:
* `convertBufferToI4`
* `convertBufferToI8`
* `convertBufferToIA4`
* `convertBufferToIA8`
* `convertBufferToRGBA8`
* `convertBufferToRGB565`
* `convertBufferToRGB5A3`
