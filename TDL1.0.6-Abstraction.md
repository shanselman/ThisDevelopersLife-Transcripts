=== 1.0.6: Abstractions

==== Introduction

Rob: Hey, everyone. This is Rob and thank you for listening to This Developer's Life, episode number 6.

We'll get to that in just a second. But I had a few things I wanted to talk about.

Number 1: The show hit number one on all technical audio podcasts on iTunes this last week, which was awesome. Also a bit scary. We managed to peg the bandwidth at our ISP who is hosting the audio downloads, and that brought some overage charges. My ISP, as awesome as they are, decided to work with us and forgive it and for that, many, many, many thanks to Maximum ISP. My ISP, I love them. Thank you so much.

In addition, to help out with the costs going forward, we have two volunteers who've stepped up to sponsor us. The first is Twilio, twilio.com. If you need SMS or voice capabilities for your application, go check them out. John Sheehan, at twilio.com, was good enough to help out with sponsoring this episode. In addition, Umbraco, an open source .Net content management system -- they are helping out as well. Do me a favor. Go check out their site and services. They are bringing you this show today. Many thanks from Scott and myself to them.

Now on with the show!

Scott: In the last episode of This Developer's Episode, 1.0.5, called Home Run, I mentioned the idea of geek trading cards. I always thought that there would be computer people looking cards. Right. I would have like, you know, the H. Edward Roberts, creator of the Altair 8080 rookie card. (Oh yeah, I've got Roberts' rookie card. Yeah.) Him and Gary Kildal, you know, who made CPM. I'll trade you an Adam Osborne and a Bill Gates for a Lee Felsenstein, maker of the Osborne 1. Or, you know, Clive Sinclair. You give me a Sinclair for an Andrew Kay, founder of Kaypro. Oh, really? OK, I'll trade you a Steve Jobs rookie card for a Dan Brooklyn.

One of the clever things I said was edited out by our elustrious editor Rob Connery. Always trying to keep the show tight. He edited it out. Now, Rob does the editing of the show. He is the garage band and I am just part of the band. I was a little curious why that remark didn't make it into the show.

Rob: Well, it's not like I was trying to censor you or anything. Well here, I'll just play it.

Scott (replay): "If you haven't heard of Visicalc, you're a bad person. This is the spreadsheet. This is the electronic spreadsheet. He wrote it."

Rob: So, I've actually used Visicalv in the past, and I guess that make's me not a bad person. But, the names on those geek trading cards -- I know a few of them. I mean, who doesn't know who Charles Petzold is? But, some of them I didn't know! Lee Felsenstein -- one of the great names that you dropped there. I don't who Lee Felsensten is.

Scott: Tell me, please tell me that you knew Dan Bricklin.

Rob: Well yeah, ok, I know who Dan Bricklin is. But I only know him because of your show. I honestly didn't know the name before that. I mean, is that important?

Scott: How can you be a programmer and not know who these people are? It's like, flying in an airplane without knowing who the Wright brothers are.

Rob: Honestly. How much do you really need to know about these guys? I mean, what's come before. I mean okay, who started Compaq? Do you know the name of the person who did the first Compaq mini laptop computer?

Scott: Yeah. Well I mean, of course. Compaq was founded in 1982 by Rob Canion, Bill Merto, and Tim Harris and then you know, purchased by Hewlett Packard in 2002. How do you not know this?

Rob: Well, I'm just saying. Why do I need to? Who needs to know that now? They're gone. I mean, other than a little bit of trivia, who cares?

[short, scary violin interlude]

Alright, so let's skip ahead just a little bit. Scott and I got into a great discussion about, well, history. And things that you need to know, and next thing you know, we're talking about abstraction. Now my point was, what do I really need to know from the past in order to do my job today? Scott brought up a great point. He said, "Well, the past was where the abstraction was born." In other words, all the frameworks we use today abstract the things that were learned in the past. Something I really hadn't thought about. So let's jump ahead to that part of the discussion.

Scott: OK, well when does layers of abstraction become trivial? When they're buried so deep in the layers that it doesn't matter. I mean, there's all these commandments, right? "Thou shalt not kill." Should we worry about the why? Or should we just focus on the "not killing" part?

