## DISKO 1 (easy)
#### Description
Can you find the flag in this disk image?

#### Thought Process
First time using Disk Images/doing Forensic CTFs so needed to use the hint (which was "Maybe Strings could help? If only there was a way to do that?"). Figured I could use the Strings Command on the Disk image. The output was large, so required the Grep command

#### Solution
strings disko-1.dd | grep pico. This gave me a few strings, one of which was the flag. Later found strings disko-1.dd | grep picoCTF would have been better as only the flag was returned.

## information (easy)
#### Description
Files can always be changed in a secret way. Can you find the flag?

#### Thought Process
Again had to look at the hint for a clue. It stated "Look at the details of the file". I tried ls -lah, file, stat and lsattr on the cat.jpg file but nothing significant. Looked up other ways to view details and figured it was probably something to do with the metadata. 

#### Solution
Using a EXIF tool, I looked through the metadata. On the first pass over, nothing seemed out of the ordinary, but when I went back, I saw the license section had a random string of characters associated. I figured it was encoded somehow, so tried base64 decode, and it gave me the flag.
