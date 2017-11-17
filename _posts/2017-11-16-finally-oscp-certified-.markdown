---
layout: post
title:  Finally, OSCP Certified!
date:   2017-11-16 17:54:08 -0800
comments: true
published: true
categories: cybersecurity
---

Yes! I have finally received my OSCP certificate! 
It was a long and annoying journey, but I finally made it!

# Background
This is a sort of part 2 of [my previous post about my OSCP progress](/cybersecurity/2017/06/27/oscp-progress.html).

# Whole Story
I finally received the actual certificate in mail yesterday (Nov 15).

<p align="center">
<img alt="Certified" src="/assets/offsecoscp.jpg" width="80%" />
</p>

I initially registered for OSCP labs in June and it was just for one month. I literally aced through labs hoping to at least try to get low-privileged access on (in)famous "Sufference", "Pain", "Humble", and "Gh0st" machines. To my surprise and willingness to suffer (as OffSec puts it) I was actually able to root-and-shoot those boxes. Once I was able to pwn them, I actually became a little overconfident and started slowing down on the rest of the machines, plus I was extremely exhausted because of sleepless nights and highly loaded workdays. So in that mood I registered for exams when the labtime was over, and... bad idea. I slept through the half of the exam time, plus spent 9 hours of it at work, and was able to get low privileged shells only on 2 our of 5 machines. That overconfidence was humbled back down in 2 seconds. 

Things I learnt from this failure: **F'ing rest!** Rest, rest and rest! This is important. Next, confidence is actually good, it makes you get angry and push harder when you start failing. However, overconfidence makes you lazy. Lastly, don't go for the exam knowing that you lack the most important knowledge/experience (in my case it was privilege escalation). Oh.. totally forgot, make sure your internet connection is constant and good, mine kept disconnecting throughout the exam every 10-15 minutes. I didn't report it to the OffSec team cause I wasn't getting anywhere anyway.


Following days I rested the hell out of myself, did not even do any practice for the exam, layed back and just chilled. In fact, this is how I always used to prepare for exams - even in college. 
August and September was full of pentesting at work, tons of research, meetings with clients, conferences (hilariously, one of the big and world-famous companies that was holding a conference had a vulnerability in their registration page that allowed to get free tickets that would otherwise cost couple of grands) and... oh yes - I was able to find a vulnerability in one quite famous web application and disclosed it to the owner company, will post about it sometime soon as soon as the disclosure deadline expires. So overall, these two months were extremely productive in my professional life.

Things slowed down a bit by the end of September so I decided to re-take the exam. I registered for 15 days of lab, just to get myself in the OSCP mood, however I pwned 2 machines that I never looked at and it literally didn't help me in any way. I was frustrated, such a waste of money at that point, but I had to prepare for the exam somehow, because I still wasn't sure about my skills to do proper privilege escalation.

I started building my own lab - specifically for OSCP. Internet is full of Windows flavours that Microsoft doesn't support and doesn't care anymore, and it is also full of old and dirty software products that are full of vulnerabilities. So I set up my lab in NAT Network, and having installed tons of vulnerable services in the lab, I started ramming everything with metasploit and custom exploits developed either by editing or porting metasploit scripts to python. It was fun. It taught me quite a bit on how to escalate privileges in Windows environment. Then I decided to try out my learnt skills somewhere before taking the exam. That's when I found [HTB - hackthebox.eu](https://hackthebox.eu). I love it, their machines are up to date with exploits, realistic, and really fun. I still have to complete my journey there. I tried couple of their machines and was able to privesc easily on all of the ones I tried, so I decided I was ready for the exam.

# Exam Time
October 22nd. The exam day. 
- 15:00 (3:00 PM): I received an email from OffSec that the exam has started. I go to my laptop, open the lid... WTF!!! I DON'T HAVE INTERNET!!! WHAAAT?!?!?! IT'S NOT CONNECTING!!! SHIT!!! DON'T... panic... don't panic... just restart the router... (10 minutes later) why don't I have internet on my laptop?! It's working on my phone though?!... Maybe I should just restart my laptop... 
- 15:45 (3:45 PM): I finally have internet! Ok, let's sign in to the VPN now and start enumerating.
- 17:00 (5:00 PM): What the hell am I doing? I still don't have anything... Urgh... I should relax, calm down, and just switch to different box.
- 17:55 (5:55 PM): I get my first low privileged shell.
- 20:52 (8:52 PM): I get ROOT on 4th machine. At this point I knew that I passed the exam. I was happy, proud and shocked at the same time.
- After that I had a nice dinner, and played around with the 5th machine for sometime without full interest. Had a good sleep overnight. Started organizing my notes in the morning. Played around some more with the last box, and still couldn't get anything on it, so I just switched to writing the report. 
- Took all the left hours to write both of my lab and exam reports, sent the report at 4 AM in the morning of 24th October.
- October 25th, received confirmation via email that I passed the exam.
- November 15th, finally received the actual certificate in mail.


# Resources
These are the resources that really helped me to get through labs and the exam.

- [LinuxPrivChecker](http://www.securitysift.com/download/linuxprivchecker.py)
- [g0tmi1k's github](https://github.com/g0tmi1k/)
- [g0tmi1k's blog](http://blog.g0tmi1k.com)
- [FuzzySecurity's Windows Privilege Escalation](http://www.fuzzysecurity.com/tutorials/16.html)
- OSCP Forums
- [Vulnerable By Design machines](https://www.vulnhub.com)


