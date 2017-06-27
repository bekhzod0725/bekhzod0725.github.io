---
layout: post
title:  OSCP Progress
date:   2017-06-27 05:55:33 -0800
comments: true
published: true
categories: cybersecurity
---
I've been very busy and haven't been posting for a while. I wanted to share a lot with you guys, but literally had no time or was probably exhausted to even think about blogging. 
However, finally, I found some time to post about the stuff that I've been doing and will try my best to keep posting some interesting stuff. So for today, let's talk OSCP.

# Introduction
For those who don't know, [OSCP](https://www.offensive-security.com/information-security-certifications/oscp-offensive-security-certified-professional/) is a hands-on offensive information security certification. Moreover, it is a willingness to forgetting about sleep for a month, willingness to learn the hard way, cursing a lot, and becoming humble at the end. 

# My Progress
I started my OSCP labs 16 days ago. So far it has been quite an adventure.  I hate it and I love it. There are 44 machines in Public network, and I also got access to IT network where there are 6 more horny boxes that are just waiting to be pwned. I am working on exploiting machines whenever I have a chance, mostly during the evenings and over the night too on some weekends. I have rooted 23 machines so far out of the 50 that I have access for. These 23 machines also include Pain, Gh0st, Sufference, and Humble. The latter 2 are the ones that kept me up over night on those weekends. However the feeling when I rooted them was amazing! :D I must admit, that getting low privilege access on those two (Sufference and Humble) was even more satisfying than getting root. Sufference took me about 20 hours to get root and Humble took about 10 hours. The pain and ghost were fun but relatively easy, and each probably took me about 30 minutes to get root.

During these 16 days I wrote my own enumeration scripts that are lightning fast and are becoming part of a larger tool that I probably (unfortunately) won't be able to share, since too many parts of the code are also being implemented at my job, therefore can't publish it in accordance to the IP policy of the company.

During these 16 days I also wrote my first MSF module to a certain exploit that doesn't have any coded scripts that script kiddies could use, however when I asked Offensive Security team for a permission to publishing it, they kindly asked not to do so as they consider that part as trophy :D. I understand their position and respect their request. 

Besides writing custom toolsets, I also learned a lot on tons of things that I had never thought existed. The whole experience in OSCP within these 16 days opened my mind in so many areas, that it's taking me about 2 minutes to privesc linux based machines and a little more on windows machines - my weakest part.

I am planning on rooting at least 20 more boxes till the this weekend, because according to my calculations I am far behind the schedule as I only pwned 23 machines in 16 days whereas I should have had 32 (16days * 2 machines per day) in order to be able to pwn all machines within the allocated 30 days of lab time. I think sufference and humble kinda threw me off the schedule too. So now I am trying as hard as possible to catch up with my own schedule and complete all the machines before I hit the day 30. 

# Thoughts

I recommend for eveyone who's thinking about going into Cyber Security field or who is in the field but doesn't have the certificate yet to take it. You will love it and you will learn a lot. Even if you fail it, the learning experience you get from it is unforgettable. 









*This attack is in fact called "Smudge Attack"*

<div align="center">
<img src="http://www.securitylearn.net/images/smudge-attack.png" width="45%"  />
<br /><br />
<span style="font-style:italic">Source: http://www.securitylearn.net/</span>
</div>

# Your device is INSECURE!
It doesn't really matter what type of password security you use, be it swipe, number pad, character password... all can be identified within seconds. Of course, each type of password security is stronger than the previous type, but it increases the amount of time to guess your phone password by only few seconds. 

Having your "smudge"s stolen will decrease the amount of possible keys to crack your password. For example, if you were using a number pad based password and your pattern is {1, 3, 9, 0}, then you have only 4 x 3 x 2 x 1 = 24 different possible keys (on 4 digit key). However, your password is possibly one of the following four: "0913","0931","1309","3109" - because it is most probably your birthday, or it may be something else. Point is - you and I are humans, we have habits and they give us away. This makes any security system insecure.

Here is a bit lengthier research paper done on "Smudge Attack" by University of Pennsylvania: [Link](http://static.usenix.org/events/woot10/tech/full_papers/Aviv.pdf)

# "Oh, I use fingerprint"
Well, I am sorry, but you are even more screwed. Your fingerprint can be hacked with an inkjet printer. Here is a video showing how it's done: [Video](https://www.youtube.com/watch?v=fZJI_BrMZXU), research by Michigan State University.

# How secure are you?
Answer has always been the same. No matter what system or device you use, the security behind it is meant to protect you from other regular people who are not hackers. However, if you become a real target for somebody, it is not hard for them to hack you.

# Conclusion
In conclusion, you may be better off by cleaning your screen and wiping your fingerprints off if you really do want true security. These securities are meant for only consumer use. Meaning that they are generic and meant to have better user experience rather than security. So your security essentially is in your hands only and you are the only person who can protect you.
