The working directory for Image 1 was /Code Project/CSE 12/.vscode/CSE15 so it printed just that. This is usual as it should print the default path.
![Image](image1.png)

I then tried printing the working directory of the file CSE15 to see where it was it basically printed the same exact thing as from image 1 but the significance is that it is pointing to where the file path CSE15 comes from.
![Image](image2.png)

Lastly I tried printing the working directory of our new file lecture1 and sure enough it printed the same exact line as it did for pwd by itself. Well its obvious that it was because lecture 1 is located within CSE15 and CSE15 located in the others.
![Image](image3.png)

For image 4 we switched to CD to see what changing the directory really does. WIthout a argument cd erased the default directory we were working from in  images 1-3.
![Image](image4.png)

In image 5 we attatch lecture one after cd like this "cd lecture1" and if you notice from the output it says main and we switch from CSE15 in the end to lecture1 which will allow us to directly access and print the list located inside lecture1.
![Image](image5.png)

Image 6 I tried printing a directory from lecture1 which was an error not on the machines end but mine. I then asked a tutor and he said java detects it as an error because it doesnt make sense for it to switch to a text file as the directory.
![Image](image6.png)

For image 7 I decided to see what the list command does and sure enough it creates a list of the contents inside the file you are currently in. In other words the default path.
![Image](image7.png)

This time I also created an error because I tried to list the contents inside of lecture 1 even though I was already in the lecture1 directory from when I changed directory to lecture1 which is important to note it said there was no access to lecture1 which had no such file or directory. This might also be because of the / I used.
![Image](image8.png)

Lastly for image 9 I wanted to see what would print from a diretory so I said "ls Hello.java" and surely it ouputed Hello.java quite literally just listing out the directory I asked it to print. Since hello.java wasnt prompted with any of the text files it didnt print any of them but rather just printed Hello.java
![Image](Image9.png)
