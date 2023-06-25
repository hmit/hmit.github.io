---
layout: single
title: Unusual Saturday
---


A piece of advice:
1.)
if (programmer==false) {
read_like_english;
}
while(parsing) {
if (encounter_words_in_`’ && know_linux_osx==false) ignore;
}

2.) This is a rather long post and about the usual Saturday turning into an unusual one. If you dislike, keep it to yourself or drop an email at idont@effingcare.com and rest assured I would keep your suggestions a due consideration before I set out to write my next public post. (if you are close to me, you know who you are and also know that this is not meant for you ;))

3.) If at any point of time, you get bored reading this, just press Ctrl-W. Don’t come back to me later telling I didn’t warn you.

4.) There is one thing, I’m genuinely sorry about. And that is the poor formatting. Well, in my defense I wrote it on a text-editor and that too `gedit’ so pardon me for that.

Today was a particularly wasteful day for me. Well, I got up at ~2pm after an awesome treat night and uneventful drink night (My recommendation: Never buy Wodka Gorbatschow! It won’t get you high. Old monk or fuel is the way to go). So I woke up to find my computer dead. This was understandable as off late, my laptop seems to have a mind of its own with going down at his will, not running certain applications at will. Only the day before it started giving me segmentation faults for linuxdc++ and synaptic package manager. I tried starting it but the login window wouldn’t come up. I tried it twice, thrice and gave it one final go when I decided to put an end to all of it and give my laptop what it wanted for so many years (yeah I haven’t changed my OS for the past three years). In hindsight, I think all the problems (check the footnote if you are interested in my laptop problems)I had been facing since the past few months with my laptop were his way of telling me to let him retire. Well, I just want it to go for at least another 3 months and then iit can lay in peace and enjoy the company of my parents or my sister. So whatever be the intention I simply couldn’t give up. Hey! I don’t as of now have money enough to buy a new computer (besides it would be really difficult for me to part with this good old friend who has always been around during my entire IIT life. If you don’t believe it ask some of my friends (check another footnote for list of friends and how to get testimonials from them) and they would let you know).

So yeah, enough digression for the time being. So I found it in switched off and tried switching it on. This didn’t work! 😦 I decided to figure out what went wrong and may be correct it. This was dear to me as there were many packages installed and I simply couldn’t afford to loose them. Here I was in Saurabh’s room working my way up (and firefoxing 😉 attn:no chroming) to figure out what went wrong when I decided to take a backup of everything that’s on my comp. My good friend PJ had a hard-disk with just enough free space to store everything that was on `/’ folder. I started the transfer and left my computer. Just then Amogh walked in and started using my laptop (although this wasn’t how things actually happened but this will do. I have any way over-explained a lot of things and I wouldn’t want to belabor you with a lot of crap). He, the asshole and convenience freak he is, unplugged the hard-disk. I realised this as soon as I entered the room and got real angry with me. In my rash I started to move all the files in `/’ to PJ’s HDD. Also, at the same time I started deleting the old files from PJ’s HDD. A minute too late I realised my error that I had used `mv’ instead of `cp’ on both occassions and `rm’ for delete. I realised the grave error I had made and blamed Amogh for ruining the backup process (and also my wish to get my comp up and running using a few modifications instead of a fresh install). Thankfully, I had saved my `/etc/apt’ folder and `ls /var/lib/dpkg/info’ at some point of time and so I had the package-list installed on my comp. Upon some checking I realised that these files had magically evaded the `rm’ and were lying safely in the backup folder. So far so good! I had the package list that I were installed on my comp and would just have to configure the selections and `dpkg’ to set everything up.

I did a fresh Ubuntu 10.04 install (this is unusually fast; faster than Windows IMO). I did some playing around with `sed’, `awk’, `sort’, `uniq’ and `dpkg –set-selections’ to somehow use the file to get everything up (their are other technical details and additional info that I’m deliberately skipping). This ofcourse wasn’t going to work but was worth giving a try. At one point I even played with the idea of writing a `C/C++’ program to make the file look exactly like the one you get on `dpkg –get-selections’. I also had a chat with Prashant to use his _selections_ file (most other ubuntu/linux users had gone to Goa); this was also a dead end.
Desperately looking for a way I once again googled `dpkg –set-selections’ and the error I got when `dpkg’ wasn’t working (it was `unexpected end of line in package name…’ if you are that curious; hell you are not but I just wanted to write it :P). And voila! Jackpot! I hit upon a link (http://ubuntuforums.org/showthread.php?t=1636261 this is just for me; would help me to find it later) which described exactly what had to be done to get all the packages back and my laptop up and running to yesterday’s state sans the errors. So here I am writing the next public blog post sitting on pool-side, a mocktail beside me watching the installation happen. (Well, I am not actually near pool-side nor do I have a mocktail within the next 500m of me but it does evoke a good image)

Note, this isn’t the end but I’m very happy to make it this far without any big troubles. I now have to run some upgrades and configure my local packages to work properly but this should not be a major problem. I’m glad that I took Harsh’s advice in my sophomore year and installed my `Home’ and `/’ folder separately. 🙂

Ciao!

Footnotes:
1.)
a.) It has fallen (screen first in NSL once) and escaped with only a hard-disk crash.
b.) My home profile once simply stopped working.
c.) I’m struggling with low space every now and then.
d.) Heating problems every now and then.
e.) The ethernet port has almost stopped working (a little hyperbolic).
f.) Slow performance on netbeans and google-chrome.
g.) Hard-disks have increased these days.

2.) List of friends for testimonials on my laptop: Saurabh, Amogh, Pravjyot, Naman, Samyak

3.) Whenever I decide to do something productive on a particular day, my dear laptop is close by to ruin it. 😉

Update: It took me nearly a sleepless night to get my system up and running. Incidentally, I faced the exact problem after the installation as well. Turns out a local installation of zlib was the culprit. It was fortunate of me to install doxygen which needed a texlive package which had conflicts with the newer zlib. However, this zlib caused a segfault for libc (found upon a bt in gdb for synaptic and linuxdcpp and also no login screen showing up yesterday). Phew! All’s well that ends well.
You can find the exact description of the problem here: http://tech–help.blogspot.in/2011/02/ubuntu-solved-segfault-at-address-error.html