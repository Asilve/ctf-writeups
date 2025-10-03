## Super SSH (Easy)
#### Description
Using SSH to find the flag. Provided information: a user name, a domain, a port number and a password.

#### Thought Process
Simply connect to the ctf-player@titan.picoctf.net server using SSH, on the provided port. If asked for a password, input the password provided.

#### Solution
"ssh ctf-player@titan.picoctf.net -p 62914"
then entered the password when prompted. Successfully logged into the remote server. After logging in, the flag immediately displayed in the teminal.
