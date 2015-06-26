# TwinCAT_3_Lib
Basic libraries, that builds upon the standard Beckhoff libraries, to help you get started using TwinCAT 3

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
