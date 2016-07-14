# TwinCAT_3_Lib

Special note to users and contributors
As a guideline to contribute to this library, classes' (function blocks') multi-cycle methods should always return a DINT result code.
The guidelines for result code is as follows:
CODE < 0 is defined as successful execution
CODE = 0 is defined as busy execution
CODE > 0 is defined as failed execution
Special code meanings can be encoded as a multiple of 1's or -1's.
Existing code prior to this writing (14/Jul/2016) should/might be updated to reflect this new guideline.

This library is provide as-is, and is meant to be used as a foundation to speed up your development when using TwinCAT 3. 

Serial_Communication v1.1
+ (fb)Serial_Channel
  + This function block type is the basic unit of the serial communication.
  + It supports only the EL6002/EL6022 type of BECKHOFF hardware
  + Just declare a serial_channel for each serial comm ports you need create
  + If you wish to you the standard/fast task objects, please declare your channels into an array. Ideally, also as a global variable
  + This object already contain methods to send and receive strings
+ (fb)Serial_FastBackgroundTask
  + This function block basically acts as an interface to the array of channels.
  + You will need to set the CHANNELS and COUNT properties before you can use the function block
  + Set .CHANNELS to the address of the Serial_Channel array
  + Set .COUNT to the number of channels you have created
  + It contains the method to execute the necessary fast task
+ (fb)Serial_StandardTask
  + This function block basically acts as an interface to the array of channels.
  + You will need to set the CHANNELS and COUNT properties before you can use the function block
  + Set .CHANNELS to the address of the Serial_Channel array
  + Set .COUNT to the number of channels you have created
  + It contains the method to execute the read/send strings

Motion_Library v1.1
