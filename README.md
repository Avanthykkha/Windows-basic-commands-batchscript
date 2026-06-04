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

<img width="376" height="62" alt="image" src="https://github.com/user-attachments/assets/6063b54f-888c-46ff-9426-0a5d785a3d0c" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT

Create the file Rose.txt

<img width="382" height="54" alt="image" src="https://github.com/user-attachments/assets/48e13359-cdd3-4f5a-a12f-96012563288d" />


## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection

<img width="454" height="60" alt="image" src="https://github.com/user-attachments/assets/ba660a35-58d6-40ed-bd92-5cb5d710197b" />


## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt

<img width="479" height="89" alt="image" src="https://github.com/user-attachments/assets/69217998-8a7f-4a4b-8856-9b62f991e15b" />


## COMMAND AND OUTPUT

Remove the file hello1.txt
<img width="412" height="78" alt="image" src="https://github.com/user-attachments/assets/4eda44f6-3924-4e1d-9a2f-10228fababda" />

## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

List out all the associated file extensions 


<img width="408" height="153" alt="image" src="https://github.com/user-attachments/assets/3b1ea661-8010-492f-b5fa-0bd4c3a96329" />


## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

<img width="408" height="157" alt="image" src="https://github.com/user-attachments/assets/87f166e6-22b8-4e0b-b50d-81c7ca3ff028" />

<img width="678" height="970" alt="Screenshot 2026-06-04 051738" src="https://github.com/user-attachments/assets/bb2e7c4f-0fc1-4089-9f7b-4fbb2d9aaacd" />

<img width="632" height="973" alt="Screenshot 2026-06-04 051801" src="https://github.com/user-attachments/assets/c304ab47-947d-4dac-9957-8fb1c3725cf7" />

<img width="660" height="968" alt="Screenshot 2026-06-04 051825" src="https://github.com/user-attachments/assets/618bfbcf-d57c-4275-b7d3-f4718ea2e1db" />

<img width="595" height="953" alt="Screenshot 2026-06-04 051844" src="https://github.com/user-attachments/assets/9f4addf1-9441-423f-b963-f743b95c8d32" />

<img width="517" height="940" alt="Screenshot 2026-06-04 051905" src="https://github.com/user-attachments/assets/93f2495f-d5b3-4606-9e8c-25b512ab6b4e" />

<img width="635" height="944" alt="Screenshot 2026-06-04 051927" src="https://github.com/user-attachments/assets/cd3f4d13-8324-4ec3-8554-f3f9a1b62aa2" />

<img width="600" height="953" alt="Screenshot 2026-06-04 051950" src="https://github.com/user-attachments/assets/dc8ade63-f4db-412a-93fd-003809bdc18f" />

<img width="568" height="858" alt="Screenshot 2026-06-04 052009" src="https://github.com/user-attachments/assets/d41809ef-99dd-4452-9774-c1906c3177d0" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".


```
@echo off
set name=John
echo Hello, %name%
pause
```


## OUTPUT

<img width="446" height="130" alt="image" src="https://github.com/user-attachments/assets/9fc13543-719b-4de9-8453-0615547f8e6e" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

##BATCH PROGRAM

```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```

## OUTPUT

<img width="459" height="161" alt="image" src="https://github.com/user-attachments/assets/f48ac38d-7541-48e0-9da9-9823d49d15b0" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

<img width="484" height="168" alt="image" src="https://github.com/user-attachments/assets/db8cf840-4fd9-4698-924d-2c50747e81da" />



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

<img width="448" height="70" alt="image" src="https://github.com/user-attachments/assets/606be5b2-8edf-4047-9f15-26ffbc7c48c9" />

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

##BATCH PROGRAM

```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

## OUTPUT
<img width="456" height="169" alt="image" src="https://github.com/user-attachments/assets/aa026362-a141-4abc-a9a7-75ca2134f860" />

<img width="356" height="115" alt="image" src="https://github.com/user-attachments/assets/ad3db761-e7e8-404a-a2fe-7daf65aa76bf" />

<img width="360" height="130" alt="image" src="https://github.com/user-attachments/assets/f0243218-2dfd-4cc8-87c3-13b9893c9357" />


# RESULT:
The commands/batch files are executed successfully.

