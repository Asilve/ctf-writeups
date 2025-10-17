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