Rob: Sure, but I mean come on. That's like religion, cultural, socio-political stuff like that. They cause wars and hurt people. We're talking about computers, and software. I mean, how do you… do you even want to repeat the craziness that came before if you think about this in a historical setting? I sure don't.

Scott: But we are repeating it. I mean, we're building giant mainframes, again, that do big, batch processing, except we're calling them "the cloud." Do we think we're doing that because it's all twenty year olds that are building the cloud?

Rob: It's interesting to bring that up, because a lot of people are likening the cloud to mainframe 2.0.

Scott: Well remember the guy that said that there is at most a market for about five computers in the world. And here we are, building five computers. You know who that was?

Rob: No, I don't. Dan Bricklin.

Scott: That was Thomas J. Watson, and he was the president of I.B.M. He said, "There is a market for about five computers."

Alright, let's forget about those five computers. Let's think about this in terms of people. We can look to the past, and we can look to the patterns, we can look to the computers of the past. But, why don't we try looking at the people of the past that are still around today doing innovative things. People like Ward Cunningham. People like Dan Bricklin that we talked to last week. People like Charles Petzold. These people bridge yesterday and today. We've got the guy that wrote Visicalc writing iPad applications. We've got the guy that invented the wiki, whose working on sensor arrays in his home. We've got the guy who wrote Programming Windows 3.1, whose now writing Windows Phone 7 applications. These people made history and continue to build the future.

[interview transition]

Unidentified voice: I'm talking in my normal voice. How loud am I now?

Scott: That's perfect.

[end of interview transition]

==== Ward Cunningham

I was thinking I would go talk to Ward Cunningham. Maybe you've heard about the idea of a wiki. He's the guy that invented the wiki. Do you ever wish you had like a crazy, old uncle. But instead of the kind that would take you fishing all the time, he would take you down to the cave and show you how to burn things, and do physics experiments? This is what Ward's house is like. You come in, and you immediately know that there's electronic parts being shipped to and from. And he says, "Let's go downstairs into the workshop." And you go down into the workshop, and it's like, this wonderful episode of hoarders. But not the bad hoarders where they hoard all sorts of things that they should have thrown away. This is the good kind of hoarders where you've got fifty years of computing history in here. There's literally a PowerBook next to a brand new Mac. And a Windows machine next to an oscilloscope.

[space music interlude; dial tones and modem connection negotiation chirps]

He's got fifty projects, all running at the same time. And you ask him why he's doing it. And he says:

Ward: Well I want to understand the whole stack.

Scott: So I try to think of the smartest thing I could ask. I mean, this guy's got a master's degree from Purdue and I went to a community college. So I asked him: What do I need to know? Do I have to understand a Turing machine in order to write business software?

Ward: Well, I think, clearly not because there's a lot of business applications written by people who don't understand Turing machines. But, there is something that happens to you as a person, in terms of stroking your curiosity, when you discover that you can understand a Turing and understand why a Turing machine has something -- not a lot maybe -- but something to say about a business application. And that "something" could come in handy some time.

Scott: Ward makes a really good point because he's saying understanding abstractions _does_ come in handy. The question is, when do you stop?

