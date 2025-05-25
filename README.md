Sure. Here's the completed version of your document with all necessary Windows command and batch script code filled in:

---

# Windows-basic-commands-batchscript

Ex08-Windows-basic-commands-batchscript

# AIM:

To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware

### Step 2:

Write the Windows commands / batch file. Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.

### Step 3:

Execute the necessary commands/batch file for the desired output.

# WINDOWS COMMANDS:

## Exercise 1: Basic Directory and File Operations

Create a directory named "my-folder"

## COMMAND AND OUTPUT

```cmd
mkdir my-folder
```

Remove the directory "my-folder"

## COMMAND AND OUTPUT

```cmd
rmdir my-folder
```

Create the file Rose.txt

## COMMAND AND OUTPUT

```cmd
type nul > Rose.txt
```

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

```cmd
echo Hello World > hello.txt
```

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

```cmd
copy hello.txt hello1.txt
```

Remove the file hello1.txt

## COMMAND AND OUTPUT

```cmd
del hello1.txt
```

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

```cmd
dir hello1.txt
```

List out all the associated file extensions

## COMMAND AND OUTPUT

```cmd
assoc
```

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

```cmd
fc hello.txt rose.txt
```

## Exercise 2: Advanced Batch Scripting

Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

### `hello_name.bat`

```bat
@echo off
set name=John
echo Hello, %name%
pause
```

## OUTPUT

```
Hello, John
```

Create a batch file on the desktop that checks whether a user-input number is odd or not.

### `check_odd.bat`

```bat
@echo off
:top
set /p num=Enter a number:
set /a rem=%num% %% 2
if %rem%==0 (
    echo The number is even.
) else (
    echo The number is odd.
)
:ask
set /p choice=Do you want to check another number? (Y/N):
if /i "%choice%"=="Y" goto top
if /i "%choice%"=="N" (
    echo Thank you.
    pause
    exit
)
echo Invalid input. Please enter Y or N.
goto ask
```

## OUTPUT

```
Enter a number: 5
The number is odd.
Do you want to check another number? (Y/N): Y
...
```

Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:.

### `loop_numbers.bat`

```bat
@echo off
for /l %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

```
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
```

Write a batch script to check whether a file named sample.txt exists in the current directory.

### `check_file.bat`

```bat
@echo off
if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)
pause
```

## OUTPUT

```
sample.txt exists
```

Write a batch script that displays a simple menu with three options.

### `menu_script.bat`

```bat
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Enter your choice:

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

## OUTPUT

```
1. Say Hello
2. Create a File
3. Exit
Enter your choice:
```

# RESULT:

The commands/batch files are executed successfully.
