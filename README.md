PS C:\dev\Developer\whatif-core-application> pip config set global.index-url https://tools.rbspeople.com/nexus/repository/daeng-pypi-all-repos/simple
pip : The term 'pip' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ pip config set global.index-url https://tools.rbspeople.com/nexus/rep ...
+ ~~~
    + CategoryInfo          : ObjectNotFound: (pip:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
 
PS C:\dev\Developer\whatif-core-application>  py -m ensurepip --upgrade
Looking in links: c:\Users\dzikohn\AppData\Local\Temp\tmpj4ii50_v
Requirement already satisfied: pip in c:\users\dzikohn\appdata\local\python\pythoncore-3.14-64\lib\site-packages (25.2)
PS C:\dev\Developer\whatif-core-application> py get-pip.py
C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\python.exe: can't open file 'C:\\dev\\Developer\\whatif-core-application\\get-pip.py': [Errno 2] No such file or directory
PS C:\dev\Developer\whatif-core-application> py pip.pyz --help
C:\Users\dzikohn\AppData\Local\Python\pythoncore-3.14-64\python.exe: can't open file 'C:\\dev\\Developer\\whatif-core-application\\pip.pyz': [Errno 2] No such file or directory
PS C:\dev\Developer\whatif-core-application> py -m pip install --upgrade pip
Requirement already satisfied: pip in c:\users\dzikohn\appdata\local\python\pythoncore-3.14-64\lib\site-packages (25.2)
PS C:\dev\Developer\whatif-core-application> pip -v
pip : The term 'pip' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ pip -v
+ ~~~
    + CategoryInfo          : ObjectNotFound: (pip:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
 
PS C:\dev\Developer\whatif-core-application>
