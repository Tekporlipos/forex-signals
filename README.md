PS C:\Windows\system32> Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile C:\dev\wslubuntu.appx -UseBasicParsing
Invoke-WebRequest : Received an unexpected EOF or 0 bytes from the transport stream.
At line:1 char:1
+ Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile C:\dev\w ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Invoke-WebRequest], IOException
    + FullyQualifiedErrorId : System.IO.IOException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand

PS C:\Windows\system32>
