# USB-keyboard-to-OMEGA-converter
A converter for connecting a 'qwerty' or 'azerty' USB keyboard to the keyboard port of the MSX2 OMEGA computer

**Released under the cc-by-sa-4.0 license for non-commercial use**

![USB CONVERTER](/images/USB-Converter-3D.png)

## Reference of the components used in the design

|Value|	Designator|	Footprint|	Quantity|	Manufacturer Part|	Manufacturer|
|-----|-----------|-----------|---------|-------------------|-------------|  
|3.3uF|	C1|	CAP-SMD_L3.5-W2.8-R-RD|	1|	T491B335K016AT|	KEMET|
|100uF|	C3|	CAP-SMD_L3.5-W2.8-R-RD|	1|	TAJB107M010RNJ|	AVX|
|10uF|	C6|	C0805|	1|	0805F106M160NT|	FH|
|100nF|	C7,C4,C5,C2|	C0805|	4|	CL21B104KCFNNNE|	SAMSUNG|
|2510S-4P|	CN1|	CONN-TH_4P-P2.54_A2510S-4P|	1|	2510S-4P|	Shenzhen Cankemeng|
|DS1023-2*8SF11|	H1|	HDR-TH_16P-P2.54-V-M-R2-C8-S2.54|	1|	DS1023-2*8SF11|	CONNFLY|
|17-21/G6C-FM1N2B/3T|	LED1|	LED0805-RD|	1|	17-21/G6C-FM1N2B/3T|	EVERLIGHT|
|330R|	R1|	R0805|	1|	TC0525B3300T5E|	UniOhm|
|1Ω|	R2|	R1206|	1|	RT1206BRD071RL|	YAGEO|
|1K|	R3|	R0805|	1|	0805W8F1001T5E|	UniOhm|
|100M|	R4|	R0805|	1|	0805W8F1006T5E|	Uniroyal Elec|
|CH9350L|	U1|	LQFP-48_L7.0-W7.0-P0.50-LS9.0-BL|	1|	CH9350L|	WCH|
|STM32G030C8T6|	U2|	LQFP-48_L7.0-W7.0-P0.50-LS9.0-BL|	1|	STM32G030C8T6|	STMicroelectronics|
|LM1117MPX-3.3/NOPB|	U3|	SOT-223-3_L6.5-W3.4-P2.30-LS7.0-BR|	1|	LM1117MPX-3.3/NOPB|	TI|
|USB-A-F-90-H9.5|	USB1|	USB-A-TH_C168725|	1|	USB-A-F-90-H9.5|	LCSC|

Note: This list is given as an indication. Please report any errors to sillycony@mailo.com

## Resource files:

Gerber file 'Gerber_PCB_USB KEYBOARD CONVERTER.zip' -> You can provide this file directly to the PCB manufacturer.

Elf files -> Choose the appropriate file for the type of keyboard used, 'azerty' OR 'qwerty'. The selected file must be programmed in the STM processor.

## Tools:

To program the processor, you will need to use an STLINK V2 type interface. This type of USB interface is easily found for a few dollars.

![USB CONVERTER](/images/STLINK_V2.jpg)

With this dongle, you will use the STM32CubeProgrammer software to program the processor flash.

![USB CONVERTER](/images/STMCubeProgrammer.jpg)

You can download this software free to use at [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html).

All of these tools are very easy to use and shouldn't cause you any problems.

## USB keyboard specific keys.

For both types of keyboard, 'azerty' and 'qwerty', the left modifier keys are used in this way:

|USB Keyboard|	OMEGA Keyboard|
|-----|-----------|
|LEFT-SHIFT| SHIFT|
|LEFT-CTRL| CTRL|
|LEFT-SYSTEM| GRAPH|
|LEFT-ALT| CODE|
|MAJ| CAPS LOCK|

On the 'azerty' type keyboard, the right modifiers key RIGHT-SHIFT and RIGHT-ALTGR are used to obtain characters which are not natively arranged in the same way as on the 'qwerty' keyboard such as the character '\\' for example.

Once the converter has been produced and programmed, all you have to do is insert it into the keyboard connector of the Omega board and connect a USB keyboard to it.

![USB CONVERTER](/images/USBKeyboardtoOMEGA.jpg)

 However, be careful when inserting to place the converter well in the center of the OMEGA connector otherwise the pins may be shifted. This is, in principle, not dangerous for either the Omega board or the converter, but will prevent the computer from starting.
 
Enjoy and do not hesitate to let me know of your difficulties in assembly or use. This converter can also be adapted to other types of vintage computers other than Omega.

## Examples of adaptation for other MSX boards.

Konkotgit, https://github.com/konkotgit/JFF, created an MSX1 compatible board :

![Konkotgit](/Other_implementations/jff_r_1_1_01_s.jpg)

Due to the different design compared to the OMEGA card, Konkotgit has worked out a new implementation of this adapter which uses the same programming 'elf' file :

![Konkotgit](/Other_implementations/usb_keyboard_adapter.jpg)

## IMPORTANT UPDATE 2023-02-27.

- Fixed 'Esc' key code on QWERTY (US) keyboard.
- Addition of support management for *TWO SIMULTANEOUS KEYS* pressed for both keyboards (FR) & (US).


## sillycony@mailo.com
