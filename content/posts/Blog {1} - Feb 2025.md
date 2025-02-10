---
title: Blog {0} - Jan 2025
date: 2025-02-10
draft: false
tags:
  - Blog
---
## Conundrums

#### What day is it?
I had the (un)lucky task of covering out of hours on call over New Years, and so was woken up at 03:00 on New Years Eve to encounter an issue where errors were streaming in from our FTP platform - most notably the process which transfers orders from the website into our warehouse management system (WMS). After some quick investigation, I noticed that the affected jobs looked to only be those communicating with our Azure Blob storages. 
After I had confirmed no changes to the environment from our side, the manager on call alerted the internal team who support our WMS and the external 3rd party who support our website. I then started investigating the start time of the errors - exactly midnight! At this point, a Microsoft support engineer was called in to advise and confirmed the hypothesis - the leap year had led to some confusion in the FTP system, and it was unable to authenticate with the provided credentials.
Unfortunately, while the MS engineer was able to advise the suspected root cause (we were his 3rd customer just that morning), the advice was that the issue was with the FTP platform, not Azure.

The next step here was obvious. Get coffee. 

After grinding up some slow-roasted Italian beans and slowing pulling the flavour out from them (read: Nespresso machine), I raised a support ticket with the FTP support. While waiting for a response, I was then having to manually retrieve order information, and load the files into the WMS to ensure continuation of service (no orders were harmed in the making of this story). FTP support then responded to my distress call by confirming that there was an error, but the cause was from Azure and there was nothing more they could do. Queue the back and forth between two mighty service providers, while I sat in the middle drinking coffee and transferring XML files...

By this point, the sun had risen and it was time to go to the office. We'd agreed to a 9am catch up call to determine if anything else had changed (spoiler alert: it had not). Thankfully, the WMS support team were then able to put in a better workaround than me manually transferring the files, and I left my management to battle it out with FTP support management, who at this point would not confirm any issue on their end.

My New Year celebrations at midnight then consisted of me logging in to see if the issue had resolved itself (as was speculated) and thankfully all was good! I could see files happily making there way into Azure again and everything was right with the world. After an 18 hour work day (punctuated by a short nap), I logged off and went to sleep!

## Learning

I've started studying towards earning my SC-300 (Identity and Access Management) certification from Microsoft, and am also looking at getting some wider industry certs under my belt - any recommendations, please give me a shout in the comments!