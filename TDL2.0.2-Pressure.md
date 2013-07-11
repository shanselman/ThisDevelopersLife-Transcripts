## Pressure

### Introduction

Rob: October tenth two-thousand and ten: the database that powers [stackoverflow.com](http://stackoverflow.com/), one of the top-200 destinations on the Internet ... melted.

Jeff: Every day the Chaos Monkey's gonna randomly pull the plug on one of our servers.

[musical interlude]

Geoff: Our database was - was missing - was just gone. [inaudible, laughter]

Sam: I'm deleting rows from one place, if I'm deleting from the wrong table, the whole site will be totally broken.

J: you don't have all three days to think about "Oh, what's the best way to do this?" You know? It just has to get done.

[musical interlude]

G: I fully expected to see something big, like, fire or something catastrophic.

[musical interlude]

G: Sam's thoughts are: "I can fix this, I can make it work".  My thoughts and some others in the group were just "Let's just get it working".

Sam: Haven't drunk for hours and - haven't done anything.  Haven't gone to the toilet.  Haven't done anything.  I'm sitting in front of a computer and my fingers are on the keyboard - the only thing that I'm thinking about is this ... and do I trust myself?

[musical interlude]

[2:06]  
Scott: Remember that scene in *Pulp Fiction* when they're about to put a syringe in Uma Thurman's breastplate?

#### Clip from *Pulp Fiction*:

> Woman: What's wrong with her?

> Man1: She's ODin'

> Judy: Get her the hell outta here!

> Man1/Man2: Get the \_\_\_\_ shot!

> Woman: \_\_\_\_ you.  \_\_\_\_ you too.

> Man1: She's gettin' the shot.  I'm gonna go get my little black medical book.

Scott: And they're gonna jab this thing into her heart with no medical training and you felt that sense of pressure.

> Man1: You've never given an adrenaline shot?

> Man2: I never had to it. I don't go joypoppin' with a bunch of bubble-gummers, my friends can handle their highs!

> Man1: Get the shot!

> Man2: I am, if you'll let me.
	
> Man1: I ain't somethin-\_\_\_\_ stoppin' you.

> Man2: Well stop talkin' to me, start talkin' to her.

> Man1: Get the shot!

> Man2: Right!

> Man1: You're - You - You're givin' her the shot.

> Man2: No, you're gonna give her the shot.

> Man1: I ain't givin' her the shot

> Man2: I ain't givin' her the shot

> Man1: I never done this before.

> Man2: Yeah, I ain't never done it before either.  Alright?  I ain't startin' now.  Look, you brought her here and that means you're gonna give her the shot.

> \*thump\*

> \*OD-woman gasps for air and starts screaming then coughing and gasping\*

> Woman: That was \_\_\_\_ trippy. 

> \*woman laughs\*

[musical interlude]

[03:13]  
R: You're a dev on one of the top sites on the Internet and it's just over-dosed.  The syringe is in your hand.  What are you gonna do now?  That's the theme of our show this week: "Pressure".  Pressure with a capital "P".  I talked to the Stack Overflow team - found out how they handled it ...  when their site went offline back in October last year.

[musical interlude]

Scott: This Developer's Life is brought to you by CodeRush for Visual Studio.  We appreciate their support with consume-first declaration, powerful templates, smart selection tools, intelligent code analysis, innovative navigation and an unrivaled collection of visual refactorings all working together.  Your development productivity will increase dramatically. Get CodeRush. You'll be glad you did.  Check them out at [devexpress.com/coderush](http://devexpress.com/coderush).


[musical interlude]


#### Act 1: Geoff Dalgas

[04:16]  
Rob: Every web developer wants to believe the site they're working on just might explode into popularity and become super-high capacity and relevant and important. Give us a chance to flex our engineering muscle as a software developer. "You see that amazing site over there? That one - yes, that does a million hits every hour. Yeah, that was me. I built that. I keep that thing running."

R: The truth of the matter is it really just doesn't happen that often.  But this last April, when I was in Las Vegas at Microsoft's MIX conference, I got to meet a group of developers who actually do have to do that every single day.

R: It was the Stack Overflow team and I got to talk with Sam Saffron and Geoff Dalgas.  I couldn't help myself, I said "What was the worst thing that ever happened to you?" 

R: Sam started to laugh and said, "Well that would be when stackoverflow.com exploded."

R: I looked at Geoff and I said, "Details please - tell me all about this. Well what was your reaction?  What went down?  What happened?"

Geoff: It's almost like your child is in jeopardy.  I guess that's the best way I can explain it.  Even I've just become a new parent.  I liken it to you just hear that scream that's off in the distance, you know?, like 'Oh no' - something really bad is happening.  I need to do something about this. And ... uh... that may be a little dramatic, but I uh - that's kinda how I feel about it working with the Stack Overflow group, the technology and the - the team - so, it's just something.  This is our baby.  I need to figure out what - what's happening.

G: I always sleep with my - my phone on and my laptop next to me and my wife hates this, but this is the way I live my life - lived my life back then when we didn't have a real system administrator whose job was basically to do - to be maintaining our servers.  It was my job and I don't classify myself as a system admin.

G: So the first thing you do when you get that call, is to run in to grab - I grabbed my laptop opened it up try and try and get to the site and Chrome's telling me that the system - site is down.  Wireless is working fine, everything in my house is working fine.  But, yet I can't get to any of the sites.  That point is a sense of panic, a sense of fear, a sense of uh... disbelief that. How - I mean what could have possibly gone wrong to get to the point where not just Stack Overflow, but all of our sites were just gone off the face of the Internet.

[6:54]  
R: It's three in the morning.  As a web developer having your site go offline - let's just say that's one of the worst things you could face.  Your phone pings - it's your notification service.  It pings again, and then again, and you get up and you realize this is serious stuff.  You've gotta do something, but what?  Your site, your servers, your database - everything's gone.

G: If we can't get to our site, there's nothing that we can do, other than hop in my car and drive down to the data center to find out what it is that - that happened.  Cause I'm expecting something big, like, if we can't get to anything our sites that's - it's a big deal.

[7:40]  
G: So yeah, I hopped in my car.  Just driving down the road.  Didn't even mention it to my wife; left her a little note - said, "I'll be back soon", case she happened to wake up.  Headed to the data center and it's only about a mile and a half down the road from where I live.

R: I can only imagine that drive.  Site's offline.  You don't know what's going on.  Can you imagine the thoughts going through your mind?  

G: They're not able to use this thing that you've built.  The thing you've considered to be your baby, your child.  The thing you've worked on.  I mean that's the pressure.  That's when the pressure comes in, so ... [deep breath]

G: So after I headed to the data center I noticed right away that the - there's a lot of commotion, there's a lot of people moving around that shouldn't be at that hour - normally aren't at that hour - especially being three in the morning.  I have a key, I can get myself in.  I hit the key and open the door and head to the co-lo.

R: At the time the Stack Overflow servers, which were carefully built custom by Jeff Atwood, were co-located at an ISP in Corvallis, just a mile away from Geoff Dalgas's house. So he got to babysit them.

G: Most of the people have seen me before and know who I am.  That's just living in small-town Corvallis.  You know - that's the advantage of that, [laughs] I guess.  I fully expected to see something big, like, fire or something catastrophic that had happened.  Obviously there's a lot of redundant systems that ISPs have.  It means something really really bad has happened.  So when I opened the door I did - I fully expected to see maybe fire, fire department, fire trucks in the driveway, something that - just that worst case, the one where ..., the one - the big one!

[musical interlude]

G: There's electricians, there's the people that I expected, I expected to see, but maybe not at three in the morning.  The normal guys running the data center there. They all were bustling around and not actually even really interested that I was there at the mom- when I first walked in.  And so, it took me a matter of - I just walked over to where our servers were and opened up the case to expect, to at least just look at my servers, just to see if they were working - if they were on.

[10:14]  
R: When things go wrong with some mechanical object we need to see it with our own eyes, see if we can fix it, or divine what happened to it. On the face of it, I mean Geoff going to his ISP to go stare at his server it almost seemed a bit ridiculous.  I mean what's he going to do just by looking at it?  Is he going to be able to crack the lid and manually start his database by flicking the hard drive with his thumb?  Very possibly - Geoff's a talented dude, but seriously what could he possibly do? Turns out he did the right thing:

G: And sure enough all of them were completely dark.

R: You mean the power was out?  Was it like someone kicked the plug out of the wall?

G: It was, it was a power outage.  And later found out it was a power outage as a result of some upgrades that were happening.

[11:08]  
R: Oops. Well it seems like a simple fix, but something tells me this isn't the end of the story.

G: After the power comes back, the first thing I do is check to see if the sites are gonna - are the database, the engine, the big power horse of our entire system.  Is that thing - is it going to come on?  Is it going to live?  I mean it's just a simple matter of opening up SQL Server Management Studio and watching the databases just come online first.  And I, in the past we've even primed the cache manually prior to turning our sites live.  Cause of the amount of data we'll have to "select" it - like do a "select star" on our largest table and get it all into memory first.  So I was expecting to do that, just open up SQL Server Management Studio and run a "select" on the posts table we have and get it all loaded. But looking at SQL Management Studio it was clear that our database was missing.  It was just gone. [laughs]

[12:23]  
R: So the actual boxes that fire stackoverflow.com, well they're up and running, the web server's running, app server's running, even the database server's running.  But when Geoff logs into it, goes to try and prime the database pumps so to speak, finds out that the actual file, the database file, containing all the data is corrupt.  SQL Server refuses to serve it, cause it thinks it's suspect. 

G: After I had found out the database wasn't alive, wasn't responding at all in SQL Server Management Studio, then I notified the team.  I had brought my laptop so I could at least get on the wireless and talk to everyone while I was there in the group chat.  So, I fired that up and just started having a conversation with Sam about: "What do we do - where do we go from here?  Database is off, is out.  Is there anything that I missed?  Is there anything, any magic that you have that I" - cause I was at that point thinking well the best thing we can do is just restore from backup, which was several hours old and that would look pretty bad. So, just trying to assess the situation.  I also fired off an e-mail to Brent Ozar, who happens to be an amazing DBA as well.  So, I was getting - I was starting to ring the bells at every - every bell that I could figure out.  Can this person - does it have any more knowledge?  After I had exhausted all the avenues that I expected just to doing simple - performing simple SQL "alters" to try and figure out if I could get the database back online - all by my-, you know, without any assistance.

[14:03]  
R: It was at this point the Stack Overflow team faces a very interesting set of decisions.  They can just restore the database and the service, it's a 5-hour-old backup and they're going to lose some data unfortunately.  To complicate matters their supreme leader, Jeff Atwood, isn't around.  He's at a conference, literally giving a talk at the time all of this is going down.  So he is completely offline and unavailable.  So the team has to make the call: Do we start the service?  Do we go with the 5-hour backup?  Do we lose 5 hours' worth of data?  Or, do we try and rescue this situation?  Can we rebuild this database?

G: I also was more interested in getting our service back up and running than recovering the database as it was.  I knew that it's very possible to restore from backup that there was no question of that.  That was all functioning and had been tested quite well actually several days before.  So, that was not a question for me.  I wanted the service up and there was some heated discussion around "Hey, let's just get this thing working, because the longer we're down the more people are gonna notice, the more people are gonna think that we basically don't have a clue or know what we're doing."  Sam's thoughts are: "I can fix this, I can make it work".  Whereas my thoughts and some others in the group were just "Let's just get it working."

I'm thinking in the back of my mind, "Well, what would Jeff Atwood do?  What would he say?  What would he-" [laughs].  That's all something that's re-occurring in my brain and I know that he would be like "Let's just get this thing back, let's just get it working - the faster, the better.  There's no excuse for being slow."

[15:53]
R: Your big website is offline.  Thousands of users are yelling at you on Twitter.  Jeff Atwood is your boss and you can't get ahold of him.  You need to make a decision.  Do you get this service back online?  Right now?  Or do you try and restore some lost data and avoid the backlash that is sure to come.  

G: At some point we were able to come to a consensus that it was easy enough - we kind of compromised, really.  It was easy enough to restore the database in parallel with what Sam was working on.  So, I began that process, just let's get a restore going.  Let's get the database back online and in the meantime Sam was able to work his magic on the - he was able to get the database to the point where we could get data out of it.  We actually thought we had it at one point in the middle of the restore and looked to be like it was functioning properly and in Management Studio.  So we thought we could bring the sites back online and at that point and tried, attempted once and ended up with just a massive amount of exceptions in our error log and they were not ones we'd ever seen before - we'd ever seen SQL produce.  Very low-level, very diffi- exceptions you just don't want to see. 

R: Well, the servers are back online.  Geoff's done his job.  Now we need to piece this data back together.  That's coming next, we talk to Sam Saffron.

[musical interlude] 

#### Act 2: Sam Saffron

[18:25]  
Rob: Well next up we talk to Sam Saffron, the data magician for Stack Overflow.  The easy part is seemingly done: turning the servers back on.  Now we gotta piece this database back together.  Fortunately, as Sam's about to find out, he's the only one that can pull this thing out.  Or, to put it another way, Sam's going to try and land this database in the Hudson. 

Sam: And then it's a real thing.  This can either work and if it works then all the people posted their questions and answers in the 5-hour gap are gonna be happy because that information's going to be there, they're not going to have to re-enter it.  Or it could fail and probably the site will go down for a while.  Some really messy things could happen if I made a big mistake, because I'm deleting rows from one place, if I'm deleting from the wrong table, the whole site will be totally broken.  If stuff is out-of-sync it's going to take us forever to repair it and the site will just kind of work, but not for those particular pages.

R: So the stakes just got raised a little bit here.  This isn't just about rescuing data, rescuing credibility.  This is about upping the ante.  If Sam fails, then the database could get corrupted further.  It could corrupt the only backup they have, waste time and not get back online.  Man, this is getting intense.

[20:00]  
S: I have five hours of data that I want to rescue and I have this confidence that I've done this before.  I trust myself.

R: Nerves and other things made of steel.

S: There is that moment when you're going, "Yeah, do I really trust myself?"  I've made off-by-one errors before, I've made mistakes in queries before and now I have this magical confidence that at three o'clock in the morning, when I'm totally tired, and had my head in the computer and haven't drunk for hours and - haven't done anything.  Haven't gone to the toilet.  Haven't done anything.  I'm sitting in front of a computer and my fingers are on the keyboard - the only thing that I'm thinking about is this ... and do I trust myself?

It's - there's that going on, and there's questions on "meta".  "What's going to happen with all of our questions?"

R: "meta" is meta.stackoverflow.com, a place where you can ask questions and get answers about Stack Overflow itself.  Questions like:

S: "Why?  What is going on here?  What happened?  When is this going to be fixed?  Is this all lost?"

R: Is it all lost, indeed?  So put yourself in Sam's position.  He's sitting there - he's trying to juggle all the team members who are now online, they're across the globe, they're now on Skype.  Skype's going "ba-doop", "ba-doop", "ba-doop" in your ears - everybody wants to know what's going on.  "meta" is going off, thousands of users upset.  Geoff is wondering, "Is this a good plan?  Do you really need to do this data ... now?  Can't we just get the servers back online?"  And all of a sudden the pressure is mounting.  Is this team going to stay together?

[musical interlude]

S: And there's this trust.  The team trusts that I'm going to do the right thing in that crisis situation.  There's this known thing in the team that you are your mistakes that you make and I make them regularly and I own them and I try and get the situation better.  But I'd say at that point in time it was like do whatever you have to do.  If you believe - if you really believe that this can work - we trust you.  We know that you're capable of this and I don't think anybody was thinking, "Oh, no, this is going to blow up, everything is going to be bad."  It already did, [laughs] I mean we were already recovering from a very bad situation.

[22:51]  
I guess there's also people didn't see the scripts that I was writing.  You know?  There was no peer review for a lot of this, it was kinda, "Sam, review it yourself.  Make sure that you don't make mistakes."  [laughing]  You couldn't read it.  It wouldn't make sense.  I mean, you're doing all sorts of pretty sophisticated tricks to get this data massaged in and yeah, you know, it's written for me it's not written for anybody else to read.  It's written so it's clear to me what I'm doing, but honestly if I looked back at that script today, I'm not sure if I'd understand in like half an hour - would take me awhile.

R: Sam's on his own.  Pressure is mounting literally by the minute.  He's gotta write this script that no one can review but him.  You know at some point you gotta think about this and think, "Man, this is just a job.  I'm doing this for a paycheck.  Is this really worth it?"

I asked Sam that, "Did you ever question what the hell you were doing?"

S: This is more than a job to me.  For me like, I see us as people who provide a framework for other people to interact, and the job is bigger than - and the actual thing, Stack Overflow, is bigger than the job.  The information we'll be there when the company isn't there, because it's all Creative Commons.

[crying in background]

R: So just to let you know that's Sam's daughter; woke up from a nap a little bit cranky.  Guest appearance on our podcast.

S: The programmers are the ones that provide all the value to others and my job is to make sure that the ship keeps on sailing and that is more - that's like a service to my fellow programmers.  So for me I don't think, "Ah yeah, in other jobs I wouldn't have this pressure.  Why worry about it?"  I think, you know, I'm enabling this interaction that wouldn't be enabled without me and I'm expected to do that as the person doing it.  The expectation is for the best people out there to be able to run this.  That's how people have trust in the system, trust that, you know, when they answer a question it's still going to be there in a month or a year or forever.  At no point in time am I thinking, "I wish I had another job or I wish I didn't have to do this at three o'clock in the morning."  The only thing I'm thinking is, "I wanna get this done.  I want this to work properly.  I wanna be proud of what I'm doing and I wanna solve this problem.  I don't wanna go home.  I don't want to go to another place, or be in another place, or be in another job that doesn't have that level of responsibility."  I love it - that drives me.

[25:54]  
R: Pressure.  Some people thrive off of it, some people don't.  Let's get back to our story...

Sam, you were trying to rebuild a database, how's that going?  Done yet?

S: There's this constant like, trickling of, "Is it done yet?  What are we gonna do?  Is it done yet?" and that's coming in on Skype constantly, like in the background, and just - I kinda shut it off.  So a lot of my work during that time is shutting off the rest of the world and just focusing on my task.  Yeah, at some points I felt like going on "meta" and saying, "Let's just shut down this 'meta' thing for a few hours.  I don't want to deal with it now.  We can shut this off and let us just do what we're doing."  But I guess that's not the attitude?  And internally, there were times like that - these decisions or questions, it's like, "Yeah, let's just give up on this data.  People can live without five hours of data, and the risk is really really high."  And people are saying that, you know, "Yeah - you're risking stuff here."

There is this drive that is beyond that; that I knew what the right thing to do was and I knew the risk and I knew that I could pull this one off and I knew that it would sit on me.

[27:06]  
R: Look out... here comes "Super Sam".  What about the rest of the team?   Don't you sorta have to convince them what you wanna do here?

S: There was no, "Let's have the committee.  Let's have on big committee and decide what we're going to do and have meetings and go to the whole way." A lot of crisis situations are run like that, but it takes, you know, 24 hours to even decide what you're going to do and whether it's worth it and run through a million steps. And it all ran very very smoothly.  Like everybody knew what their job was and what they could do in that situation and we were all like filling our own roles.  My role happened to be around recovering data at that point in time.

[28:11]  
R: All your SQL scripts are written; unfortunately not reviewed. You've looked over them any number of times, but eventually you're gonna have to press the button.  You're gonna have to run the query and either restore the database or blow it up completely.  

S: At the end, yeah, at the end it comes down to, like, "Do I press 'Enter' now or not?" And I did. And it worked out.

R: Steel 

[musical interlude]


#### Act 3: Jeff Atwood

[29:49]  
Rob: As a business owner or a development manager you're incredibly lucky if you have people as committed as Sam and Geoff here.  And Scott and I got to wondering, "Does Jeff Atwood, co-founder of Stack Overflow, does he understand just how good he's got it with employees like Geoff and Sam?"  Scott sat down and talked to him about that and some questions about how his team handled the October melt-down.

Scott: So Sam talked to us about this idea that he was in the situation room as if the - he had a "Star Trek" moment.  Like, Sam had this moment where he wrote up this script that was going to recover the database.  He had no peer review, but he also did not have a "James Kirk" to make that call for him.  To say, "Do it!", you know, "Put the torpedoes in backwards - I know all the paperwork says it won't work, but I'm sure it will work."  You know what I mean?  And they put the torpedoes in backwards and it saves everyone.  If you were there with him as he's got his finger on the 'Enter' key and he's like, "I think that this is gonna do it."  What would you have said?

Jeff: I certainly would have supported it.  I mean, I feel like everyone on the bridge, if you will (going with the "Star Fleet" metaphor), is extremely capable.  You know?  And they don't necessarily need me to tell them every little thing to do.  I think it helps sometime to have somebody focus, so that everybody's sorta driving the correct direction and aren't going all over the place, but sure - no, I totally support that.

[31:12]  
S: But what if he pushed the button and it deleted everything?

J: Well I think at the crisis-point that they were at it could only really get better.  It's like when you're fully down, it's like, short of destroying even more data, which I don't think was actually possible.  I think this was a recovery scenario, right?  So it's like this is a best-effort sorta thing from the get-go.

S: Okay.

J: So there's nowhere really to go but up in this case and get the data back.

S: Of course, I mean I appreciate where Jeff's coming from.  What's he gonna say?  "I didn't trust my team."?  "I don't trust Sam."?  But I really wanted to dig in this.  It's easy with hindsight - the benefit of hindsight to say, "Yeah, of course I would trust my guy."  But would you really trust your wife, your friend, your co-worker in that moment of pressure?

[32:07]  
That's really surprising.  It feels - it seems like I believe you, but at the same time I'm like, "Wow." You guys have that much trust for each other that you can do that?

J: Oh yeah.  Totally, totally.  I mean I think when you work with people that are - you know Sam's in Australia and I'm half a world away and here in California, you're dealing with people that are - I mean, they just get it done.  You know?  It doesn't - I don't need to be there - I like to be there, because I like to be part of the team.  It's more fun to work in the team, but part of the reason they were hired from the beginning was that they get shit down.  You know?  Like nobody has to tell them to do things.  In fact, one of the things I like to say, partially tongue-in-cheek, is that if I have to tell you what to do then you suck.

[33:07]  
J: You should be coming to me saying, "Jeff we really need to do 'x' and 'y' and there's all these things I really wanna do."  And I just basically sign off on it.  Make sure, again, we're going roughly in the correct direction for the vision we have for this thing.  But I just unleash them and then they get things done.

[33:25]  
S: There was something you said in your post about the Chaos Monkey, about "coming to blows" and what I wanna - I'm not trying to like incite trouble, but I would like to understand why you seem so calm and very kinda like controlled and thoughtful right now, but in your blog post it was like you said something like, "came to blows".  I'm trying to understand if that was just a phrase, or if there was actual kinda tension there.

J: I think the crisis-points I think are little easier, because everybody comes together, everybody focuses.  But it's sorta the Chinese water torture of like every day you have this thing failing.  That was a slightly different scenario that was just more like, every day the Chaos Monkey's gonna randomly pull the plug on one of our servers.  Somebody has to get out of bed, or whoever's around has to deal with it.  And it just grates on you, because it's like the psychic weight of every day, you don't know when, you don't know where but the boogey-man's gonna poke you, right?  Like, every day.  And after a couple of weeks of this you start to really get on edge.  Like, I remember Geoff Dalgas talking about this, he's like, "I dreaded going to bed." 

I think this one was a little easier, because it was a big crisis-point.  There was a clear thing that was wrong.  Whereas with the Chaos Monkey scenario we didn't know what was wrong.  We spent months trying to figure out what that was and doing all these crazy things.  When you get to the bottom of the barrel we're like "Okay, let's try this.  Let's try this.  That didn't work.  Okay, now try this."  Then you start getting to the crazy-shit it's like, "Should we even try, does this even make sense anymore?  Are we just like working on voodoo now, you know, is this like sacrificing chickens to the gods?  Do we even know what we're doing at all?"

[both laughing]

[35:05]  
That's when tempers start to flare, because your crazy idea may not be any better than my crazy idea, right?  Cause we exhausted all the normal human being ideas of like what this could be, and now we're like in outer space.  I think the cosmic rays are flipping the bits of the memory, you know, and that's why this is happening.

S: But isn't that the kind of crazy stuff that doesn't - you're describing Star Trek, right?  I mean, everything that we know is wrong.  Right?

J: Yes

S: So, you know, you stand here and I'll say this and we'll put the torpedoes in backwards and that will send us backwards in time to Thursday when before - it's just kind of Rube Goldbergian, physics do not apply, kinda world.

J: Yeah, totally.  I mean, I you know, think this is more of a disaster recovery scenario that we're describing which is also traumatic, don't get me wrong, but I think it's so much saner when you have clear thing that is wrong and a some kinda path to solution.  When you have something wrong, you don't know what it is so you don't know where it is, you don't know when it's gonna happen. A few months of that, and literally it was months - it was like at least two solid months of sorta every few days that kinda thing would happen.  It gets really old and that's when tempers start to flare and fortunately that is now behind us.

[36:27]  
S: Were there particular people that, and I'm not trying to call people out, but are there some people who just crack under the pressure?  And they're just like...

J: Well, if you go back to something I just said, I said, "If I have to tell you what to do, then you kinda suck." - I mean, again, tongue-in-cheek, I'm not fully saying that, but the side-effect is I have people working for me that are very very talented that know what they're doing that don't really need my input to proceed necessarily.  And sometimes they want to push ahead, they don't wanna really want to have someone else make the decision for them.

And part of what it comes down to is, "Okay, look, we have four things we could do, I can't tell you which one is correct.  I don't even know which one is correct myself, but I have to pick one, ok, because we have to have a direction" - we can't try four different things - we have to try one thing at a time in some kinda order that makes sense to someone and somebody just has to be the decision maker.  Someone has to call the shots in that case when there's not a clear path forward.  And not everybody, and even now a lot of the decisions we make, not everybody agrees with everything we do and I wouldn't want them to.  I don't want a team full of "yes men" that are telling me, "Oh yes, Jeff, you're brilliant.  This is exactly what we should be doing - of course we'll do exactly what you say."  I want them to push back and say, "You know what? I don't know if this even the right thing for us to do."  And that's cool, but when you reach the breaking-point of a lot of things going on that you don't understand and you tried all the normal human being things I think that's when that process starts to break down a little bit and everybody gets on edge.

[38:04]  
I mean if you look at the people who advocate these programming tests, part of the reason they give you these programming tests, they're meant to be a little bit stressful.  You go into some interview.  You have to write code you've never seen.  You have to do some thing you've never done before, like, with a time limit.  And I will say that there's some truth to this.  When people can't get things done in a reasonable time-frame - that *can* be a problem.  

In a point of crisis, like if you have a crisis like this you have a time window, like you have - you don't have all three days to think about "Oh, what's the best way to do this?" You know? It just has to get done. And be able to think on your feet, think quickly and make key decisions and say, "You know what?  Based on the information that I have this is the way I'm gonna go."  And feel confident about it is really essential.  I mean, that's what makes someone good.

[38:59]  
S: When you started Stack Overflow and you started - you talked to Joel, there was no doubt like pressure to get it started.  And then when it was gonna crash that day - when it crashed that day there was pressure and then there's like everyday pressure, or feature pressure, or self-imposed pressure.

Is it more stressful when there's that kind of intense acute pressure?  Like, the site's down or is more intense when there's the kinda larger background pressure that we need to get this system migration working in the next two months.  Less acute, but more kinda on-going and slow, like water torture pressure.  

J: I think for us it's a concept of almost like peer pressure of we're trying to do things - we're a site for - well Stack Exchange the network is bigger than programmers, but Stack Overflow is obviously all about programmers. It's like how would you feel about a programming site where, and this of course happens, which is embarrassing, but they e-mail you your password.  This is a site for programmers, where you say, "Hey, I need to do a password recovery." and they mail you your actual plaintext password.  Well immediately you're like, "Okay, how seriously can I really take this site if it's run by people who don't understand the very basics of not storing plaintext passwords?" The fact that you know my password indicates you don't know what you're doing.

So operationally, if we can't keep the site fast, reliable or just up at all, right?  That would mean we're kinda incompetent as programmers.  You know, as people who run a website.  You know, it's not rocket science to run a website.  There's a lot of things to get wrong, but fundamentally I would say the biggest pressure for me is peer pressure.  You want to be a good role-model for the community.  You want to be an example of the way to do things properly, like when you go to Stack Overflow and you look at a question, you expect an answer that's okay, this is reasonable good practice for programming.  So there's no reason you wouldn't have the same expectation of the website.  Right?  This is a reasonable way to run a top-200 or top-250 website, which is what we are now.  

[41:13]  
S: What do you think is going on right now with the guys over at PlayStation Network?  Do you think that...

J: Is that still down?

S: Yeah, dude it's still down.

J: Ah, man.  That's just - see but again, it's just like - this is borderline incompetence, this is like laughingstock-type material.

S: So, I'm kinda like wondering what do you think it's like over there? Are they like freaking out and jumping off of buildings and stuff?  Or do you think that they're just like yelling at each other and they're starting to figure out, "Should we put our torpedoes in backwards?" or do you think they're doing this in a very meticulous kind of organized fashion?

J: Those guys are so screwed.  Right there.  I mean, that's sorta the nightmare scenario.  You go down and you like can't come back up.  It's like, "I've fallen and I can't get up." [laughing] Like the old TV commercial.  So, man, I don't even want to think about what that's like.

But that's the type of thing we're trying to avoid.  If you think about how bad that would feel, just as a professional as a person who does a job whether it's running a website or programming - you know, to be such a public example of how not to do it, is like, that's - I don't want to say, "why I get up in the morning", because you get up in the morning because you wanna do positive things - you wanna like make the Internet better, that's the whole... 

S: Right. Right.

J: [inaudible] ... behind Stack Exchange.  But I think the flipside is I wake up in the morning and say, "Hey" - we have a little motto, which is, the way we run Stack Overflow / Stack Exchange is we try, this is what we say, "We try very very hard not to suck."  Ok?  So every day we're like we want to suck a little bit less today, than we did the day before.  Things like being down is like, you know, you're sucking more, not sucking less.

[42:47]  
S: So Google says, "Don't be evil." and you want to "suck less".

J: Yesss ... that's definitely the goal.

Cause we make tons of mistakes and we're very public about our mistakes and what we're doing.  It's a learning process for us, we don't always get it right, but the learning is what's important.  You know, first, recover rapidly.  Rapid turnaround is really important to us.  If something's wrong, fine, fix it fast.  And then learn something from it and move on and keep improving and making things better. 

[43:30]  
Rob: Many thanks to the Stack Overflow team for their story today.  

[musical interlude]

Scott: And again a big thank you to the folks at CodeRush for Visual Studio for helping to support "This Developer's Life".  CodeRush is the fastest rename, the fastest find all references, the fastest test runner.  When it comes to creating, modifying, and refactoring code nothing's faster than CodeRush.  It's been on my ultimate power tools list since forever. Get CodeRush.  You'll be glad you did. Check 'em out at [devexpress.com/coderush](http://devexpress.com/coderush).  We appreciate their support.

[musical outro]