I tell this story a lot, about how my wife lost her wedding ring in the drain. My wife is a very smart person. She's got a master degree in business, and she has no problem understanding big concepts. But she chooses to ignore some. And one of the ones that she's chosen to ignore is the idea of plumbing. She dropped her ring, her wedding ring, down the drain. And it was gone. Because, for her, at that point where the drain enters the sink and disappears, it effectively goes into a black hole. She's not a plumber. She has no interest in plumbing. Her mental model of the way that water flows through the house is: water appears at the faucet, travels six inches, and then disappears from the universe. My mental model goes slightly farther. I'm not a plumber. My model doesn't go all the way to the sewage treatment plant. But it does go about two feet underneath the sink to a layer in the call stack, as it were, that my wife doesn't have. So I opened up the cabinets. I pulled the little trap U thingy. (You see how my mental model doesn't include the name of that thing?) I pulled that U-trap deal, and I rescued her wedding ring from the black hole. And just as any sufficiently advanced technology is indistinguishable from magic, any sufficiently abstract layer is also indistinguishable from magic. So this again brings us to that question: What level of abstraction is right?

Ward: You know, I've had this conversation with my brother. And my older brother got into electronics early in high school. And I probably became technical just trying to impress my brother. But, he stayed for a long time at the electronics level and wouldn't do software, because he just thought what happens in software is foolish. But you can't do that for long. It's a software world. He's been drug into it. And he's been drug from the bottom up, all self-taught.

Scott: Um hmm.

Ward: And we talk about what kind of the average person knows about how things work, and what he knows about how things work. And he'd talk about it, and he's incredulous, and he just says to me. He says, "How do they ever debug their programs?" And I just say, well, they don't. You know? There's bugs in the program because they simply don't have the knowledge to remove them. Or the inclination. And maybe you can say, the economic motivation for making bug free programs is simply not there. But, he likes knowing how things work. And he likes making things that work. And to him, working _completely_ is something that matters. That's just, you know, I think of it as kind of an engineering mentality. I've worked with a lot of engineers over the years that know more about how the computer works inside than how to program it effectively. And, they have a reputation of writing what you might call sloppy code, or poorly factored code. Everything's in a big pile, and it just does what it needs to do. It's probably beautiful at a level below that. And I see that people who care a lot about how their code works don't have a lot of respect for the engineers that write code. It's very empowering to know what's going on at every level. And there's lots of different levels in our software. My brother says, "How do you find the bugs if you don't know all the levels?" But then I think we drift in this like, "What is a bug? Is it a bug if a program is not organized as modules?" At some point it is, because you can't build up. You know, you debug down, but can you build up? So you need modularity at every level. And discovering that modularity means you have to understand what's important at a given level. And once you know what's important at a level, you can organize that level to serve the needs of what's important. And then that frees yourself to work at a level higher, or other people to work at a level higher. And if they choose to work at a level higher without digging down, you know you've succeeded, in some sense. But those people won't be like you. I think that anybody who builds anything that's meant to be accessible -- whether it’s the guy who's designing a flip flop so that you can store a bit. As a circuit designer, without having to figure out how to store, you buy that package and you put it in your circuit and you've got an abstraction. Well, that flip flop has to flip when you need it to flip. And that means it has to have characteristics. There is something you could check on Wikipedia called the meta-stability of synchronizers. And that is a study of when flip flops failed to flip. And what you do is you get down to the analog world, out of the digital. Now, a good circuit designer knows enough about meta-stability that he doesn't push his flip flops too hard. But, the same thing if say you're working at the highest level of business applications. And, you're using powerful blocks. And, you stick them together and you say: Well, I know this is a powerful block, but I know underneath this it's a database query. And because we have this many tables that are this big, that's database query is going to take minutes, not seconds, or milliseconds. And you say: If we need to do it, we could have a button and you could press it and take a minute, but you want to think twice before you do that because somebody's going to think it's broken. And that's where, even with great tools, the lower level can kind of leak up to the upper level, and it really helps to know. Now, you may just need to know that that query's going to take a minute. You don't necessarily need to know why it's going to take a minute. Or, what it's doing during that minute. What's happening on the disk head, going in and out, or something. So some guy who wrote a database optimizer tried to shield you from that knowledge, and hopefully he's done a great job. So, I would say, I like to build things at a lot of different levels of abstraction. And I like to go down to the lowest level and debug things with an oscilloscope. And when I build on my own layers, I get to build the right way. Because, I don't have to enslave myself from what's going on deep down. When I build for myself, I can make very clever things that use almost no parts to do powerful functions. But, I get away with that, because I don't have to make my components so robust that  when I'm working at a higher level, I can absolutely forget what's going on at the lower level. I like to think up and down. I like to debug. I like to be building something that's running on my cell phone, that's talking to a web server on my laptop, that's talking to a microcomputer, that's talking to a little circuit. And I like to be able to plug my oscilloscope to that circuit and touch my phone and watch all that stuff work. I like to go up and down the levels and to infer what's happening. But, that's because I know all the levels. It strokes my sense of power.

[musical interlude (Kraftwerk's Pocket Calculator)]

Rob: Ward builds oscilloscopes. What?!

Scott: Yes. Yes. He worked for Tektronix and this was _the place_ that built oscillioscopes. This was the company that built the building blocks that allowed people to create other computers. It was huge. And it's actually down the street from my house. And, walking into Ward's basement was just like walking into this wonderful computer version of the show Hoarders. Except, he was only keeping cool stuff. It wasn't like trash bags and things like you see when you think about someone hoarding. It was just, wonderful, half-built robots and automatons, and pieces of art with servo motors and oscilloscopes and… This is the guy who's got a brand new computer next to a soldering iron. He can grab either one. Whatever tool he needs at whatever layer he needs to work at. He can just grab it and go.

Rob: I can definitely identify, though, with one thing that Ward said in the story there. If I go down deep enough… Well here, I'll let him say it.

Ward (replay): I like to build things at a lot of different levels of abstraction. I like to go down to the lowest level and debug things with an oscilloscope. And when I build on my own layers, I get to build the right way. Because I don't have to enslave myself from what's on deep down.

Rob: So lately, I've really been enjoying all the light weight tools out there that are coming. Like WebMatrix for .Net, or Razor view engine. Sinatra for Ruby. The abstraction is in there and there's not this large API you have to understand. It kind of just gets you to the work. And I just mentioned this in the Sinatra series that I did, that, I felt that Sinatra was a great framework for craftsman. In that, you got to get in there and write only what you needed, and write it your way. And for a lot of people that makes it better.

Scott: Right! For a lot of people who like to write code and tinker, that layer of abstraction can be a pain. It's a lie. They don't like being lied to. They really want to get down and get dirty. They want to see what's happening.

==== Professor Connery

Rob: One thing I don't want to do is relive what these guys had to go through, in terms of what they needed to understand just to get their work done! Don't get me wrong. I like abstraction. And well, I spoke to my brother who I've mentioned on my blog a few times. He's a professor up at University of Oregon, in Eugene. Did I say Eugene right this time?

Scott: Yes, it's Eugene.

Rob. Eugene.

Scott: It's not YOU-gene. It's Eugene.

Rob: I always get that wrong. So he's a professor of Computer Science up there. And check this out: This is what he had to do to log into his computer.

Rob's brother: This is a great story. Alright, so it was a PGP-12. You go into the lab and it had a key. When you turn the key, and that turned the ignition and it'd fire her up, because it had been shut down the night before. And, when it came up, it was up. It wasn't running. And so there was an on/off, there was a Start switch. And this was well before there were any kind of crons or any kind of rebuilding memories. And so, what we would do, was a twelve bit word. And there were twelve keys on the console. Twelve toggle switches. And you'd have a switch up for a one bit and down for a zero bit. And you would toggle in the bootstrap code. And so, the simplest one is the two liner. You'd type switch settings for the twelve bit word you want and then push a button and it'd enter that word into memory. And then you set the toggle switches for the next twelve bit word and you just hit the switch again and it'd go into the next word after that. So now that you got these two twelve bit words in there, that's a two line program. A two instruction program. And then you hit the Go button, and the computer would jump to the location where you entered the bootstrap and fire up. And if you did it right, that was a little two line program that said go get the first block off of the tape and load it into memory. And that would be your operating system. It'd fire up and there you go.

Rob: And how long did this process usually take?

Rob's brother: Well, since you did it every day or a couple times a day… Probably about one second! [laughter] You just knew… That's a little bit of an exaggeration. In fact, it's pretty silly. Those toggle switches would be almost in position from the last time somebody keyed it in. So, you didn't have to do too much switching around. You just know what the… And it was an interesting pattern. It was probably like… For some reason I remember the seven thousands. That would be the last three up and the right nine down, or something like that. So, you just come in and smack those things around, hit the button, and do another little one. So, a couple seconds.

Rob: So, how hard was it to figure out what somebody else's login sequence was?

Rob's brother: There was no login sequence. [laughter] If you had the key, you had the computer.

Rob: So that's just old technology right there. I mean, using toggles to log in to a mainframe. I guess I just don't see the relevance of that today, necessarily. Know what I mean?

Scott: Well, and that's where you get into the philosophy of it. Is he a better person. Like demonstrably and objectively a better person? Probably not. But, how can you not want to know this stuff? And isn't that, he _knows_ how the login system works now. Now I suppose I could just type in my name and my password and hit enter, and just hope that some magic gnomes take my password over to the server and do it. And for I know, there was magic gnomes. But to really know what's happening there, understand the chain that's in place, to know that those toggles cause some hashing algorithms to do some work. That's inspiration that you can use in your work. Just the knowing of that, at your core, even if you don't consciously know it, can make you a more effective coder. Let's do some mixed metaphors here. You're standing on the shoulders of giants, sure. But I mean, your crown has been paid for. You just need to put it on. You don't need to know any of the wars, and the drama, and the mainframes, and the mini-computers, and the Apple II that came before you. Alright. Guys like Dan Bricklin did that work for you. They fought those wars. They invented this stuff from scratch.

==== Dan Bricklin

And look, what I talked to Dan last week, what he said about developing UIs.

[musical interlude]

Dan: Back then, I had to figure out, what does each keystroke do? So the state diagram, if you look at it… Some of it's on my web site, and it's in some books, like Programmers at Work. I have, I think, some of it's in my book, Bricklin on Technology. But, there I had to say, if you pressed the Splash key, what could you do next? If you pressed the Arrow key, what could you do next? If you pressed the Plus key? Because that's what we had to figure out. And that's how the system worked. On today's system, more you worry about what's on the screen. What buttons are on the screen? What can you do? What can you drag? There's some of the same stuff that I did that did not make it into the books, where I haven't shared some of my early data layout. Obviously, as a programmer, one of the most important things is what the data layout looks like. And I was very concerned about that, figuring out how we were going to be storing the sheet, to be able to fit in the little bit of memory that we had. We only had about 16 K or so of memory. Sixteen thousand bytes. To be able to hold a reasonable amount of data to make this useful. So, you had to be very compact. And, so I was figuring out how to do that, and I think Bob used some of my design for that. And for a lot of applications after that, I had to do the same things. I do that, obviously, today. I have to look at what's the data layout of how I'm doing it, just like programming has probably always been. And, you decide when you click here, what can you go to. If there are keystrokes, then you do a state diagram. So, it's always something like that. And I'm scribbling them down. And I actually used paper, or sometimes do it on my application itself. We had to develop things like, invent the ruler, which you now take for granted. But in the word processor, the thing with the tabs on it and all. The embedded ruler. Each of us had to invent that independently for our word processors. So this stuff just goes on and on and on. It's part of the craft. A lot of the stuff is just part of the craft. It's why some old timers will laugh at some of the youngsters who think that this is new. They think that some of the concepts are new, because they were able to do it for the first time, and they don't know people did in the sixties, and seventies, and eighties.

Dan: A lot of that wasn't saved because the computers don't continue to run. Old software doesn't always run on new computers. I've been lucky. Visicalc was written for the I.B.M. PC among other things. It was about a year or two, a couple of years after it first came out. And we copy protected it because that's what was done in those days. Copy protection. But one of our employees kept an internal version of it, that was not copy protected, and kept it on one of his computers. And when he left, took it with him. And he gave me that copy years later. He was into history and I had borrowed old stuff from him, and he said, "Hey, I have this old copy of Visicalc!" Since it wasn't copy protected, I could actually use it on new machines years later. Because the copy protection assumed certain hardware, it took advantage of that hardware to know whether it was a copy of the software or the original disk. So that version got put up and I have that up on my web site. And thousands and thousands of people downloaded it. They can run what was Visicalc back in 1981. Well, apparently, Microsoft has used that as part of the test suite to see if new versions of Windows are compatible backwards. So, it's stayed compatible for many, many, many years. Which is kind of cool. But, that's highly unusual.

Rob: Yeah. Dan. Dan is amazing.

Scott: I mean don't you just feel smarter because you listened to him talk? I mean, he's just _mainlining_ information.

==== Charles Petzold

Rob: Yeah, absolutely. Something that's fascinated me as well is that… Well, I listened to the recording you did last week with Charles Petzold. 

Scott: Yeah, yeah. I talked to him a couple weeks ago, basically about that same things I asked Ward. What do we need to know?

Rob: He's amazing. This is my favorite part.

Scott: If you know how to take a C program and hand assemble it and all, are you a smarter programmer? Are you a better person? Are you…?

Charles: Umm. That I do not know. Sometimes, it goes the other way, though. Certainly, my assembly language programming days, and my C programming days kind of overlapped. And, once I got familiar with higher level structures in C, I started applying those to my assembly language programming. I had a similar experience when I first started using, um… It was the first version of BASIC for Windows. Seeing how, in Visual Basic, you would design a window of controls. I started doing that kind of thing in my C Windows programming, where it wasn't so obvious. So I've had more the experience of going in the opposite direction; of applying high level concepts and structures in lower level languages. Whether any programmer these days has the time to start off with digital design, and then have a good foundation in assembly language, and then move up the scale from C to C++ to C#... That seems to me a little too much to ask of the education system and of the individual programmer. Certainly, people don't seem to have the patience for that type of long learning. It was certainly different when you're encountering these things as they are introduced into the market. When you are back working when the only assembly language programming you could do at home was on the 8080 or the Z80. You encountered these things historically as they become wide spread in the market. By the time C# is introduced, you already have a couple of decades of backgrounds in all this. I don't think you want to necessarily take a young programmer and force them to go through this entire history of building up things. For those of us who lived through it, it took twenty years to get me from 8080 assembly language to C#. [laughter] That's a long education!

Scott: Ward likes to know the complete stack so that he can debug it. But also so that he knows which part he can rewrite his way. And basically invented the stack. He did everything that he needed to do in order to get Visicalc to work, but he was working at a very, very low level, doing a lot of this stuff in assembly language. But in answering this question, Charles is acknowledging that there's just a whole lot of stuff to know. It's probably a bit much to learn it all. This is something that many people can probably identify with. But what parts can we let go? As Rob and I are discussing, those who are unaware of the past are doomed to repeat it. And in that same way, those who are unaware of the lower levels of abstraction are doomed to rewrite it. That's what I asked Charles next. What things can the developer today safely forget?

Charles: Nothing comes to mind off hand. Maybe you really do have to learn all this stuff? I don't know. There seems to be quite a few programmers who do just fine without it. Is that what's important? Well, it's important if you think of programming in a corporate sense, of delivering products to the market. But I hope that there is still a lot of programmers who have this interest in history. There's always been a retro-computing movement. I'm not sure that I personally would enjoy going back to coding for 16-bit Windows, but some people get a kick out of it.

Scott: Yeah, I mean he's doing some great stuff. And he's writing a wonderful book on Windows Phone 7. I think what makes his book special is that he's got that context. He's got twenty plus years of Windows. Gosh, almost 25-30 years of Windows.

Rob: I know, but you'll agree that he struggled a bit when he was answering that question, "What do we really need to know?"

Scott: Well, yeah, I mean he seemed to be at a bit of a loss.

Rob: I'll tell you what. One thing that struck me about the audio from Charles, and from Dan, and from Ward, is: these guys are really excited about what they're doing now. They don't really care, much, or it doesn't seem like they have any nostalgic reverence for the past. They're as motivated now as they've ever been.

Scott: That's really what's surprised me. I expect that I'd be sitting down with three great uncle types. Maybe not grandfatherly -- we'll give them that respect. But you know, a slightly elder, great uncle type. And that they were going to tell me about how awesome it was in the past, and how much more the past influenced them. But, none of them seemed all that interested in dwelling on the stuff that they did before. I thought they were going to give me some wisdom as I climbed the mountain all the way up to the top. And they would just lay it on me. But honestly, they were excited about programming _today_. I'm not even sure, but I think Petzold may have been programming while I was talking to him.

Scott (back to interview with Charles): Well, you just finished a book on Windows Phone.

Charles: Right. Well, I'm still working on it. Almost as we speak, I'm actually coding while I'm going to be doing the interview. [chuckles]

Rob: It definitely sounded that way, because it took him a while to uh… when you asked him a question. And then he came out and said it! "I'm actually writing code right now." And I just love that. He's so passionate about the work he's doing. You could just tell he was wrapped up in it.

Scott: I mean, yeah. We were talking and I'm kind of hearing [muffled key stroke noises]. I'm like, "Are you multitasking?" I mean yeah, look at Dan. Dan's making this new application for the iPad.

(paused at 35:25)
