# Multiplayer-Memory-Game
The independent final project from my participation in the Embedded in Embedded club at the University of Calgary, 2025-26

A C-based sequence memory game developed on the Nordic nRF52840 DK using Zephyr RTOS. The project integrates physical button inputs, LED outputs, and an LVGL touchscreen interface to create an interactive memory game.

## **Features**
**State-machine architecture:** Implements gameplay using Zephyr's State Machine Framework (SMF).   
**Physical controls:** Uses onboard pushbuttons to enter and reproduce sequences.   
**LED feedback:** Provides visual feedback during sequence entry, playback, and gameplay.  
**Touchscreen interface:** Uses LVGL to display interactive game regions and status messages.  
**Modular design:** Separates gameplay logic, hardware drivers, and user-interface functionality.   

## **Hardware**
Nordic nRF52840 DK  
Adafruit 2.8-inch TFT touchscreen shield  
Onboard buttons and LEDs  
Software
C  
Zephyr RTOS  
Zephyr State Machine Framework (SMF)  
LVGL  
CMake and West build system  

## **Project Structure**
src/ — Application entry point, gameplay state machine, and LCD interface  
include/ — Application header files  
drivers/ — Project-specific hardware drivers  
prj.conf — Zephyr configuration  
CMakeLists.txt — Application build configuration  
docs/ — Project documentation and hardware images  

## **Building**
**Install** Zephyr's development environment and the required SDK.  
**Install** or clone the project and its documented dependencies.  
Navigate to the **application directory** within your Zephyr workspace.  
**Build** for the nRF52840 DK with the touchscreen shield:  
west build -b nrf52840dk/nrf52840 app  

The build command assumes the application directory is named app relative to your workspace and that the required shield definition is available.  

## **Design**
The game uses a state machine to separate gameplay phases and transitions. All possible combinations of gameplay should be accounted for with  accurate detection for the correct winner. Hardware inputs are processed by the game logic, while LED outputs and the touchscreen provide   feedback. The modular architecture allows the interface, hardware drivers, and game behavior to be developed independently.  

## **Future Improvements**
Add persistent high scores and round tracking.  
Add Bluetooth BLE functionality to create custom player names.  
Create more unique touchscreen animations and visual feedback.  

## **Author**

Noah Weir Chaba  
Developed as an embedded systems project using C, Zephyr RTOS, and LVGL  
