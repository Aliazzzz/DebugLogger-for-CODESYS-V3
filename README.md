# DebugLogger for CODESYS V3 

Credits and kudo's to the original poster: https://github.com/SebastianRau/Codesys2-DebugMessages


# Adds debug messages to a global array in your application

Usage:

Include the .Library,

(optional) write the actucal time to stDebugInformation.dtActualTime := SOME_DT_VAR;

call function DebugLog(...) to add a Message to the Ringbuffer. 
Parameters are:

        sMessage 	: STRING(64);
        ePriority 	: E_DebugMessagePriority;

Priorities are:

        DEBUG := 0
        INFO := 1
        WARN := 2
        ERROR := 3
        FATAL := 4

All messages will be added to the stDebugInformation Struct in Global Variables of the Library.

To change the Ringbuffer size, set the the iMaxDebugEntries constant in DebugLogParam library parameter.
