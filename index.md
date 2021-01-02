# Development from scratch for MacOS

Disclaimer: By clicking this page and or reading anything in this page you agree that:
* These tutorial(s) are not for beginners in programming.
* Currently the tutorial(s) that are available maybe incomplete and the tutorial(s) may not produce the expected result when completed.
* I'm not responsible for any software/hardware damages from performing these tutorials.

---

### Tutorials
* Making a simple app on MacOS without using Xcode
* Using external C++ libraries for MacOS applications (gcc and g++ only)

---

<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>

## Tutorial 1: Making a simple app on MacOS without using Xcode

You will need:
* A Mac that is running MacOS (I mean, do I even have to put it here?)
* A Text Editor
* A basic understanding of MacOS
* A compiled and linked executable program that has the name like Main with no format ending so that it is executable

First, go to your desired folder to create your app like the Desktop folder. I will be using a folder that I created for this project called MyApp. Then inside that desired folder, you should create another folder and name it something like test.app for example and after that hit enter. At the end of all of this you should have something like this in your project folder:
![Picture showing test.app as a damaged or incomplete application in the MacOS Finder](/images/pic1.png)
Now that the app is in place, right-click the blank app that was created (look back at the picture for a reference) and choose "Show Package Contents". This should then open a blank folder space, right-click again and make a folder named Contents (Please do not name the folder anything else as this is a naming standard in MacOS). Now this Contents folder will hold everything in your app, but to make it work make two things, a file called Info.plist (FYI: The name for the file was not a typo, also make sure the folder is actually a plist and not a plist.rtf or something) and a blank folder called MacOS. These two pieces will be the key and beating heart of the app, without these two the app cannot be read by MacOS and cannot be launched by MacOS either, here is a picture of what your Contents folder should look like:
![Picture showing the contents in the Contents folder in the app](/images/pic2.png)
After those processes you have just completed the structure of the app, but we are not done with the app just yet. To make the app valid, we must modify our Info.plist file so that it aligns to Apple's app standards, normally Xcode will do it for us but it is possible to do this from scratch. I have made a template of the Info.plist file in my Github and you can copy it [here](https://github.com/PancakesWasTaken/Development-from-scratch-for-MacOS/blob/main/Info.plist), now the inside of the template I added all the required values for a plist file to work please don't delete them! Now that we have gotten our plist file partially complete we need to fill the values, while the values might look complicated but they are actually really simple to understand and fill out. Here is what all of the values in the plist file do in layman's term:

(To fill them out just put your entry in between the string tags)

* CFBundleName - Its the short name for your program. This doesn't really matter visually as I have seen so far.

* CFBundleIdentifer - Its the thing that identifies your app to MacOS. I found that to get it working, you just need to copy whatever you put in CFBundleName.

* CFBundleVersion - The version of your app that will be displayed to the user if they want to know. Put the version in the format x.x.x

* CFBundlePackageType - This is already prefilled with APPL and that tells the system its an app. Generally, you should just ignore it.

* CFBundleSignature - Now this is a special 4 character code that is specific for your app. I already prefilled it with ???? and from my tests, that should be enough for MacOS.

* CFBundleExecutable - Remember that requirement about a compiled and linked program? Well put it in the MacOS folder and put down its name in this value.

Now if you had not read everything above, you need to have your compiled and linked program in the MacOS folder so that it can be found by MacOS. Now we can start the grand finale of the tutorial and finish any last checks as well as touches. Make sure you recheck your executable's position as well as the contents inside your plist file so that it should look something like this on the inside:
![Picture showing what is supposed to be in the plist file](/images/pic3.png)

Now assuming that you got your executable in the appropriate place and your plist file in the appropriate configuration as well as your Contents folder in the appropriate order, you can now exit out of the Contents folder and even though it still looks the same on the outside you can now launch it at will like any normal app! This has been my first tutorial and if you have any problems feel free to drop an Issue at my Github page.

<p>&nbsp;</p>
<p>&nbsp;</p>

## Tutorial 2: Using external C++ libraries for MacOS applications (gcc and g++ only)

(THIS IS WIP. DUE FOR RELEASE: TBD)

You will need:
* Mastery of Tutorial 1
* Makefile knowledge
* Basic knowledge of a compiler and a linker
* MacOS knowledge

First, go to your project folder that contains your code and your Makefile. I will be using a folder called ProjectVulkan and in this case I will use Vulkan in conjunction with GLFW. Now make sure that your project folder space is neat and tidy currently as that will be needed later, trust me you don't want to learn the mistakes the hard way. After that make sure you have two folders called lib and include. This is what the folder should look somewhat like: ![Picture showing what the result should be](/images/pic4.png)
*Note for dummies: You may not see a code file in the folder and that is because this is a demo.*

Now each C++ library should have a folder that contains everything about it, make sure you open it and dump the contents of their respective lib and include folders into your project's lib and include folders, then go back and make sure you got everything in the transfer. After that, make a standard Makefile and put ```g++ [your options here] -I include -L lib -l [your library name here]``` as a make command for everything to actually work. Please copy the flags and arguments correctly as they are case sensitive, please note that you can use the -l flag as much as you like as long as it still makes sense to read the command. Here is my Makefile for example for you to refer off of: ![Picture showing the Makefile's content](/images/pic5.png)

After that save the Makefile, cd to your project directory and just type make to build the project. Then using your knowledge of Tutorial 1 use/replace the executable in your app. This has been my second tutorial, if you have any problems feels free to flag up an issue for me in the Github page, thanks for reading and hope you enjoy! *For more information, please see Addendum AD_2*

---

<p>&nbsp;</p>
<p>&nbsp;</p>


---

## Addendum(s)

* AD_2
  * When dumping contents of include there is most commonly a folder with the library's name in the said include folder, just transfer the whole folder. DO NOT ATTEMPT TO DUMP THE CONTENTS OF THE FOLDER INTO THE PROJECT'S INCLUDE FOLDER.

<p>&nbsp;</p>
<p>&nbsp;</p>


## Links for dummies

[Github for this page](https://github.com/PancakesWasTaken/Development-from-scratch-for-MacOS) - [Issues page](https://github.com/PancakesWasTaken/Development-from-scratch-for-MacOS/issues) - [Pull request page](https://github.com/PancakesWasTaken/Development-from-scratch-for-MacOS/pulls)
