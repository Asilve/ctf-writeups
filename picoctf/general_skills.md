## Super SSH (Easy)
#### Description
Using SSH to find the flag. Provided information: a user name, a domain, a port number and a password.

#### Thought Process
Simply connect to the ctf-player@titan.picoctf.net server using SSH, on the provided port. If asked for a password, input the password provided.

#### Solution
"ssh ctf-player@titan.picoctf.net -p 62914"
then entered the password when prompted. Successfully logged into the remote server. After logging in, the flag immediately displayed in the teminal.

## Binary Search (Easy)
#### Description
Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag?

#### Thought Process
Guessing game will be presented, and based on the CTF title, I will have to use Binary search. As binary search is Logarithmic Complexity, the amount of possible numbers the correct answer can be will be halfed each time until the answer is found.

#### Solution
Connect to the provided server using SSH. Guessing game is initiated, 10 guesses, number between 1 and 1000, Higher or Lower based on the guess. Using Binary search algorithm, I found the correct number after 9 guesses. Flag was then provided after the guessing game was completed.

## FANTASY CTF (Easy)
#### Description
Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.

#### Thought Process / Solution.
Given a Netcat command to connect to upon starting the CTF. Connected to it and given a text based game. Each time the game prompted an option, I selected the most appropriate response given the context. At the end, The flag was presented.

## Log Hunt (Easy)
#### Description
Our server seems to be leaking pieces of a secret flag in its logs. The parts are scattered and sometimes repeated. Can you reconstruct the original flag?

#### Thought Process
I downloaded the file and tried to find a way to differentiate normal messages from the flag message, As stated in the hint, grep is a good candidate for this.

#### Solution
Outputted the whole file, seemed large, so definitely needed to use grep. All flags start with picoCTF so that was the natural first step. I found the start of the flag, but also it was cateogorised as "INFO FLAGPART:". So I did for "grep FLAGPART server.log", this returned all of the flag parts, which i them reassembled to find the final flag.

## Time Machine (Easy)
#### Description
What was I last working on? I remember writing a note to help me remember...

#### Thought Process
Given a git repo, i first checked the program that the creator of the CTF was working on. It lead to a guessing game (same one as Binary Search) so i played that again. After finding not much of note (except an error message that a file was missing) I checked the "Drop In" folder. A message stated that this is what he worked on today, and they would need to look at their commit history. Besides this message, a .git folder was present, I thought to check there next.

#### Solution
Looking at the git folder, I saw a number of files and folders, one being a "COMMIT_EDITMSG" file. I opened that and saw the flag.

## Commitment Issues (Easy)
#### Description
I accidentally wrote the flag down. Good thing I deleted it!

#### Thought Process
I was provided a git repo file. There was a text file inside that had the flag removed and "Top Secret" in its place. Naturally I knew I needed to find the information of the previous commit. After poking around, I found a file called HEAD that had two commits, the initial commit and the flag removal commit.

#### Solution
After researching how to revert back to a previous commit using the command line, I found a command i could use which was "git Checkout" along with the git commit code. This let me look at the previous commit, I use cat on the text file and the flag was there. 
Note, After looking at solutions after completing the room, I found a better way of doing it using "git log" and "git show".

## endianness (Easy)
#### Description
Know of little and big endian?

#### Thought Process
First time working with endianness. Found quite quickly that it involves converting to hexadecimal.

#### Solution
After connecting to the server using the netcat command provided, I was given a string (zapot) and asked for the little endian. I converted zapot to hexadecimal, and after confusing big and little endians for the first few attempts, I entered the little endian correctly. Following this I was prompted for the big endian, I entered it and it gave me the flag.

## Collaborative Development (Easy)
#### Description
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

#### Thought Process
Firstly, I checked the python file provided. No flag there. Then I thought about using git logs. Nothing there, then I looked at possible branches.

#### Solution
Using the git branch command, I saw main, and three other branches. I looked at the difference between main and each of the branches, which lead me to find all three parts of the flag, which I then reconstructed.

## Blame Game (Easy)
#### Description
Someone's commits seems to be preventing the program from working. Who is it?

#### Thought Process
There was a message.py file, which had print("Hello, World!" - Missing the last bracket. Needed to find a way to see who modified the file. Thought to do git log but too many commits to find the user who made the error.

#### Solution
After some research, gitk message.py was the command i needed. It opened up a window that showed me all the changes to the file and who committed them. The name of the person who committed message.py last was the flag.

## binhexa (Easy)
#### Description
How well can you perfom basic binary operations?

#### Thought Process / Solution
After connecting to the netcat instance provided, I was presented with a sequence of binary operations I needed to perform on 2 numbers. After completing these, I needed to convert the last binary number to hexadecimal. I was given the flag after inputting it correctly.

## repetitions (Easy)
#### Description
Can you make sense of this file?

#### Thought Process
Provided with a file. Decided to check the file type. After seeing it was an ASCII file, I checked the contents and saw it was encrypted, with base64 by my best guess (featured "==" at the end which is typical base64 encoding padding).

#### Solution
After decoding the file multiple times, I finally was provided with the flag I needed.

## Big Zip (Easy)
#### Description
Unzip this archive and find the flag.

#### Thought Process
After seeing a large quantity of text files and directories inside the main file, I knew I had to grep to find the "picoCTF" flag.

#### Solution
I used grep to search the immediate text files for "picoCTF", nothing came up, so i researched how to use grep to search inside directories too. This led me to "grep -r". After using this, I found the flag.

## First Find (Easy)
#### Description
Unzip this archive and find the file named 'uber-secret.txt'

#### Thought Process
As I had just done Big Zip, Grep -r was fresh so I used that to find the flag. However as the challenge was to find the file, I thought to start again. The natural command I needed was find.

#### Solution
Using find with -type file and -name uber-secret, I found the file path. After that I used cat on the file path, and the flag was output.

## runme.py (Easy)
#### Description
Run the runme.py script to get the flag.

#### Solution
I ran the provided python script which gave me the flag. Simple.

## PW Crack 1 (Easy)
#### Description
Can you crack the password to get the flag?

#### Thought Process
After downloading the script and password.txt encrypted file, I decided to run the python script. It prompted me to enter the correct password, So i dug into the python code to see if I could find any information there.

#### Solution
Within the python code was an if statement that ran if it matched the password to the string "1e1a". So I plugged that in to the script when asked for a password and it gave me the flag.

## PW Crack 2 (Easy)
#### Description
Can you crack the password to get the flag?

#### Thought Process
As with PW Crack 1, I decided to run the script provided. After doing so, again it asked for a password, so I once again decided to start digging into the python code for some answers.

#### Solution
As before, I found an if statement, this time however, the password was encoded in hexidecimal (0x64 for example, I knew the 0x prefix denoted hexidecimal). From there I just had to convert the hexidecimal to ascii and pop in the password into the script when i ran it. The flag was then given to me.

## convertme.py (Easy)
#### Description
Run the Python script and convert the given number from decimal to binary to get the flag.

#### Thought process
We have done 3 python scripts, why not try one more. Again download and run script. It gave me a decimal number and asked me to convert it to binary.

#### Solution
After getting the decimal number from the script, I converted it to binary. Upon inputting the binary conversion I was given the flag.

