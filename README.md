
</center>

![Advanced Keylogger](https://i.ibb.co/qYr8r01/Advanced-Keylogger.png)

</center>

<center>

![Python](https://img.shields.io/badge/Python-Green?style=for-the-badge&logo=Python&logoColor=white&labelColor=black)

</center>

<center>

### Code for an advanced keylogger malware in python. 

</center>



# Features

***
- Logs **all** key presses
- Takes a **screen shot** of the current display
- Starts **recording** on victims microphone
- Copys **all** information in clipboard
- Copys all **system information**
- Sends an **email** of all information captured
- **Deletes files** with information to cover tracks
- Ability to **encrypt** the information
- Written all in **python**!

# Documentation
***

####  This is all the libraries needed for the code to run properly. We have imported emailing as well as pynput to listen for key presses. Furthermore we have imported scipy to record audio and crytography to encrpyt the data.

<center>
<img src="https://i.ibb.co/CVppN6Z/Code-Libraries.png" alt="drawing" width="500"/>
</center>


#### This is all the base information, such as the name of the save file and how much time to record on the microphone.


<center> 

<img src="https://i.ibb.co/b5j1rJs/Codevariable.png" alt="All the base information" width="500">


</center>


# Functions

***

#### This function manages sending emails out with the information gathered. It takes in the file name, attachment of what you are sending and the to address which you set. It then builds the email and tries logging into the email where it is sending it from. I would recommend using a dummy email or one you don't use. Finally after logging in, it sends the email to the to address then it quits.

<center> 

<img src="https://i.ibb.co/C6LDRYC/Email-Function.png" alt="Email-Function" border="0" width="500">

</center>

#### This function is responsible for gathering all the system information. I am using ipify to get the public IP, but I believe there is a limit so I added the try except in case ipify doesn't return an IP address. The infomation it gathers includes host PC name, both public and private IP address, proccessor type, Which OS is in use, and CPU. It saves all of this to a file.


<center> 

<img src="https://i.ibb.co/Srv6ZN3/System-Info.png" alt="System-Info function" border="0" width="500">

</center>

#### This function is responsible for copy the clipboard. I added the try except in the event that whatever it tries to copy is something that can't be pasted as a text(Slides, files, etc.), it doesn't end the program.

<center> 

<img src="https://i.ibb.co/BsbWMwB/Clipboard.png" alt="Clipboard function" border="0" width="500">

</center> 

#### This fucntion starts recording from their microphone, it does this for microphone_time, which can be changed in the base information. The default is 15 seconds, then it saves that audio to a .wav file.

<center> 

<img src="https://i.ibb.co/C6PhTcb/Microphone.png" alt="Microphone function" border="0" width="500">

</center> 

### Lastly, this function is responsible for taking screenshots. Its basic but gets the job done. It saves the image to a png.

<center> 

<img src="https://i.ibb.co/tCsX17W/Screenshot.png" alt="Screenshot function" border="0" width="500">

</center> 

# The brains

***

<center> 

<img src="https://i.ibb.co/Q6FwN1g/Main.png" alt="Main function" border="0" width="500">

</center> 

#### This big chunk of code is basically how the program works. While number_of_iterations_is less than number_of_iteration_ends(set in the base information section), it keeps logging all the keys pressed and writing them down. If the current time is greater than stoppingTime then it erases everything it logged from before. It also takes another screen shot, copies the clipboard and sends an email. It keeps proccessing until it reaches number_of_iterations_end.

# Encryption
***

<center>

<img src="https://i.ibb.co/Xpy5S7R/Encryption.png" alt="Encryption function" border="0" width="500">

</center>

#### I know its nothing crazy but its something. This is responsible for encrypting the files. I use fernet to encrypt the file, then it sends the encrypted file over by email. Personally, I am still learning about encryption and how to properlly use it. I do understand how it works and the different types but to use it in practical use I am still learning. This was fun to me as I love learning about encryption. It also waits 2 minutes before running the proccess all over again.

# Covering Tracks
***

<center>

<img src="https://i.ibb.co/x1rSX9M/Delete.png" alt="Function for deleting files." border="0" width="500">

</center>

#### Last but not least, this is responsible for deleting all the files we just made. This ensures that the victim isn't aware of what is going on and the program can keep running.

<center>

# Final Thoughts

***

#### This was a fun project for me take on. Thank you for taking your time to read all of this and I would love to hear feedback from you guys! I know I am just a beginner in this vast world of cybersecurity, but I love learning and being able to see things from a different perspective. Special thanks to Grant Collins on YouTube! If it wasn't for him I wouldn't of been able to learn all of this. All the credits to him and go show him some support, he is amazing! Thank you again and I hope you all have an amazing day or night where ever you are. Happy Coding :)!

</center>