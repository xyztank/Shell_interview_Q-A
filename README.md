# Shell interview Q&A

The purpose of this documentation is to document common interview questions and answers about Linux shell script.

## Q&A

* [Q1: What is Shell?](#Q1)
* [Q2: What is a Shell Script? Can you name some of its advantages?](#Q2)
* [Q3: What are the different types of variables used in Shell Script?](#Q3)
* [Q4: How do you create a shortcut in Linux?](#Q4)
* [Q5: What are the various stages of a Linux process it passes through?](#Q5)
* [Q6: How to pass an argument to a script?](#Q6)
* [Q7: How to calculate the number of passed arguments?](#Q7)
* [Q8: How to get script name inside a script?](#Q8)
* [Q9: How to check if the previous command was run successfully?](#Q9)
* [Q10: How to get the last line from a file using just the terminal?](#Q10)
* [Q11: When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?](#Q11)
* [Q12: How to get the first line from a file using just the terminal?](#Q12)

---

### Q1.
**What is Shell?**
### *Answer:* 
**The Shell is a Command Line Interpreter. It translates commands entered by the user and converts them into a language that is understood by the Kernel. The shell interprets a command typed in at the terminal, and calls the program that you want.**

---

### Q2.
**What is a Shell Script? Can you name some of its advantages?**
### *Answer:*
**A shell script is a command-containing text-file that contains commands in order of their execution. Typical operations performed by shell scripts include printing text, file manipulation, and program execution.**

   **Following are the two main advantages of shell scripting:**
+  **It facilitates developing your own custom OS with relevant features which best suit your needs.**
+  **It facilitates designing software applications according to their respective platforms.**

---

### Q3.
**What are the different types of variables used in Shell Script?**
### *Answer:*
**A shell script has two types of variables :**

  +  **System-defined variables are created/defined by the Operating System(Linux) itself. These variables are generally defined in Capital Letters and can be viewed by “set” command.**
  +  **User-defined variables are created or defined by system users and the values of variables can be viewed by using the command “echo”.**

---

### Q4.
**How do you create a shortcut in Linux?**
### *Answer:*
**This can be done with the help of links present in Linux OS.**

  +  **Hard Link: Hard links are linked to the inode of the file and have to be on the same file system as of the file. Deleting the original file does not affect the hard link.**
  +  **Soft Link: Soft links are linked to the file name and can reside on a different file system as well. Deleting the original file makes the soft link inactive.**

---

### Q5.
**What are the various stages of a Linux process it passes through?**
### *Answer:*
**A Linux process generally passes through four stages:**

  +  **Waiting: The Linux process waits for the resource.**
  +  **Running: The Linux process is currently being executed.**
  +  **Stopped: The Linux process is stopped after successful execution.**
  +  **Zombie: The process has stopped but is still active in the process table.**

---

### Q6.
**How to pass an argument to a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo ${1}

# bash test.sh p1
p1
```

### Q7.
**How to calculate the number of passed arguments?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo "Number of Parameters passed:$#"

# ./test.sh p1 p2 p3 p4
Number of Parameters passed:4
```
---

### Q8.
**How to get script name inside a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo "Script Name:$0"

# ./test.sh
Script Name:./test.sh
```
---

### Q9.
**How to get script name inside a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
var=$?
if var=0 ;then
    echo "Script was Run successfully!"
else
    echo "Script was Run failed!"
fi

# ./test.sh
Script was Run successfully!
```
---

### Q10.
**How to get the last line from a file using just the terminal?**
### *Answer:*
```Bash
# tail -1 /var/log/messages
Oct 18 03:42:46 ke-ol7vm1 nm-dispatcher: req:1 'dhcp4-change' [eth0]: start running ordered scripts...
```
---

### Q11.
**When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?**
### *Answer:*
```
read
```
---

### Q12.
**How to get the first line from a file using just the terminal?**
### *Answer:*
```Bash
# head -1 /var/log/boot.log-20190716
[  OK  ] Started Show Plymouth Boot Screen.
```
---
