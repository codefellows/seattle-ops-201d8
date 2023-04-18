# Hello World

The tutorial discusses shell programming in general with focus on **PowerShell** as the main shell interpreter. Shell programming using other common shells such as sh, csh, tcsh, will also be referenced, as they sometime differ from PowerShell.

Shell programming can be accomplished by directly executing shell commands at the shell prompt or by storing them in the order of execution, in a text file, called a shell script, and then executing the shell script. To execute, simply write the shell script file name, once the file has execute permission.

Unlike bash scripts, the first line of the shell script file **does not** need to begin with a "sha-bang" (#!). It is common to name the shell script with the ".ps1" extension. The file extension tells the computer to use PowerShell as the shell interpreter.

Adding comments: any text following the "#" is considered a comment

To find out what is currently active shell, and what is its path, type the highlighted command at the shell prompt (sample responses follow):

**`Get-Process -Name *shell`**

    Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
    -------  ------    -----      -----     ------     --  -- -----------
    629      32        64380      77604       0.91   5972   1 powershell

This response shows that the shell you are using is of type 'powershell'. next find out the full path of the shell interpreter

**`Get-Command powershell`**

    CommandType     Name                                               Version          Source
    -----------     ----                                               -------          ------
    Application     powershell.exe                                     10.0.19041.546   C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe


This response shows the full execution path of the shell interpreter.

## Exercise

Use the "echo" command to print the line "Hello, World!".

### Tutorial Code

    # Text to the right of a '#' is treated as a comment - below is the shell command
    echo 'Goodbye, World!'

### Expected Output

    Hello, World!

### Solution

```powershell
# Text to the right of a '#' is treated as a comment - below is the shell command
echo 'Hello, World!'
```
*Adapted from learnshell.org*
