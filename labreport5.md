
![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/ff453d7a-e032-4c21-8dfa-a2d7129b3c3e)      ![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/31a0d4a3-866a-4059-aea9-8f396500ca06)

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/4c017009-abc2-435d-9b59-16f6dd130b00)

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/f498203c-4637-4648-9dcd-eb57d1ff75ec)

Hi everyone,

I'm having trouble running my Bash script that's supposed to compile and execute a Java program. When I run `test.sh`, I get the following errors:

![7e7f65f3228ef7ad5a5e4e6366ef5ea1](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/57f94118-b758-4520-bd6d-eef24c7a2ba5)

I provided the contents of each file in my directory. Does anyone see the issue thats flying over my head?

TA MR MARK:

Hi,

It looks like the issue might be related to the current working directory from which you are running the script. Your script is looking for `src/Main.java` relative to the current directory. 
Let's update your script to ensure it always references the correct paths. You can modify your `test.sh` script to use absolute paths and change to the correct directory before running the commands. Here's how you can do it:

Update `test.sh` to:
```bash
#!/bin/bash
# Change to the directory containing the script
cd "$(dirname "$0")"
# Compile the Java program
javac src/Main.java -d out
# Run the Java program
java -cp out Main
```

Me:

Hey sorry for sending another post but I tried updating the test.sh folder and I ran bash test.sh again and I got the same output.

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/9d0d2750-4aa6-4ceb-bff2-41818b139ccd)


TA MR MARK:

Hi,

Hey! Dont worry about it, this is what I get paid for.
Thanks for sharing the updated output. 
It looks like there might be an issue with the relative paths or the way the script is executed. 
Let's try a different approach to ensure the paths are correctly handled.

First, verify the directory structure is as follows:
my_project/
├── src/
│ └── Main.java
├── test.sh
└── data.txt


Ensure that `Main.java` is indeed inside the `src` directory. Then, another change you can make is to update your `test.sh` script to use absolute paths for both the source file and the output directory. 

Try to source and output the directories. You can search up what the new commands do to refresh your memory. They are important for your future cs classes.

Update `test.sh` to:

```bash
#!/bin/bash

# Change to the script's directory
cd "$(dirname "$0")"

# Set the source and output directories
SRC_DIR="$(pwd)/src"
OUT_DIR="$(pwd)/out"

# Compile the Java program using absolute paths
javac "$SRC_DIR/Main.java" -d "$OUT_DIR"

# Run the Java program
java -cp "$OUT_DIR" Main

```

Me: Oh SHOOT! I had the line-up wrong 

I fixed it now. After switching the directory from src back into myproject using cd .. I was able to run test.sh and it produced the output in the data.txt file.
![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/d349bbbd-97e3-4d20-9fdd-884b069c0a51)

Then I changed up my test.sh and ran it again with bash test.sh
![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/d3c966ef-00da-4f56-895b-2fdb93b22e6e)

THANKS FOR YOUR HELP !!

** Part 2 – Reflection **

During the second half of this quarter, I learned several new technical skills and concepts that I think are going to be pretty useful for my programming career. One of the most valuable things I learned was how to effectively use terminal commands and the Vim editor to manage and edit files. Conversations with Sammy, were particularly enlightening. Especially with the daily would you rather. Sammy helped me understand grep, awk, and sed for text processing, as well as solve some ieng6 issues I had.

Additionally, I gained proficiency in using Vim, which has drastically improved my speed and efficiency in editing code directly from the terminal. Overall, these experiences have been pretty fun and aided in my growth as a programmer and have equipped me with some not so useless skills that I will continue to use in my future projects.



