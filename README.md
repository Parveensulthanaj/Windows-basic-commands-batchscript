# Windows-basic-commands-batchscript
## Ex08-Windows-basic-commands-batchscript

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
![alt text](img9/1.png)

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233546](https://github.com/user-attachments/assets/4cf95b06-d2ea-430d-97d7-7a4029b37e78)

Remove the directory "my-folder"

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233607](https://github.com/user-attachments/assets/a84ae75d-2a75-4994-b015-e917614d5494)


Create the file Rose.txt

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233655](https://github.com/user-attachments/assets/414b1d50-02b5-44af-bf21-44a280e726c5)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233730](https://github.com/user-attachments/assets/b4d4b71f-4f7f-4524-bdb1-75dc4e7cccf5)

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233818](https://github.com/user-attachments/assets/92e9dde2-6ca0-4f90-b245-32d644d7cd41)

Remove the file hello1.txt

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 233953](https://github.com/user-attachments/assets/03deabd9-0b1f-4b62-a0e7-9b9b6bca4443)

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 234053](https://github.com/user-attachments/assets/14e75375-81a3-4abe-aabf-55fef22f95d8)

List out all the associated file extensions 

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 234158](https://github.com/user-attachments/assets/e9178588-0f7d-427b-a413-01faaf13a41a)
![Screenshot 2025-05-19 234216](https://github.com/user-attachments/assets/61696791-d552-42b4-ac4b-8e9c65720a70)
![Screenshot 2025-05-19 234227](https://github.com/user-attachments/assets/38051720-0261-458a-9d98-d52a422c333f)
![Screenshot 2025-05-19 234239](https://github.com/user-attachments/assets/7cfe05d9-e665-4dc1-b3a2-918c72fea4d8)
![Screenshot 2025-05-19 234258](https://github.com/user-attachments/assets/1eec38e8-bab4-4190-8916-798036ae391f)
![Screenshot 2025-05-19 234310](https://github.com/user-attachments/assets/7871388f-5c50-4006-b845-e02b0539d8f1)
![Screenshot 2025-05-19 234321](https://github.com/user-attachments/assets/95a26b83-5058-4024-acb4-920ea7fc2be5)
![Screenshot 2025-05-19 234334](https://github.com/user-attachments/assets/61c76f7b-a27d-4a20-83e9-a8b592f476b5)
![Screenshot 2025-05-19 234344](https://github.com/user-attachments/assets/34f493d8-8403-44ea-b7c1-4ba0659418e4)
![Screenshot 2025-05-19 234356](https://github.com/user-attachments/assets/90bcaad6-02b4-4561-aee4-5c8927283f1c)


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
![Screenshot 2025-05-19 234435](https://github.com/user-attachments/assets/6230f7bb-96e9-4bcc-885f-3334cc9b050a)

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

@echo off set name=John echo Hello, %name% pause



## OUTPUT
![Screenshot 2025-06-02 235916](https://github.com/user-attachments/assets/e929f733-7e03-4c2d-8dce-dfc0c4412a0c)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

@echo off :main set /p number=Enter a number: rem Calculate remainder when divided by 2 set /a remainder=%number% %% 2 if %remainder%==1 ( echo %number% is an odd number. ) else ( echo %number% is not an odd number. ) :choice set /p continue=Do you want to check another number? (Y/N): if /i "%continue%"=="Y" goto main if /i "%continue%"=="N" goto end echo Invalid choice, please enter Y or N. goto choice :end echo Thank you for using the odd number checker! pause

## OUTPUT

![Screenshot 2025-06-03 000020](https://github.com/user-attachments/assets/d6024c4f-9dd8-4454-9963-3ee2eb2a60af)



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
@echo off for %%i in (1 2 3 4 5) do ( echo Number: %%i ) pause



## OUTPUT
![Screenshot 2025-06-03 000054](https://github.com/user-attachments/assets/9aec37f0-d13a-4668-86f5-eb1c13511985)




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

@echo off if exist sample.txt ( echo sample.txt exists. ) else ( echo sample.txt does not exist. ) pause

## OUTPUT

![Screenshot 2025-06-03 000252](https://github.com/user-attachments/assets/50650acb-903c-4415-b732-d445c81f11c8)

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

@echo off :menu echo 1. Say Hello echo 2. Create a File echo 3. Exit set /p choice=Choose an option: if "%choice%"=="1" goto hello if "%choice%"=="2" goto createfile if "%choice%"=="3" goto end

:hello echo Hello, World! goto menu

:createfile echo Creating a file... echo This is a new file > newfile.txt goto menu :end echo Goodbye! pause


## OUTPUT

![Screenshot 2025-06-03 000348](https://github.com/user-attachments/assets/ec45fd8c-9c4a-4786-95f1-5e6f210f71f0)


# RESULT:
The commands/batch files are executed successfully.










