# STM32F

Use Arduino compatible Nucleo-F446RE and STM32CubeIDE.

## 0. Setup

* Download and Install [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
* Create new STM32 project using board selector = `NUCLEO-F446RE` (In my case)
* Build Project (it should compile)

## 1. Hello World

* insert [ITM Code](https://raw.githubusercontent.com/niekiran/Embedded-C/master/All_source_codes/target/itm_send_data.c)
into syscalls.c.
* Replace `io_putchar` with `ITM_SendChar` in _write
* Add printf to main.c
* Build Project
* Debug As -> Debug Configuration
  * Enable Serial Wire Viewer (SWV) and then press `Debug`
* Debug As STM32
* Window -> Show View -> SWV -> SWV Item Data Console
* Configure trace -> Enable ITM Stimulus Port 0
* Press Red Circle for `Start Trace` next to ITM Data Window
* Press Green Triangle `Resume` on top bar
* The message should have been printed out
  
