# Development from scratch for MacOS

Disclaimer: These tutorial(s) is not for beginners. Currently the tutorial(s) that are available maybe incomplete and the tutorial(s) may not produce the expected result when completed.

### Tutorials
* Making an app on MacOS without using Xcode

## Tutorial 1: Making a simple app on MacOS without using Xcode

You will need:
* A Mac that is running MacOS (I mean, do I even have to put it here?)
* A Text Editor
* A basic understanding of MacOS
* A compiled and linked executable program

First go to your desired folder to create your app like the Desktop folder. I will be using a folder that I created for this project called MyApp. Then inside that desired folder, you should create another folder and name it something like test.app for example and after that hit enter. At the end of all of this you should have something like this in your project folder:
![Picture showing test.app as a damaged or incomplete application in the MacOS Finder](/images/pic1.png)
Now that the app is in place, right-click the blank app that was created (look back at the picture for a reference) and choose "Show Package Contents". This should then open a blank folder space, right-click again and make a folder named Contents (Please do not name the folder anything else as this is a naming standard in MacOS). Now this Contents folder will hold everything in your app, but to make it work make two things, a file called Info.plist (FYI: The name for the file was not a typo, also make sure the folder is actually a plist and not a plist.rtf or something) and a blank folder called MacOS. These two pieces will be the key and beating heart of the app, without these two the app cannot be read by MacOS and cannot be launched by MacOS either, here is a picture of what your Contents folder should look like: 
![Picture showing the contents in the Contents folder in the app](/images/pic2.png)