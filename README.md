# cMsgBoxAsync
A drop-in asynchronous MsgBox class for twinBASIC 

<img width="501" height="239" alt="image" src="https://github.com/user-attachments/assets/01a7356a-d6b5-4e4c-bc01-a548e085c1d5" />

Even though it's not the best way of handling things, a lot of people ask about a MsgBox that doesn't halt execution, and it's a good way to get into simple multithreading in tB.

```
'******************************************************************************
' cMsgBoxAsync v1.0
' by Jon Johnson 
'
'Last update: 29 Mar 2026
'
'A simple class to display a MsgBox asychronously, so execution does not stop.
' Class is reusable/supports multiple boxes.
' You may declare this WithEvents. This is optional, to get the results.
'
' Methods:
'  .Show(MessageText[, Style, Title, ID]) - Display a MsgBox
'  .CloseAll() - Close any open messages. These will have a result of 0.
'  .OpenCount - Number of open messages.
' Events:
'   GotResult(ID, Result) - The result for the MsgBox with given ID.
'
' The Style and Result values are the standard VBx/tB constants.
'
' When this class is terminated, any open boxes are closed. These will have a result of 0.
'
' Thanks to VanGoghGaming for helping optimize the argument passing.
'
' **REQUIREMENTS**
'   This class requires Windows Development Library for twinBASIC.
'     References->Available packages
'
' **KNOWN ISSUE** 
'    When running from the IDE, you must call .CloseAll when the class is 
'    meant to unload (Form_Unload, app exit, etc), otherwise open messages
'    will not be automatically closed. 
'    Newer tB versions may have resolved the issue.
'******************************************************************************
```
