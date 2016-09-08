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
