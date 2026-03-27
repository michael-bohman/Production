---
description: >-
  Here is where the download and installation processes are documented for all
  of the software/programs/etc. used in production
---

# Software Installation Guide

<details>

<summary>U-Center (v25.06)</summary>

U-Center is used for programming the Z9P GPS boards for the RTK/PPK Air Modules

[z9p-gps-board-programming.md](../production-documentation-1/rtk-ppk/z9p-gps-board-programming.md "mention")



1. Navigate to the following link:
   1. [https://www.u-blox.com/en/product/u-center](https://www.u-blox.com/en/product/u-center)
2. Scroll down and click 'Download' under the 'u-center' tab.
3. Extract the folder containing the installer.
4. Run the installer and follow the prompts in it.

</details>

<details>

<summary>MPLAB IPE (v5.20) IN PROGRESS</summary>

MPLAB IPE is used for programing the Comms boards for the gimbals.

NOTE: This software requires Java v1.8.0 or higher. Go to the Java tab for more.

1. Navigate to the following link:
   1. [https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide#tabs](https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide#tabs)
2. Scroll down and click 'Downloads Archive'.
3. Scroll down and find version 5.20. Click on it to download the installer.
4. Run the installer and continue through the prompts.
5. Once you come to the 'Setup Applications' screen, uncheck everything except the MPLAB IPE and the 32-bit MCUs.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt="" width="343"><figcaption></figcaption></figure>

6. Finish installing the software.

</details>

<details>

<summary>Java 1.8.0 Runtime IN PROGRESS</summary>

Java v1.8.0 or higher is required for many programs that we use. Most notably, the MPLAB IPE won't work without it.



1.

</details>

<details>

<summary>Basecam Simple BGC Partner Assistant IN PROGRESS</summary>

IN PROGRESES

</details>

<details>

<summary>Pandoc IN PROGRESS</summary>

Pandoc is used for the conversion of many different file types. We use it to convert the Markdown files from Gitbook into printable pdfs. Refer to 'Gitbook Page Export Guide'.

[gitbook-page-export-guide.md](gitbook-page-export-guide.md "mention")

</details>

<details>

<summary>MikTex IN PROGRESS</summary>

MikTex is a Latex interpreter used for the conversion of Markdown files to printable PDFs with a custom template. Refer to 'Gitbook Page Export Guide'.

[gitbook-page-export-guide.md](gitbook-page-export-guide.md "mention")



</details>

<details>

<summary>Focus App</summary>

The Focus App is used for focusing PixelScout 65Rs inside with the targets. Later, it will be used for regular 65R and 6X cameras.

[1-pixelscout-65r-focusing.md](../technical-instructions/pixel-scout/assembly-steps/1-pixelscout-65r-focusing.md "mention")



1. Navigate to the following folder in taurus.
   1. "\as-taurus.jdnet.deere.com\Production\Technical Packages\PIXELSCOUT PHASE 4\65R Focusing"
2. Copy the 'focus-app\_1.4.0.zip' file to your machine and extract it.

</details>

<details>

<summary>Pico Configurator</summary>

Pico Configurator is used to program/configure P900 boards for RTK/PPK and PixelScout Systems.

The Pico Configurator program may be run directly off of taurus without downloading anything. However, it may be a good idea to download it to your machine anyways.



1. Navigate to "\as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-32011 -- P900 Radio\_tools"
2. Copy the 'PicoConfig 1.7.zip' file to your machine and extract it where you want to use it
3. The .exe file will be in the folder once it is extracted.



</details>

