---
layout: post
title:  AI to beat a game
date:   2016-10-07 22:48:15 -0400
comments: true
published: true
categories: artificial intelligence beating lumberjack game python 
---
Have you ever had a moment when you were unintentionally forced into a game competition and you just had to be at the top? Well, this post might help you out how to  get out of that situation and stay at the top.


## Lumberjack Game
In our family we use Telegram Messenger to text our relatives back in Uzbekistan. In the recent update of the App they introduced [games that you can play directly in your chatrooms](https://techcrunch.com/2016/10/03/telegram-levels-up-its-bot-platform-with-competitive-games-that-live-inside-chats/){:target="_blank"}. Fun part of these games is that you compete for highest score and the first place. 

So we're trying out all the games. We started with Math Battle and obviously I beat everyone in the group, but before doing so I guess I made my brother-in-law jealous for higher score and we started competing in all of the games. Long story short, he invited everyone to play this Lumberjack game and he was beating everyone. I was almost tying him by scoring just 10 or 20 points less. I had to beat him. So what does a Computer Science person do at these times? Of course! We write an AI to play it for us so that we don't have to waste our physical strength (especially when most of the comp. sci. people don't have it). 

### How to beat this game
The idea is simple. We check for a branch above the lumberjack's head, if it is there - then we switch to the other side, else keep cutting the tree. Branch is just an image mostly consisting of rgb(161, 116, 56).

The code is not generic, it is made to fit my browser's width. However, if you really want to take a look, please feel free to leave a comment and I will share it with more detail.

### Take a look at the result
<p align="center">
<a href="https://www.youtube.com/watch?v=okwUIrsJRn8" alt="Telegram Lumberjack AI" target="_blank">
<img alt="Telegram Lumberjack AI" src="/assets/lumberjack.png" />
</a>
</p>



**

#### Final notes?
I beat him by **207** points
