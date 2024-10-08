<a href="https://www.microchip.com" rel="nofollow"><img src="images/microchip.png" alt="MCHP" width="300"/></a>

# MCC Melody ADC Basic Printf Example - Callbacks Implementation (PIC18F57Q43)

The [ADC Basic Printf example](https://onlinedocs.microchip.com/v2/keyword-lookup?keyword=MCC.MELODY.EXAMPLES.RUNNING.ADCC.PRINTF&version=latest&redirect=true "Analog-to-Digital Conversion (ADC) Basic Printf example"
), of the MCC Melody ADCC Example Component, is used in the Callbacks implementation.  Analog-to-Digital (A/D) conversions are taken every 500 ms, using a Timer overflow callback. The LED is toggled and the result is sent to the PC terminal.  

## Video Building This Example 

[![Video Building this Example](images/4_ADCBasicPrintf-Callbacks-VideoImage.png "Moving the ADC Basic Printf Example, from the Polled to the Callbacks.")](https://youtu.be/1MbeGngNu04?list=PLtQdQmNK_0DTA08RmyuJH4dyNrYGDGi0l)

**Video:** [Introducing MCC Melody Example Components](https://youtu.be/zK5jLiIIYvE?list=PLtQdQmNK_0DTA08RmyuJH4dyNrYGDGi0l)
(while building the Polled version of the Timer Toggle LED example).  

## MCC Melody Example Components
Example Components are a tight integration of learning material directly into MCC. This allows users to conveniently place configuration instructions side-by-side to the components they are configuring. For more information, refer to the [MCC Melody Example Components Introduction](https://onlinedocs.microchip.com/v2/keyword-lookup?keyword=MCC.MELODY.EXAMPLES&version=latest&redirect=true). 

**Note:** The image below shows the ADCC Example Component, as it would be moving to the Callbacks implementation, having implemented the Polled implementation. In this case, a diff between the two implementations is shown. 

![MCC Melody Example Components](images/ADCCExample_BasicPrintf_CallbacksFromPolled-Intro_12cm.png)


Complete projects, available in [MPLAB® Discover](https://mplab-discover.microchip.com) or GitHub, are specific to a board and microcontroller. However, the current project could be recreated on a range of supported microcontrollers by following the steps in the example component.

To explore what an example component is, as well as the difference between example and implementation, see [MCC Melody Example Components - The Basics](https://onlinedocs.microchip.com/v2/keyword-lookup?keyword=MCC.MELODY.EXAMPLES.BASICS&version=latest&redirect=true).

Example Components are related to [MCC Melody Design Patterns for Control Flow](https://onlinedocs.microchip.com/g/GUID-7CE1AEE9-2487-4E7B-B26B-93A577BA154E), which shows different standard ways to organize `main.c` and other application-level files, such as Polling, Interrupt and Callback, or State Machine Design Patterns. Users might be familiar with each of these patterns, but...
- What support does MCC Melody provide for each?
- What are the recommended ways of building on the MCC Melody generated code? 

## Software Used
- MPLAB® X IDE 6.20.0 or newer [(MPLAB® X IDE 6.20)](https://www.microchip.com/en-us/development-tools-tools-and-software/mplab-x-ide)
- MPLAB® XC8 2.46.0 or newer [(MPLAB® XC8 2.46)](https://www.microchip.com/en-us/tools-resources/develop/mplab-xc-compilers/xc8)

- MPLAB® Code Configurator (MCC) Plugin Version 5.5.1 or newer (*Tools>Plugins>Installed*, search: "MCC")
- ADC Converter with Computation (ADCC) Example Component 1.0.0 or newer
- MCC Core 5.7.1 or newer 
- MCC Melody Core 2.7.1 or newer (Communicates with the MCC core, providing views and other functionality for MCC Melody)

![MCC Core Version](images/MCC_Core_ContentLibrary_Versions.png)  


## Hardware Used
- PIC18F57Q43 Curiosity Nano [(DM164150)](https://www.microchip.com/en-us/development-tool/DM164150)
- Curiosity Nano Explorer [(EV58G97A)](https://www.microchip.com/en-us/development-tool/EV58G97A)


## Setup
All instructions required to recreate this example are listed below, under Configuration Instructions.   

![TIMER Toggle LED, Callbacks Implementation](images/ADCC_Basic_Printf_Callbacks-ConfigComplete.png)

Once the program is loaded in MPLAB X IDE, find more information from Tooltips and links next to the instructions [![Tooltip and link](images/Icon-info-circle-fill.png "Find the Tx pin from your schematic and set it in Pin Grid View.")](https://onlinedocs.microchip.com/v2/keyword-lookup?keyword=MCC.MELODY.CONFIGHELP.UART.CNANO&version=latest&redirect=true).


![Tooltips and context help](images/PinsConfiguration_SelectPinForUartTx.png)


## Operation
The image below shows the [ADCC Basic Printf example](https://onlinedocs.microchip.com/v2/keyword-lookup?keyword=MCC.MELODY.EXAMPLES.RUNNING.ADCC.PRINTF&version=latest&redirect=true
) running, using the MPLAB Data Visualizer. 

1) Click the ![Data Visualizer icon](images/Icon-MPLAB-DataVisualizer_1cm.png) icon to open the MPLAB Data Visualizer.
2) Under Debug GPIO, click the ![Add to time plot icon](images/Icon-DataVisualizer_TimePlot.png "Display as raw data on time plot.") icon, to add to the time plot.
3) Under the COMx port, associated with your board, click the ![Settings Gear](images/Icon-DataVisualizer-SettingsGear.png "sourse options") icon to set the Baud Rate to 115200. 
4) Then click the ![Display as text in the terminal icon](images/Icon-DataVisualizer_TimePlot.png "Display as raw data on time plot.") icon to display text from the COMx port on the terminal.

**Note:** If your board is not recognised by the MPLAB Data Visualizer, go to the Device Manager (Windows) to determine the COMx number.  

![Running the ADCC Basic Printf Example](images/Running%20the%20ADC%20basic%20Data%20Visualizer-Low.png)



## Summary
For more example components, open the stand-alone Content Manager ![CM_icon](images/Icon-MPLAB-CM24.png) in MCC. 

![Standalone_CM](images/MCC_ContentManager_Examples_18cm.png) 

