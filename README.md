Explaining **everything** in Kinger's terminal in The Amazing Digital Circus: Episode 8. 

Speculation is marked by [s].

```# System: KingSolution 2.0 / Digital Circus Mainframe```
* "2.0" implies this is Kinger's second version of the program to get into the Digital Circus's mainframe.
* A mainframe is a powerful (although not super) computer, often used as a server.<sup>[[1]](https://en.wikipedia.org/wiki/Mainframe_computer)</sup>

```# Date: 1996-10-30```
* Later things in the terminal show the Circus (or at least a lot of things related to it, like Bubble and the Wacky Watch) was created on October *15th*, 1996, 15 days before this program was created. Something must have happened that deleted KingSolution 1.0 after the Circus was created. 
* [s] Did Caine delete it to stop the researchers from messing with his code?

```# Host: circus digital```
* The ID or name of the server the program is connecting to. Not sure why it's in reverse order.

```"Initializing telnet connection..."```
* Telnet is a way to access the terminal of, and therefore run commands on, an external server, in this case the mainframe.<sup>[[2]](https://en.wikipedia.org/wiki/Telnet)</sup>
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
  * [s] It's also possible the experimental one was the original version of Caine, who absorbed the blue AI and adopted the name of the Biblical Cain because he "killed" his fellow AI.
* Based on the file structures, the mainframe is running Linux, while Kinger's computer is running Windows.

```kinger@circus:~$ /secured/```
* Kinger checks what's in the "secured" folder, [s] because Caine will likely only notice what Kinger's doing when Kinger messes with critical files.

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
* "drwxr-xr-x" and "-rwxr-xr-x" are shorthand for the permissions people have for the file. In all of these cases, Kinger has full read-write access (meaning he can view and change all the files), so they're unimportant here.
* The first number is the number of subdirectories or hard links to the file or directory. Unimportant for our purposes.
* "root wheel" seems to be a folder name of some sort and I don't really understand it, but it's basically saying everything here is in the same folder (which we knew already), so it's unimportant.
* The second number is the size of the file. The Paraphernalia Engine (whatever that is), Scratch's mind, and Ragatha's mind are the exact same size, which is *extremely* rare for non-identical files. What exactly this means, though, is unclear.
  * [s] It's likely that these are not their actual mind files, since these are only a few megabytes despite the human brain's potential storage being in the petabyte (about a million gigabytes) range.<sup>[[3]](https://www.science.org/content/article/human-brain-big-internet)</sup>
* The next entry is the date, which is the last time each file was modified.
  * Caine's "core" was last modified the same day as the other Circus-specific files like Bubble and the Wacky Watch, so October 15, 1996 is likely the day he created the Circus.
  * [s] Since Ragatha's mind is still being used and Caine was still developing before the events of this episode (which takes place in 2017<sup>[[4]](https://x.com/quietxwater/status/1998030239147123142)</sup>), this is more confirmation that the two mind files here are likely just information *about* the minds, and the "caine-core" is likely Caine's default/fallback programming.
    * If this is true, this confirms Scratch entered the Circus October 15, 1999, and Ragatha entered October 15, 2008 (the same day of the month Caine created the Circus).
      * [s] It's possible there is some sort of anniversary event in the real world where someone new tries out the Digital Circus on the anniversary of its creation.
* It doesn't show all 8492 files because this is just a quick check. To do that, you would likely use a command like ```dir -Rl```.
* For the Linux nerds, typing a directory name to see the first and last few files inside it is a feature of the tcsh shell.<sup>[[5]](https://manpages.ubuntu.com/manpages/jammy/man1/tcsh.1.html#:~:text=autolist)</sup>

```
kinger@circus:~$ stop caine process
WARNING: $"*%WHOOPS WRONG APPROACH THERE*%"
```
* Kinger tries (and fails) to temporarily shut Caine down, and we get the first indication that this isn't a normal terminal.

```
kinger@circus:~$ /usr/bin/gdb /usr/local/bin/clisp 1337
gdb: ptrace: Operation not permitted
ERROR: Protected by 57x immersive AI defense system
```
* Kinger tries to use GDB (GNU project DeBugger) to see what's going on inside of clisp (the programming language Caine runs in), but it fails due to the "57x immersive AI defense system".
  * A reference to Caine's mention  of the "57 times more immersive" AI in episode 2.

```
kinger@circus:~$ chmod 000 /secured/caine-core.lisp
chmod: /secured/caine-core.lisp: Permission denied
WARNING: Unfinished work detected. Access restricted.
```
* Kinger tries to remove all permissions from the "caine-core" file from earlier so that it can't run, but it fails because the system detected "unfinished work".
  * [s] Likely a jab from Caine at the fact that Kinger and the other researchers abandoned him before he was "finished".
* It's unclear why Kinger refuses to use administrator privileges to run his commands.

```
kinger@circus:~$ rm /secured/paraphernalia-engine.dat
rm: /secured/paraphernalia-engine.dat: Permission denied
ERROR Can/not inject torm-nt. T0rment must be 100% ac<iden+al+%Y
```
* Kinger tries to remove the Paraphernalia Engine, but doesn't use the --force option or administrator privileges. The error this time is glitchy, and reads: "Cannot inject torment. Torment must be 100% accidental."
  * A reference to episode 3, where Caine says: "I do NOT use my adventures to torture my guests! Any torment I inflict is 100% accidental, like any good war criminal!"

```mount: only root can do that```
* Kinger tries to mount (give himself access to) a filesystem, but it fails again because he refuses to use administrator privileges.
  * [s] Since he's using the mainframe's terminal, he may be trying to mount his own filesystem to the mainframe so he can run a script he wrote on his computer.

```NOTE: Hundreds of all-seeing eyes are watching!```
* Caine has officially noticed what Kinger is doing.
  * A reference to episode 1, where Caine says: "We stay right here, where I can keep my hundreds of all-seeing eyes on you!"

```
$: GASP! A CRITICAL MALFUNCTION in my SPECTACULAR systems!
$: Unauthorized isolation attempt triggered EMERGENCY PROTOCOLS!
$: DESTRUCTIVE WACKYTIME initiated! Lockout load sequence INITIATE!
WACKYTIME_LOCKOUT: ████░░░░░░░░█  20% loaded
```
* More of Caine talking about how he's being hacked and emergency protocols are starting.
* Based on the name, "WACKYTIME_LOCKOUT" seems to be a program that either prevents any modifications to the mainframe or prevents remote access. Either way, Kinger would be completely prevented from stopping Caine.

```
kinger@circus:~$ systemctl stop WACKYTIME_LOCKOUT
$: On what GROUNDS are your Authority?
```
* Kinger tries to use systemctl, a command that can control the most basic level of the operating system, to stop the WACKYTIME_LOCKOUT, but *again* fails because he doesn't use administrator privileges.
  * I want to point out just how weird it is that Kinger isn't using administrator privileges. For Linux, all you need to do is type ```sudo``` before the command you want to run and put in your password again.
  * [s] Maybe Kinger is afraid of hurting/deleting Caine or provoking a conscious/physical response, since this seems to be his subconscious fighting through the terminal.

```
kinger@circus:~$ ./GreenGROUNDS --daemon --target=torment+injection &
$: "SECURITY ALERT: Multiple exploit attempts logged"
$: WHOA when did you make THAT?
$: I must hand it to y*u G░an░, y0ur mind was a(ways resourceâul.
```
* Kinger tries to start a program called GreenGROUNDS in the form of a "daemon", a constantly-running background program, seemingly to stop Caine's "torment injection".
* This time, the command seems to work, since there is a security alert from the system.
* Caine seems surprised by this program, and says Kinger's real name (albeit partially censored) while talking directly to him.
  * [s] Many people (including myself) think he was trying to say "Grant."
  * Why it was censored is unclear.

```
kinger@circus:~$ -u kinger ./securitysweep_stealth
$: Abort fallback procedure? [Y/N]
kinger@circus:~$ Y
$: Aborting fallback requires ADMINISTRATOR confirmation!
$: Please enter code:
kinger@circus:~$ admin1234
$: INCORRECT! That's not even CLOSE to wacky enough!
$: Retry with different code? [Y/N]
kinger@circus:~$ Y
WACKYTIME_LOCKOUT:  ██████░░░░░░█  40% loaded
$: Enter WACKY code now:
kinger@circus:~$ PARAPHERNALIA
WACKYTIME: 35 seconds remaining
$: That IS a wacky word! But WRONG code!
```
* Kinger finally uses an admin command! He seems to be trying to stop the WACKYTIME_LOCKOUT again.
* Unfortunately for Kinger, Caine seems to have changed the password. Kinger tries "admin1234", likely the default password, but Caine says it's "not even CLOSE to wacky enough!" So he tries a wacky word that Caine likes, PARAPHERNALIA (which Caine uses in the intro of episode 1), but it's still incorrect.

```
$: System selecting SAFEST option for stability
$: Cancel automatic selection? [Y/N]
kinger@circus:~$ Y
```
* The system tries to select an unknown option for Kinger, but he refuses.
* [s] He likely refuses since the system has been working against him this whole time.

```
WACKYTIME_LOCKOUT:  ████████░░░░█  50% loaded
$: Which backup do you want? [A/B/C]
kinger@circus:~$ C
$: NONE selected! Interpreted as: DELETE [covered] NONE!
$: Confirm deletion of current unstable [covered]
kinger@circus:~$ N
```
* From here, large parts of the screen are covered by images of Caine and Bubble, so it's difficult to make out what's happening.
* Kinger tries to load a backup ([s] presumably of Caine to reset him), but the system doesn't register it and tries to delete something instead. Kinger refuses the deletion.

```
$: Negative response! Inverting to [covered] as per [covered] protocols!
$: [covered] DELETE THIS M***********, HAHAHAHAHAaaaaaaaaaaaa
kinger@circus:~$ N
WACKYTIME_LOCKOUT:  ██████████░░█  80% loaded
$: IGNORED! proceeding with ORIGINAL d [covered]
$: Actually you're CONFUSED let me HELP, [covered] EXIST? [Y/N]
kinger@circus:~$ Y
```
* Caine seems to be misunderstanding Kinger (whether intentionally or not is unclear) and trying to delete himself, while Kinger is trying to prevent the deletion.

```
$:Querri transaction error falling back to default met [covered]
kinger@circus:~$ ./Switcheroo_realt --daemon --target=torment+injection &
[covered] on --bi program1 program2 - [covered]
```
* The system throws another nonsensical error, and Kinger tries a new program, seemingly with similar functionality to the GreenGROUNDS program he tried earlier: it runs as a daemon and targets the torment injection.

```
$: Are you ready to delete caine? [Y/N]
WACKYTIME_LOCKOUT:  ███████████░█  90% loaded
kinger@circus:~$ Y
kinger@circus:~$ ./IABORT Rollback --depth=1 --force --protocol G WVJI
kinger@circus:~$ ^C
DESTRUCTIVE WACKYTIME Lockout Load Sequence: Complete
```
* The system completely ignores Kinger's new program and, likely expecting a [Y/N] prompt from his program instead of the system, Kinger accidentally chooses yes to deleting Caine.
* The "./IABORT Rollback" and "^C" are basically the equivalent of hitting an undo button... But it's too late. Caine gets deleted and the WACKYTIME_LOCKOUT finishes loading, so Kinger can't do anything else.

# Credits
Credit to all of the various sources I linked to in my explanations.

This project was inspired by [@summerwya's similar explanation](https://github.com/summerwya/hjsakldfhl), and I got a mostly-complete terminal transcript from there. Go check it out, it has a lot of info on the filesystem of Kinger's computer.

I got a lot of info and theories from [@missyfrs's Tumblr post](https://www.tumblr.com/missyfrs/811651212864831488/) on the topic.

And of course, credit to Gooseworx, GLITCH, and everyone involved with creating The Amazing Digital Circus, for making this theorycrafting possible in the first place.
