---
modified_at: 2026-06-12T16:33:04-05:00
---
# Jellyfish PCB Card
A custom-designed PCB Business card inspired by [isayx](https://forge.hackclub.com/projects/342) & [ghastly](https://forge.hackclub.com/projects/369). The main goal was to include an NFC chip/antenna to send a portfolio and a heart-rate sensor linked to LEDs as a fun way to create interactions.

I mainly worked on this because I wanted to challenge to construct my fully polished PCB device, and to get my foot in the door in learning electronics, KiCAD, and some SVG editors.



## Schematic
![Schematic](images/Schematic.png)

## Silkscreen
![FrontS](images/FrontSilkscreen.png)
![BackS](images/BackSilkscreen.png)

## PCB Layout
![FrontC](images/FrontCopper.png)
![BackC](images/BackCopper.png)
![FullC](images/FullCopper.png)
> Note: Ground Pour on Back Layer is not shown in these images
![FullLay](images/FullLayout.png)

## 3D Render
![FrontR](images/FrontSilkscreen3D.png)
![BackR](images/BackSilkscreen3D.png)


## Bill of Materials (BOM)

| Part        | Description        | Qty | Source Link   |
| :---------- | :----------------- | :-- | :------------ |
| ATtiny85    | Microcontroller    | 1   | [Insert Link] |
| NT3H2211    | NXP I2C NFC Tag    | 1   | [Insert Link] |
| MAX30102    | Heart Rate Sensor  | 1   | [Insert Link] |
| CR2032 Clip | SMT Battery Holder | 1   | [Insert Link] |
| 0805 Parts  | Resistors/LEDs     | 6   | [Insert Link] |
