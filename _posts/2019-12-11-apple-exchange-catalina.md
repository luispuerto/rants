---
layout: post
title: " Apple MS Exchange Mail on Catalina is going berserk with no connection"
date: 2019-12-11 08:52:40
featured: true
tags: [apple]
image: https://i.imgur.com/AxRGZHU.png
---

Hey  Apple!!! 

It's me —again & again— your loyal customer for more than 10 years.[^1] Again, and like the last time, I really didn't expect to be here —once more— complaining about you so soon. 

This time is a really stupid problem. I just update the other day to macOS Catalina 10.15.1 and today to 10.15.2 and I, and others, have noticed that the MS Exchange module on Mail in Catalina isn't working as it should. If you have Mail open and your connection drops the service `accountsd` just goes crazy and consume all the resources. The main reason is, if you have an MS Exchange account enabled on Mail it will try to connect to the account all the time, even if there is no connection and it probably enters in a crazy loop. 

It's only happening with Mail, and other services, like Calendar or Contacts, work pretty much fine AFAIK. 

I understand that there can be bugs, and for that reason the different releases in a OS are there to fix them. However, I really think that this is a major bug :bug: and I can't understand how it could have been overseen after 3 releases and 4 months since the first release. Yeah, three releases since 10.15.2 haven't fixed it yet. 

Why not more people isn't complaining about this? Well, we are living in an hyper connected world where hardly you disconnect your computer —or any other device— from the Internet, so it takes time to notice. Also, most people that uses a MS Exchange account on macOS uses it on Outlook, for several reasons. That means that really few people uses Mail to connect to their Exchange accounts. 

Some of us love the simplicity of Mail and we're really use to it. Right now I'm coping with the issue using exchange as IMAP, but this is a suboptimal solution and I really would like to continue using Mail with my MS Exchange account normally. 

Not to mention how dangerous the issue is. I noticed it because I was in the hospital —where these is not Internet so I needed to tether from my phone— and I left my computer with the lid closed and connected to power. When Power Nap fired up so Mail can check the mail, it found that the tethered connection wasn't there anymore —as it should— and enter in the vicious loop or trying to check the mail on the exchange account. I woke up to a warm Mac with its fans at full speed. 

Please Apple fix this issue!

Thanks! 

[^1]: Yeah... I know that for you a customer of just 10 years is nothing, since you have a 50 years history and some of your customers are as old as that. 