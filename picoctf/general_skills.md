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
