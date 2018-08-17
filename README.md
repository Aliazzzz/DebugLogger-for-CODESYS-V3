# DebugLogger for CODESYS V3 

Credits and kudo's to the original poster: https://github.com/SebastianRau/Codesys2-DebugMessages


# Adds debug messages to a global array in your application

Usage:

Include the .Library,

*(optional) write the actucal time to stDebugInformation.dtActualTime := SOME_DT_VAR;

*(optional) to change the Ringbuffer size, set the the iMaxDebugEntries constant in DebugLogParam library parameter.

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

# To open the Array online in the CODESYS IDE; 

        open the librarary manager, 
        search for the DebugLogger, 
        double-click the GLOBALS.
