/**
  @page BSP Example on how to use the BSP drivers
  
  @verbatim
  ******************** (C) COPYRIGHT 2013 STMicroelectronics *******************
  * @file    Examples/BSP/readme.txt  
  * @author  MCD Application Team
  * @version V1.0.0
  * @date    20-November-2015
  * @brief   Description NUCLEO-207ZG BSP description.
  ******************************************************************************
  *
  * Redistribution and use in source and binary forms, with or without modification,
  * are permitted provided that the following conditions are met:
  *   1. Redistributions of source code must retain the above copyright notice,
  *      this list of conditions and the following disclaimer.
  *   2. Redistributions in binary form must reproduce the above copyright notice,
  *      this list of conditions and the following disclaimer in the documentation
  *      and/or other materials provided with the distribution.
  *   3. Neither the name of STMicroelectronics nor the names of its contributors
  *      may be used to endorse or promote products derived from this software
  *      without specific prior written permission.
  *
  * THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
  * AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
  * IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
  * DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
  * FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
  * DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
  * SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
  * CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
  * OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
  * OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
  *   
  ******************************************************************************
   @endverbatim

@par Example Description 

The BSP examples detects the presence of Adafruit 1.8" TFT shield with joystick and uSD.

If the Adafruit shield is NOT connected, then:
 - Blue led (led2) blinks waiting the user button is pushed.
 - When user button is pressed : LED1 (green) and LED2 (blue) start blinking at high frequency.
 - Pushing user button again and again blinking frequency decreases until looping 
   to high frequency.

If the Adafruit shield is connected, then this example shows how to use the different 
functionalities of LCD, SD card and joystick by switching between tests using user button. 
  - Firstly, use the joystick button to move a pointer inside a rectangle 
    (up/down/right/left) and change the pointer color(select).
  - Secondly, this example shows how to use the different LCD features to display 
    string with different fonts, to display different shapes and to draw a bitmap.
  - Thirdly, this example shows how to erase, write and read the SD card.
At the end of the nine examples when pushing the user button the application loops 
to the beginning (first examples).

@par Directory contents 

  - BSP/Src/main.c                     Main program
  - BSP/Src/system_stm32f2xx.c         STM32F2xx system clock configuration file
  - BSP/Src/stm32f2xx_it.c             Interrupt handlers 
  - BSP/Src/joystick.c                 Joystick feature
  - BSP/Src/lcd.c                      LCD drawing features
  - BSP/Src/log.c                      LCD Log firmware functions
  - BSP/Src/sd.c                       SD features
  - BSP/Inc/main.h                     Main program header file  
  - BSP/Inc/stm32f2xx_hal_conf.h       HAL configuration file
  - BSP/Inc/stm32f2xx_it.h             Interrupt handlers header file
  - BSP/Inc/lcd_log_conf.h             lcd_log configuration template file
  - BSP/Inc/stlogo.h                   Image used for BSP example


@par Hardware and Software environment

 - This Demo runs on STM32F2xx Devices 
  
 - This example has been tested with STMicroelectronics NUCLEO-207ZG Rev.B (MB1137) 
   and can be easily tailored to any other supported device and development board.

 - NUCLEO-207ZG Set-up
   - Connect the Adafruit 1.8" TFT shield (https://www.adafruit.com/products/802)
   
   
@par How to use it ? 

In order to make the program work, you must do the following :
 - Open your preferred toolchain 
 - Rebuild all files and load your image into target memory
 - Run the application
 
      
 * <h3><center>&copy; COPYRIGHT STMicroelectronics</center></h3>
 */
