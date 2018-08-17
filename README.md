# DebugLogger for CODESYS V3 

Credits and kudo's to the original poster: https://github.com/SebastianRau/Codesys2-DebugMessages


# Adds debug messages to a global array in your application

Usage:

Include the .Library,

(optional) write the actucal time to stDebugInformation.dtActualTime := SOME_DT_VAR;

call function DebugLog(...) to add a Message to the Ringbuffer. 

Parameters are:

        sMessage 	: STRING(64);                   // Your debug log message
        ePriority 	: E_DebugMessagePriority;       // A given priority

Priorities are:

        DEBUG := 0
        INFO := 1
        WARN := 2
        ERROR := 3
        FATAL := 4

All messages will be added to the stDebugInformation Struct in Global Variables of the Library.


# Change the Ringbuffer size;

        Change iMaxDebugEntries parameter in DebugLogParam library

![Alt text](https://github.com/Aliazzzz/DebugLogger-for-CODESYS-V3/blob/master/pics/DebugLogger%20iMaxDebugEntries%20parameter%20change.png "iMaxDebugEntries Parameter Change")



# Opening the debugmessages online;

        open the librarary manager, 
        search for the DebugLogger, 
        double-click the GLOBALS.

![Alt text](https://github.com/Aliazzzz/DebugLogger-for-CODESYS-V3/blob/master/pics/GVL_DEBUG%20online.png "debug online")
![Alt text](https://github.com/Aliazzzz/DebugLogger-for-CODESYS-V3/blob/master/pics/GVL_DEBUG%20online%202.png "debug online 2")

