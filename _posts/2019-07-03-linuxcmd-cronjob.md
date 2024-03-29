---
layout: post
title:	cronjob
category: 技术
tags: linuxcmd
description: linuxcmd 关于cron job 解读
---
 * * * * * CMD
The * means all the possible unit — i.e every minute of every hour through out the year. More than using this * directly, you will find it very useful in the following cases.

When you specify */5 in minute field means every 5 minutes.
When you specify 0-10/2 in minute field mean every 2 minutes in the first 10 minute.
Thus the above convention can be used for all the other 4 fields.
5.To schedule a job for more than one time (e.g. Twice a Day)

The following script take a incremental backup twice a day every day.

This example executes the specified incremental backup shell script (incremental-backup) at 11:00 and 16:00 on every day. The comma separated value in a field specifies that the command needs to be executed in all the mentioned time.

00 11, 16 * * * /home/maverick/bin/incremental-backup
00 – 0th Minute (Top of the hour)
11, 16 – 11 AM and 4 PM
* – Every day
* – Every month
* – Every day of the week

6.To schedule a job for certain range of time (e.g. Only on Weekdays)

If you wanted a job to be scheduled for every hour with in a specific range of time then use the following.

Cron Job everyday during working hours :
This example checks the status of the database everyday (including weekends) during the working hours 9 a.m – 6 p.m
00 09-18 * * * /home/maverick/bin/check-db-status
00 – 0th Minute (Top of the hour)
09-18 – 9 am, 10 am, 11 am, 12 am, 1 pm, 2 pm, 3 pm, 4 pm, 5 pm, 6 pm
* – Every day
* – Every month
* – Every day of the week

Cron Job every weekday during working hours :
This example checks the status of the database every weekday (i.e excluding Sat and Sun) during the working hours 9 a.m – 6 p.m.
00 09-18 * * 1-5 /home/maverick/bin/check-db-status
00 – 0th Minute (Top of the hour)
09-18 – 9 am, 10 am, 11 am, 12 am, 1 pm, 2 pm, 3 pm, 4 pm, 5 pm, 6 pm
* – Every day
* – Every month
1-5 -Mon, Tue, Wed, Thu and Fri (Every Weekday)

![cron1](https://raw.githubusercontent.com/Stenson00o/Stenson00o.github.io/master/assets/img/cron1.jpg)
![cron2](https://raw.githubusercontent.com/Stenson00o/Stenson00o.github.io/master/assets/img/cron2.jpg)
![cron3](https://raw.githubusercontent.com/Stenson00o/Stenson00o.github.io/master/assets/img/cron3.jpg)
![cron4](https://raw.githubusercontent.com/Stenson00o/Stenson00o.github.io/master/assets/img/cron4.jpg)
![cron5](https://raw.githubusercontent.com/Stenson00o/Stenson00o.github.io/master/assets/img/cron5.jpg)