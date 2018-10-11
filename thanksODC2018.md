# ODC Appreciation Day: Sentences that an Oracle techie should hear more often

It is the time for the [day](https://twitter.com/hashtag/ThanksODC?src=hash) of the year that reminds me I should finally start blogging regularly. Well I guess once a year is also regularly :innocent:. This time I wrote down some thoughts that often come to  my mind when I leave work and ride my bike back home.

## 1.	“Let’s prove it with a proper test case”
Here is a funny meeting disease. If up to 8 people in a meeting room discuss about what COULD get wrong, what SHOULD happen or what MIGHT be the proper way to go forward with a technical problem. Count me in! I love thinking through problems theoretically. But sometimes enough is said and You simply need to sit down and prove or test things with a proper test case.

Not sure if it is only my experience but common problems seem to be :
* TEST environments up are not up to date. They should at least resemble 90% like prod.
* Other people ignoring the approach because the test might not be realistic enough.
* People who think that it is not worth the effort.

It is hard to beat the last two arguments, but something is always better than nothing. Executing the test case or even setting it up teaches You things that You might not have expected! Ideally You learn new things or at least You simply have a more healthy blood pressure when switching things in PROD after the test case worked :stuck_out_tongue_winking_eye:.

My thoughts are also with the [ask tom team](https://twitter.com/connor_mc_d/status/1036875819379904512)...but that’s a different story :D.

## 2.	“That sounds like a horrible task. Have You ever thought about automating it?”
I think about that so often. E.g. I did my first intern at a company that did reporting in financial services. A lot of database guys had the requirement to spool .csv files and hand them over to the next department where they would prepare the proper KPIs.
The Oracle DB and all the SQL techniques like analytic functions is made to prepare data in a very efficient way. And no! - most likely the other persons job will not be taken away. IT guys still need the guidance in what the KPIs should actually report. That domain knowledge is still required.

In my current project, we have some smart users that finally started to produce monthly KPIs based on SQL queries. And no! That does not take my job away. They still need some guidance. Management already wanted to revoke the read privilege from them because even read access might bring a Database down. Oh yeah I am not arguing with that...but if they are smart enough to write SQL queries shouldn’t we build more trust? We should accept that even non-IT guys should have a chance to use IT for a better, more performant, time-saving everyday-work life. We can guide them by sharing our knowledge. There are also great resources for SQL beginners:
* Free tools like [livesql](https://livesql.oracle.com/apex/f?p=590:1000)
* Free training like [Oracles MOOCs](https://blogs.oracle.com/developers/learn-sql-with-this-free-online-12-week-course)
* Free quizzes like [the DEV GYM](https://devgym.oracle.com/pls/apex/f?p=10001:2001::::2001::)


## 3.	“I did not simply copy and paste from Stack overflow, I read the manual first.”

Maaaan, this is the part where I have to thank the great OTN community! All the blogs and tweets about issues You solved and provided Your code. I am a script kiddie! All those code snippets are so damn helpful. 
But still, it is sometimes better to take a few breaths before simply copy and pasting code into Your environment.

* Have a look at the following picture. You are not really into Linux? Let’s quickly open a random Linux host, run the commands and see what happens, right? Eeehm no!! #RTFM (or open the man pages) first, please :bowtie:.

![fun0](https://www.cyberciti.biz/media/new/cms/2017/05/russian-bash-code.jpg)

* Nothing is so permanent as a temporary government program. - Milton Friedman
Milton said that about political decision. But this is something that can be simply transferred into software development. Have You Ever created a table that You planned to drop later on “until the proper solution makes this workaround unnecessary”? It’s the same with a quick copy and paste of any code snippet. It works and the pain that users/managers put pressure on You, why things not have been fixed yet are gone. There is nothing wrong with it! But according to Marvin Minsky “You don't understand anything until you learn it more than one way.” So again: What is wrong with taking a few breaths in this fast and complex world trying to understand or learn something in depth?

So both - learning from all the great resources in the internet but at some point consider looking into the official manual - is veeery helpful :-). 
By the way: [Who else](https://twitter.com/FranckPachot/status/1049673933472055296) would like to get back the feedback option in the Oracle Docs? 

## 4.	“Developer had time to instrument the code properly from the very first run”
Here is a common problem
We had a .NET code hosted on a Windows Server. There is SQLPLUS installed and which handles the connection to the DB. The Windows Server is a VM hosted on an ESX machine. Suddenly, the .net Code hung up during the weekend recurrently.
It turned out to be a bandwidth problem. Windows thought there is 1GB but ESX/Switches only allowed a traffic max. capacity of 100 MB. At the weekend a full backup is taken, which takes away the full capacity.

The big deal: How did we find it? 
We had a quick look at the log files. And hell yeah this application generates a loooot of log files. Some might think that this is SPAM, but hey! The support by this company is great and they know how to read their log files! They quickly found: “Oracle ORA-03113: end-of-file on communication channel” and told us that this is an infrastructure problem. We addressed it internally and a proper tooling that supported the network guy in his analysis solved the issue within a suitable timeframe.

It would have been a completely different story if we hadn’t have any log files by the application. If it simply hangs up we probably would still RDP to the server and recycle/restart/reboot processes fighting the symptoms without really knowing about the root cause.

## 5.	“That is something where we are stuck in together. We should JOINTLY solve this issue.”
Cooperation not blaming! If You think about the example in point 4, here is how it could have worked: We could have blamed the software vendor for not re-opening the connection properly and that their software is shit. The DB Team could have blamed the Windows admins. Windows admins could have blamed the network guys,...and on and on and on. No! We did not. In this case we all sat together and each team tried to justify, why they think the issue is not related to their domain. In a lot of cases I see tickets that are pushed from one responsible group to another without really adding a REASON why they think it is not related to their domain. There is nothing wrong with stating that it is none of Your business 

![fun1](https://i.kym-cdn.com/photos/images/newsfeed/000/782/935/ce2.png)

..but why not adding a reason { maybe with a test case ;-) } tries to point up Your thoughts.

I am getting more and more frustrated seeing tickets were the list of assigned groups is flip-flopping back and forth. 

Which brings me to the conclusion: Talking to each other, sharing experience, trying to add prove to what You think.
I never saw sb. in the community biting a newbie for expressing/showing/asking something in the community. 

Happy to see Your tweets! Which sentence would You like to hear more often?


