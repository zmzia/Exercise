Queries raised in the social medium and the received responses(if any)
StackOVerflow  

Q.1.Simple print statement is not working in python .py when converted to .exe using pyinstaller
Python file contains one line print statement
#file1.py
print("python to exe")
Converted the .py file to .exe using pyinstaller Library in the windows environment successfully and got the executable file 'file1.exe'
pyinstaller --onefile -w 'file1.py'
Tried executing the 'file1.exe' in the command line prompt, the .exe neither prints nor shows any error. Any help is appreciated

Answer
This is because you're using the "-w" option. On Windows this will disable the console window when running the program. From the pyinstaller documentation:
-w, --windowed, --noconsole
Windows and Mac OS X: do not provide a console window for standard i/o. On Mac OS X this also triggers building an OS X .app bundle. On Windows this option will be set if the first script is a ‘.pyw’ file. This option is ignored in *NIX systems

Q.2. Pyinstaller generates .exe of huge filesize
