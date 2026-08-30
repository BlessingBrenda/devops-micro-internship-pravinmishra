# Assignment 5 — Bash Script Automation Drill (OPS Checklist)

Part of the DevOps Micro Internship (DMI) Cohort 3 with Agentic AI

---

## Purpose

In this assignment, you will practice Bash scripting by building a series of small automation scripts covering environment setup, variables, arrays, loops, file conditionals, if-else logic, and functions. These scripts form the foundation of real-world Linux automation used in DevOps, cloud, and production support environments.

---

# Task 1 — Bash Environment & Workspace Setup

## Goal

Verify that Bash is available on your system and create a clean workspace for this assignment.

### Evidence

#### Screenshot 1 — Output of `echo $SHELL` and `bash --version`

![alt text](<screenshots/Screen 1.png>)

---

#### Screenshot 2 — Output of `pwd` and `ls -lah` showing the scripts directory

![alt text](<screenshots/Screen 2.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is Bash?**

Bash(Bourne Again Shell) is a command-line shell and scripting language used on Linux systems. It reads commands typed by a user or written in a script and tells the operating system what to do.

---

**2. What is the difference between shell and Bash?**

A shell is any program that lets you interact with the operating system through commands. Bash is one specific type of shell, others include sh, zsh, and fish. They all do similar jobs but differ in syntax and features.

---

**3. Why is it important to confirm the Bash version before writing scripts?**

Different Bash versions support different features and syntax. Checking the version first ensures the commands and scripts you write will actually work on that system.

---

# Task 2 — Your First Bash Script

## Goal

Create your first Bash script, make it executable, and run it from the terminal.

### Evidence

#### Screenshot 1 — Content of `first-script.sh`

![alt text](<screenshots/Screen 3.PNG>)

---

#### Screenshot 2 — Output of `./first-script.sh`

![alt text](<screenshots/Screen 4.PNG>)

---

#### Screenshot 3 — Output of `ls -l first-script.sh` showing executable permission

![alt text](<screenshots/Screen 5.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is the purpose of `#!/bin/bash`?**

#!/bin/bash is called the shebang line. It tells the operating system which interpreter to use to run the script, in this case, Bash. Without it, the system might not know how to correctly execute the commands inside the file.

---

**2. Why do we use `chmod +x` before running a script?**

A newly created script doesn't have execute permission by default. chmod +x adds that permission, allowing the file to be run directly with ./filename.sh. Without it, you'd get a "permission denied" error.

---

**3. What is the difference between running a script using `./script.sh` and `bash script.sh`?**

Running ./script.sh executes the file directly, which requires the script to have execute permission, and it uses whatever interpreter is specified in the shebang line (#!/bin/bash) at the top.
Running bash script.sh tells Bash to read and execute the file directly, regardless of whether it has execute permission. In this case, Bash is used even if the file's shebang line specifies a different interpreter.

---

# Task 3 — Variables: User Information Script

## Goal

Use variables to store and display user-related information.

### Evidence

#### Screenshot 1 — Content of `user-info.sh`

A variable in Bash is just a name you use to store a value, so you don't have to keep typing that value over and over. For example, when I ran echo $SHELL, that $SHELL was already a variable that held the path to my shell (/bin/bash). If I create my own variable, like name="Brenda", I can then use $name anywhere in my script, and it'll pull in that value automatically. If I ever need to change it, I just update it in one place instead of hunting through the whole script

---

#### Screenshot 2 — Output of `./user-info.sh`

In Bash, spaces actually change how a line is read. If I write name = "Brenda" with spaces, Bash doesn't understand it as "set a variable," it thinks name is a command I'm trying to run, and gets confused by the = and the value after it. That's why it has to be written tightly, like name="Brenda", no spaces, so Bash correctly reads it as an assignment

---

### Notes

Answer the following in your own words:

**1. What is a variable in Bash?**

A variable in Bash is just a name you use to store a value, so you don't have to keep typing that value over and over. For example, when I ran echo $SHELL, that $SHELL was already a variable that held the path to my shell (/bin/bash). If I create my own variable, like name="Brenda", I can then use $name anywhere in my script, and it'll pull in that value automatically. If I ever need to change it, I just update it in one place instead of hunting through the whole script
---

**2. Why should we avoid spaces around the `=` sign when creating variables?**

In Bash, spaces actually change how a line is read. If I write name = "Brenda" with spaces, Bash doesn't understand it as "set a variable," it thinks name is a command I'm trying to run, and gets confused by the = and the value after it. That's why it has to be written tightly, like name="Brenda", no spaces, so Bash correctly reads it as an assignment

---

**3. How do you access the value stored inside a Bash variable?**

To use the value stored in a variable, you put a $ sign in front of its name. So if I stored something in a variable called name, I'd access it by writing $name. That's exactly what happens in commands like echo $SHELL, the $ tells Bash "go get the value stored here" instead of just printing the word

---

# Task 4 — Arrays & Loops: Tools Checklist Script

## Goal

Use arrays and loops to print a checklist of tools used in Bash scripting.

### Evidence

#### Screenshot 1 — Content of `tools-checklist.sh`

![alt text](<screenshots/Screen 8.PNG>)

---

#### Screenshot 2 — Output of `./tools-checklist.sh`

![alt text](<screenshots/Screen 9.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is an array in Bash?**

An array stores multiple values under a single variable name. Example:

tools=("bash" "nano" "chmod" "echo" "ls" "pwd")
---

**2. Why are arrays useful in scripts?**

They let you group related values together instead of creating a aseperate variable for each one so you can loop through them, making the script shorter and easier to maintain/update

---

**3. What does `"${tools[@]}"` mean?**

It expands to all the values in the tools array. The double quotes matter because they preserve each element as a separate item — this is critical if any element contains spaces (without quotes, a multi-word item could get split incorrectly).

---

**4. What is the purpose of the `for` loop in this script?**

It iterates through the array one item at a time, assigning each value to a loop variable (e.g., tool) and running a command (like echo) on it each round — typically something like:


for tool in "${tools[@]}"; do
    echo "$tool"
done

---

# Task 5 — Loops: Number Counter Script

## Goal

Use loops to repeat a task multiple times.

### Evidence

#### Screenshot 1 — Content of `counter.sh`

![alt text](<screenshots/Screen 10.PNG>)

---

#### Screenshot 2 — Output of `./counter.sh`

![alt text](<screenshots/Screen 11.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is a loop?**

A loop is a programming construct that lets you repeat a block of code multiple times without having to write that same code out over and over manually.



---

**2. Why do we use loops in Bash scripting?**

We use loops in Bash to automate repetition, so we can perform the same action across many items or many times without writing duplicate code for each one.



---

**3. How many times did the loop run in your script?**

The loop run in my script ran 5 times?



---

**4. What would you change if you wanted the loop to run 10 times?**

To make the loop run 10 times, I'd extend the list of values after in to include ten numbers instead of five.



---

# Task 6 — Files & Conditionals: File Validation Script

## Goal

Use file checks and conditionals to verify whether files and directories exist.

### Evidence

#### Screenshot 1 — Output of `ls -lah ../test-folder`

![alt text](<screenshots/Screen 12.PNG>)

---

#### Screenshot 2 — Content of `file-check.sh`


---week-03-linux-and-bash-for-devops/screenshots/Screen 13.PNG

#### Screenshot 3 — Output of `./file-check.sh`

![alt text](<screenshots/Screen 14.PNG>)

---

### Notes

Answer the following in your own words:

**1. What does `-d` check in Bash?**

Bash?
-d is used to check if something is actually a folder/directory. When I run a script and use if [ -d path ], Bash looks at that path and asks "does this exist, and is it a directory?" If yes, it returns true and the script can move on to whatever I told it to do next, like creating files inside that folder.

---

**2. What does `-f` check in Bash?**

-f works kind of like -d, but instead of checking for a folder, it checks if the path points to an actual file (a regular file, not a directory or something else). So if [ -f path ] is basically Bash asking "is there a real file sitting at this location?" If the file is there, it's true and the script continues.

---

**3. Why should file and directory paths be stored in variables?**

Instead of typing out the same path over and over in different parts of the script, I store it once in a variable. That way if the folder name or location ever changes, I only have to edit it in one place instead of hunting through the whole script to fix every instance. It also makes the script cleaner and less prone to typos, since I'm reusing the same variable name each time rather than retyping the path.

---

**4. What happens if the file does not exist?**

If the script checks for the file using -f and it's not there, the condition just comes back false. So instead of running the "file found" commands, it drops into the else block and prints something like:
File does not exist: ./test-folder/student-info.txt


---

# Task 7 — Conditionals: Pass or Retry Script

## Goal

Use if-else conditionals to make decisions based on a variable value.

### Evidence

#### Screenshot 1 — Content of `score-check.sh` with `score=85`

![alt text](<screenshots/Screen 16.PNG>)

---

#### Screenshot 2 — Output showing `Result: Pass`

![alt text](<screenshots/Screen 17.PNG>)

---

#### Screenshot 3 — Content of `score-check.sh` with `score=55`

![alt text](<screenshots/Screen 18.PNG>)

---

#### Screenshot 4 — Output showing `Result: Retry`

![alt text](<screenshots/Screen 18.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is the purpose of if-else in Bash?**

Basically, if-else lets my script make a decision instead of just running the same commands no matter what. It checks a condition first — if that condition turns out true, it runs whatever's in the "if" part. If it's false, it skips that and runs whatever's in the "else" part instead. So depending on what's happening, the script can react differently instead of doing the exact same thing every time.

---

**2. What does `-ge` mean?**

-ge is short for "greater than or equal to." I used it to check if a score meets a certain cutoff — in this case, whether the score is 70 or higher:
[ "$score" -ge 70 ]
If the score is 70 or anything above that, this condition is true.

---

**3. Why should conditions be tested with different values?**

I tested it with more than one number because I wanted to make sure the script actually behaves correctly in every situation, not just the one I happened to try first. I used 85 to check that it correctly gives "Pass," and 55 to check that it correctly gives "Retry." I also tested 70 exactly, since that's the cutoff point — I wanted to confirm it counts as a Pass and not accidentally get treated as a Retry, since that's the kind of mistake that's easy to miss if you only test "normal" numbers.


---

**4. How can conditionals help in automation scripts?**

Conditionals basically let a script "think" before it acts. Instead of blindly running commands, it can check things first — like whether a service is actually running, whether a file is where it's supposed to be, or whether the disk is almost out of space — and then decide what to do based on what it finds. That's what makes automation actually useful instead of just running the same steps regardless of the situation.


---

# Task 8 — Functions: Final Bash Automation Script

## Goal

Create a final Bash script using functions to organize reusable code.

### Evidence

#### Screenshot 1 — Content of `final-automation.sh`

![alt text](<screenshots/Screen 19.PNG>)

---

#### Screenshot 2 — Output of `./final-automation.sh`

![alt text](<screenshots/Screen 20.PNG>)

---

#### Screenshot 3 — Output of `ls -lah` showing all created scripts

![alt text](<screenshots/Screen 21.PNG>)

---

### Notes

Answer the following in your own words:

**1. What is a function in Bash?**

A function is basically a chunk of commands that I group together and give a name to, so instead of writing the same lines over and over, I can just "call" the function whenever I need that task done. It's like creating my own mini command that runs everything inside it in one go.

---

**2. Why are functions useful in scripts?**

They keep my script from turning into one long messy block of code. By breaking things into functions, each part handles one job, which makes it way easier to read through and figure out what's going wrong if something breaks. And if I need to repeat a task, I don't have to copy-paste the same commands again — I just call the function.

---

**3. Which functions did you create in this script?**

I made four functions:
print_header – prints out the header for the assignment.
print_user_details – prints my full name along with the assignment name.
check_files – checks whether the folder and file I need actually exist.
print_tools – loops through the array and prints out each tool one at a time.

---

**4. How does this final script combine variables, arrays, loops, conditionals, files, and functions?**

Honestly this script pulls together everything I've learned so far. I used variables to hold things like my name, the assignment title, and the file paths I needed. I used an array to store all the tool names in one place instead of separate variables for each one. Then I used a loop to go through that array and print each tool out. I used conditionals (the -f and -d checks) to confirm whether the file and folder actually exist before doing anything with them. And I wrapped all of that logic into functions so the script stays organized instead of just being one giant list of commands from top to bottom.

---

# LinkedIn Post (Required)

## Evidence

#### LinkedIn Post URL

https://lnkd.in/p/en5xMm32

`Add your URL here`

---

#### Screenshot — Published LinkedIn post

![alt text](screenshots/Capturee.PNG)

---

# Submission Instructions

- Add all required screenshots in your submission
- Full name must be visible in required screenshots
- All script files must be created and run successfully
- Required notes must be answered clearly for every task
- Do not expose sensitive information (keys, passwords, credentials)

---

# Completion Checklist

- [ ] Task 1: Environment setup verified, workspace created (Screenshots 1–2, Notes answered)
- [ ] Task 2: First script created, executed, permissions verified (Screenshots 1–3, Notes answered)
- [ ] Task 3: Variables script created and run (Screenshots 1–2, Notes answered)
- [ ] Task 4: Arrays and loops script created and run (Screenshots 1–2, Notes answered)
- [ ] Task 5: Counter loop script created and run (Screenshots 1–2, Notes answered)
- [ ] Task 6: File validation script created and run (Screenshots 1–3, Notes answered)
- [ ] Task 7: Pass/Retry conditional script tested with both values (Screenshots 1–4, Notes answered)
- [ ] Task 8: Final automation script created and run (Screenshots 1–3, Notes answered)
- [ ] All scripts run without errors
- [ ] Full Name visible in all required screenshots
- [ ] LinkedIn post published and URL submitted
- [ ] No sensitive data exposed

---

## 📌 About DMI & CloudAdvisory

DevOps Micro Internship (DMI) is a project-based DevOps program run by Pravin Mishra (The CloudAdvisory) focused on real-world execution, systems thinking, and career readiness.

It helps learners build strong DevOps foundations with hands-on experience.

---

## 📌 Resources

- 🌐 DMI Official Website: https://dmi.pravinmishra.com?utm_source=github&utm_medium=readme  
- 🎓 University: https://university.pravinmishra.com?utm_source=github&utm_medium=readme  
- 💬 Discord Community: https://discord.pravinmishra.com?utm_source=github&utm_medium=readme  
- 📝 Blog: https://dmi.pravinmishra.com/blog?utm_source=github&utm_medium=readme  
- ▶️ YouTube Playlist: https://www.youtube.com/playlist?list=PLFeSNDtI4Cho  
- 🔗 Pravin Mishra (LinkedIn): https://www.linkedin.com/in/pravin-mishra-aws-trainer/  
- 🏢 CloudAdvisory (LinkedIn): https://www.linkedin.com/company/thecloudadvisory/

---

*This submission is part of DevOps Micro Internship (DMI) Cohort 3 — Agentic AI Track.*