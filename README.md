
PS C:\dev\Developer\whatif-workspace\backend\template-backend> .venv\Scripts\activate
.venv\Scripts\activate : The module '.venv' could not be loaded. For more information, run 'Import-Module .venv'.
At line:1 char:1
+ .venv\Scripts\activate
+ ~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (.venv\Scripts\activate:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CouldNotAutoLoadModule
 
PS C:\dev\Developer\whatif-workspace\backend\template-backend> Import-Module .venv
Import-Module : The specified module '.venv' was not loaded because no valid module file was found in any module directory.
At line:1 char:1
+ Import-Module .venv
+ ~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ResourceUnavailable: (.venv:String) [Import-Module], FileNotFoundException
    + FullyQualifiedErrorId : Modules_ModuleNotFound,Microsoft.PowerShell.Commands.ImportModuleCommand
 
PS C:\dev\Developer\whatif-workspace\backend\template-backend> python -V
Python 3.14.0
PS C:\dev\Developer\whatif-workspace\backend\template-backend>
