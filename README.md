# qtp-reporter
An html report library for HP QTP

This is a free html report generator for HP QTP. It uses the program's functions to crete an html report file. Please read the instructions in order to use the library correctly. You can update an existing project or directly use this library in any new project.

Instructions:
Each test should start by calling the testStarted function.
Each test should end by calling the testFinished function.
Each action should start by calling the actionStarted function.
Each action should end by calling the actionFinished function.

The following verification (assertion) functions are used:

verificationPassed (verificationMessage) - Use this function to assert a successful checkpoint. Provide a message to be tracked in the report file. Also triggers the micPass event of QTP.

verificationFailed (verificationMessage, screenShotName) - Use this function to assert a failed checkpoint. This function will take a screenshot of the active desktop at the time of failure. The screenshot will be accessible in the html report. Provide a message to be tracked in the report file and a name for the screenshot. Also triggers the micFail event of QTP.

verificationFailed_NoScreenShot (verificationMessage) - Use this function to assert a failed checkpoint. Provide a message to be tracked in the report file. No screenshot will be taken through this function. Also triggers the micFail event of QTP.

verificationInfo (verificationMessage) - Use this function to log information messages in the report file. Provide the message to be logged. Also triggers the micDone event of QTP.

verificationWarn (verificationMessage) - Use this function to track warnings in the log file. Provide the message to be logged. Also triggers the micWarn event of QTP.
