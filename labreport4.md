![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/df80e5ab-71cf-4cf5-b4e4-f1f1a89c48b6)

Step 1. Test if the tests pass: 'bash test.sh'

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/5d68d0b5-cc2d-494c-b324-a83488c0d221)

Step 2. Check what files exist so you can go into them in vim: 'ls'

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/0bdf792e-4103-4037-b99a-e81545a15e00)

Step 3. Open vim to fix the error: 'vim ListExamples.java' 

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/834a8c0b-e401-4eaf-9797-4593743d93d5)

Step 4. Press J 43 times to go down to the line with the error. (J = down in vim) <j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j><j>

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/f599f8ee-af57-4f55-b3d6-ed26a85be2a9)

Step 5. Press <l> twice (l = right arrow) <l> to move cursor above the desired word and press <I> to enter insert mode. Then <backspace><backspace> now press <2> to insert a 2 after removing
the number 1. Which would fix the issue.

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/55cfe5a0-660a-4f7c-97d6-c607a59988da)
![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/dfe94e97-5995-4d50-afdc-c5943262836f)

Step 6. Hit <esc> to get back to normal mode. Then hit : + w + q to exit after saving the changes.

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/d17110df-aa90-4294-a03b-3f38848819c0)

Step 7. Test the files once more to see if the issue has been resolved: 'bash test.sh'

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/288ed63f-35a4-4ed9-9d5d-3a3279e861f8)

Step 8. Now that the bug has been resolved. Add the changed files: 'git add'
Step 9. Make sure that the correct test files have been added: 'git status'

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/657cd004-66aa-41a2-854f-dca455bba1ac)

Step 10. Commit the changes: 'git commit -m "FileExamples.java bug has been fixed"'
Step 11. Push the changes to your repository: 'git push'
