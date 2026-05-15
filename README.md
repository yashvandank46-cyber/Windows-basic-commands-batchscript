# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

<img width="1920" height="111" alt="image" src="https://github.com/user-attachments/assets/6c6bf8d9-2539-4ef7-97c2-317d20c6616a" />





Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="489" height="165" alt="image" src="https://github.com/user-attachments/assets/a00be8c9-b1d9-4b52-8859-4ff8350eedc5" />



Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="270" height="90" alt="image" src="https://github.com/user-attachments/assets/de8a6f7c-fe2b-4c85-9d7c-f39ccbce1e72" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="1920" height="113" alt="image" src="https://github.com/user-attachments/assets/6df52f3b-c0d3-4f37-a458-30c790dfda90" />



Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="1920" height="131" alt="image" src="https://github.com/user-attachments/assets/aed6d4b3-73ea-42a9-b80a-dbcdddd11f49" />


Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="1920" height="105" alt="image" src="https://github.com/user-attachments/assets/e4590e1e-d853-481b-967d-bbfd33492ebe" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="1920" height="250" alt="image" src="https://github.com/user-attachments/assets/e9181e0c-267f-4f39-bdd2-28c11ce2da02" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="1920" height="773" alt="image" src="https://github.com/user-attachments/assets/14667adb-d304-44dd-8121-096dba459daa" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="1920" height="210" alt="image" src="https://github.com/user-attachments/assets/18edd8d6-505d-4e03-acf7-7c68bec2f8f9" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

## PROGRAM
```
@echo off
set name=John
echo Hello, %name%!
pause

```



## OUTPUT


<img width="385" height="140" alt="image" src="https://github.com/user-attachments/assets/30607c65-9aa4-4820-8641-fcf7d236f5db" />




Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.


## PROGRAM
```
@echo off

:main

set /p number=Enter a number:

set /a remainder=%number% %% 2

if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)

choice /M "Do you want to check another number"

if %errorlevel%==2 goto end

if %errorlevel%==1 goto main

:end
echo Thank you
pause
```


## OUTPUT

<img width="847" height="306" alt="image" src="https://github.com/user-attachments/assets/f9c860c2-daf0-4401-a183-68cfdd0a447f" />





Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

## PROGRAM
```
@echo off

for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)

pause
```



## OUTPUT

<img width="567" height="328" alt="image" src="https://github.com/user-attachments/assets/dc6097a8-405b-492f-b465-6da5e2b2392b" />





Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## PROGRAM
```
@echo off

if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)

pause
```

## OUTPUT

<img width="911" height="242" alt="image" src="https://github.com/user-attachments/assets/c9328cb1-31d3-44d5-9893-75ba99af2f5e" />



Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## PROGRAM
```
@echo off

:menu

echo 1. Say Hello
echo 2. Create a File
echo 3. Exit

set /p choice=Choose an option:

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu

:end
echo Goodbye!
pause
```

## OUTPUT
<img width="892" height="434" alt="image" src="https://github.com/user-attachments/assets/f8ea9610-211e-499e-8e41-fe9799955ba2" />



# RESULT:
The commands/batch files are executed successfully.

