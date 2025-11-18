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
```
mkdir my-folder
```



Remove the directory "my-folder"

## COMMAND AND OUTPUT
```
rmdir my-folder
```
<img width="862" height="388" alt="image" src="https://github.com/user-attachments/assets/813ccebd-71f5-428b-b465-d0ba13624f5b" />


Create the file Rose.txt

## COMMAND AND OUTPUT
```
COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time
^Z

dir Rose.txt
```
<img width="933" height="194" alt="image" src="https://github.com/user-attachments/assets/666c35b3-d257-4390-87b0-feec48124d4d" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
```
echo “hello world” > hello.txt
type hello.txt
```
<img width="1025" height="164" alt="image" src="https://github.com/user-attachments/assets/76ae1200-56ec-45b2-a398-1dc8a390e4db" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
```
copy hello.txt hello1.txt
```
<img width="1261" height="416" alt="image" src="https://github.com/user-attachments/assets/ceb205d2-e83e-4955-a44d-82464dcca18f" />


Remove the file hello1.txt

## COMMAND AND OUTPUT
```
del hello1.txt
```
<img width="1021" height="58" alt="image" src="https://github.com/user-attachments/assets/e851e3ce-6929-4b77-b589-fab182de0692" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
```
dir hello1.txt
```
<img width="1036" height="289" alt="image" src="https://github.com/user-attachments/assets/a3e5b671-4426-4a2b-a4bf-18ed5b7e9004" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
```
assoc | more
```
<img width="854" height="752" alt="image" src="https://github.com/user-attachments/assets/ff724556-449c-4cb3-acfc-3879b79bd0bb" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
```
fc hello.txt Rose.txt
```
<img width="927" height="233" alt="image" src="https://github.com/user-attachments/assets/b9f73b2a-7382-4888-89b7-2a519b44e63f" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```
## OUTPUT
<img width="753" height="91" alt="image" src="https://github.com/user-attachments/assets/5f599b15-3e11-47b6-8376-51c270f788c5" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```
## OUTPUT
<img width="731" height="249" alt="image" src="https://github.com/user-attachments/assets/904d1fb2-1c3d-4cc1-810b-8726f41ba222" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```
## OUTPUT
<img width="719" height="173" alt="image" src="https://github.com/user-attachments/assets/723a8be3-a17d-4e03-af61-bc0fa3290050" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
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
<img width="936" height="326" alt="image" src="https://github.com/user-attachments/assets/0701498c-7614-4fa6-b0c2-b88188d7b364" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

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
<img width="731" height="458" alt="image" src="https://github.com/user-attachments/assets/15621b6b-05f1-4725-8174-bc3901ffe9b5" />



# RESULT:
The commands/batch files are executed successfully.

