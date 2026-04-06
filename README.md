# hjsakldfhl
Explaining **everything** in Kinger's terminal in The Amazing Digital Circus: Episode 8. Speculation is marked by [s] before a sentence.

```# System: KingSolution 2.0 / Digital Circus Mainframe```
* "2.0" implies this is Kinger's second version of the program to get into the Digital Circus's mainframe.
* A mainframe is a powerful (although not super) computer, often used as a server.[[1]](https://en.wikipedia.org/wiki/Mainframe_computer)

```# Date: 1996-10-30```
* Later entries show the Circus (or at least a lot of things related to it, like Bubble and the Wacky Watch) was created on October *15th*, 1996, 15 days before this program was created. Something must have happened that deleted KingSolution 1.0 after the Circus was created. 
* [s] Did Caine delete it to stop the researchers from messing with his code?

```# Host: circus digital```
* The ID or name of the server the program is connecting to. Not sure why it's in reverse order.

```"Initializing telnet connection..."```
* Telnet is a way to access the terminal of, and therefore run commands on, an external server, in this case the mainframe.[[2]](https://en.wikipedia.org/wiki/Telnet)
* [s] How is the mainframe still running over 20 years later if C&A is abandoned like we've been seeing? Or is the mainframe itself *within* the digital world? 

```Login: "kinger"```
* "Kinger" seems to be his C&A username, since he was able to log in to the mainframe with it.

```Pass: queenie123```
* "Queenie" is the circus name of Kinger's wife, but it's unclear how the name connects to her in the physical world.
* [s] Possible explanations include:
  * She was a C&A employee like him
  * "Queenie" was a nickname/pet name for her

```
kinger@circus:~$ whoami
kinger - administrator
```
* Not as deep as you might want to think: ```whoami``` in this case is just being used to check if Kinger has admin privileges, which he does.

```kinger@circus:~$ grep AI-Location```
* Since Kinger didn't specify what file to search, the ```grep``` command searches for the text "AI-Location" in every file on the mainframe.
* [s] Probably searching for a specific variable that he knew was in specifically the AI files he wanted to look at.

```
root 1337 /usr/ai/agent/caine
root 1338 /usr/ai/agent/experimental
root 1339 /usr/ai/module/consciousnessresearch
root 1340 /usr/ai/module/brainscans
```
* What he finds from the search are files named "caine" and "experimental" in the /usr/ai/agent directory and files named "consciousnessresearch" and "brainscans" in the /usr/ai/module directory.
* [s] The "experimental AI agent" may be the blue AI that Caine absorbed in the episode's intro animation.
* [s] It's also possible the experimental one was the original version of Caine, then when he absorbed the blue AI he renamed himself after the Biblical Cain because he "killed" his fellow AI.

```kinger@circus:~$ /secured/```
* Kinger checks what's in the "secured" folder, because Caine will likely only notice what Kinger's doing when Kinger messes with critical files.

```total 8492```
* There are 8492 files in the "secured" folder, so there's a lot to look through.

```
drwxr-xr-x 3 root wheel 512 Oct 15 1996 .
drwxr-xr-x 45 root wheel 1024 Oct 15 1996 ..
-rwxr-xr-x 1 root wheel 892344 Oct 15 1996 caine-core.lisp
-rwxr-xr-x 1 root wheel 234512 Oct 15 1996 paraphernalia-engine.dat
-rwxr-xr-x 1 root wheel 234512 Oct 15 1999 [Scratch].dat
-rwxr-xr-x 1 root wheel 234512 Oct 15 2008 [Ragatha].dat
...
...
-rwxr-xr-x 1 root wheel 45632 Oct 15 1996 wacky-watch.c
-rwxr-xr-x 1 root wheel 78234 Oct 15 1996 bubble-chef.lisp
```
* "drwxr-xr-x" and "-rwxr-xr-x" are shorthand for the permissions people have for the file. In all of these cases, Kinger has full read-write access, so they're unimportant here.
* The first number is the number of subdirectories or hard links to the file or directory. Unimportant for our purposes.
* "root wheel" seems to be a folder name of some sort and I don't really understand it, but it's basically saying everything here is in the same folder (which we knew already), so it's unimportant.
* The second number is the size of the file. The Paraphernalia Engine (whatever that is), Scratch's mind, and Ragatha's mind are the exact same size, which is *extremely* rare for non-identical files. What exactly this means, though, is unclear.
* The next entry is the date, which is the last time each file was modified.
  * Caine's "core" was last modified the same day as the other Circus-specific files like Bubble and the Wacky Watch, so this is likely the day he created the Circus.
  * [s] Since Ragatha's mind is still being used and Caine was still developing before the events of this episode (which take place in 2017), the two mind files here are likely just the base mind that was first uploaded to the Circus, and the "caine-core" is likely Caine's default/fallback programming.
    * If this is true, this confirms Scratch entered the Circus October 15, 1999, and Ragatha entered October 15, 2008 (the same day of the month Caine created the Circus).
      * [s] It's possible C&A have some sort of anniversary event where someone new tries out the Digital Circus on the anniversary of its creation.



# Credits
This project was inspired by [@summerwya's similar explanation](https://github.com/summerwya/hjsakldfhl), and I got a mostly-complete terminal transcript from there. 

I got a lot of info and theories from [@missyfrs's Tumblr post](https://www.tumblr.com/missyfrs/811651212864831488/) on the topic.

And of course credit to Gooseworx, GLITCH, and everyone involved with making Digital Circus, for making this theorycrafting possible in the first place.
