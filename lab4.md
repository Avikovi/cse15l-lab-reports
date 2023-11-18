# Lab 4
## Starting from Step 4 - Log into ieng6
In the terminal type the command `ssh cs15lfa23nm@ieng6.ucsd.edu` and press <enter>. This will allow you to log in to the ieng6 server.
![Image](lab4-images/lab4-1.JPG)

## Step 5 - Clone your fork of the repository using the ssh url
Go to your forked reposity, click the green button that says "Code", make sure you are in the "ssh" tab and copy the link by clicking the button to the right of the link.
![Image](lab4-images/lab4.2.JPG)

After copying the link, you would go back to your terminal, typing `git clone`, and pasting the link using <control> and the "v" key at the same time, resulting in typing out the line `git clone git@github.com:Avikovi/lab7.git`, then press <enter>.
![Image](lab4-images/lab4.3.JPG)

Finally, cd into the new folder by typing `cd lab7` and press <enter>.
![Image](lab4-images/lab4.4.JPG)

## Step 6 - Run the tests, demonstrating that they fail
To run the tests we need two run two commands. The first command we run is to compile the java files in our folder which we can do by typing `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` into the terminal and pressing <enter>.
![Image](lab4-images/lab4.5.JPG)

The second command we need to run is to actually run the new complied files. We can do this buy typing `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` into the terminal and pressing <enter>.
![Image](lab4-images/lab4.6.JPG)

## Step 7 - Edit the code file to fix the failing test
