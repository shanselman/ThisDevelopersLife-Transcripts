### 1.0.6: Abstractions

#### Introduction

Rob: Hey, everyone. This is Rob and thank you for listening to This Developer's Life, episode number 6.

We'll get to that in just a second. But, I had a few things I wanted to talk about.

Number 1: The show hit number one on all technical audio podcasts on iTunes this last week, which was awesome. Also a bit scary. We managed to peg the bandwidth at our ISP where I was hosting the audio downloads, and that brought some bandwidth overage charges. My ISP, as awesome as they are, decided to work with us and forgive it and for that, many, many, many thanks to Maximum ISP ([maximumisp.com](http://maximumisp.com/)). My ISP, I love them. Thank you so much.

In addition, to help out with the costs going forward, we have two volunteers who've stepped up to sponsor us. The first is Twilio ([twilio.com](http://twilio.com/)). If you need SMS or voice capabilities for your application, go check them out. John Sheehan, at twilio.com, was good enough to help out with sponsoring this episode. In addition, Umbraco ([umbraco.com](http://umbraco.com/)), an open source .NET content management system -- they are helping out as well. Do me a favor. Go check out their site and services. They are bringing you this show today. Many thanks from Scott and myself to them.

Now on with the show!

Scott: In the last episode of This Developer's Episode, 1.0.5, called Home Run, I mentioned the idea of geek trading cards. I always thought that there would be computer people rookie cards. Right. I would have the H. Edward Roberts, creator of the Altair 8080, rookie card. (Oh yeah, I've got Roberts' rookie card. Yeah.) Him and Gary Kildall, who made CPM. I'll trade you an Adam Osborne and a Bill Gates for a Lee Felsenstein, maker of the Osborne 1. Or, Clive Sinclair. You give me a Sinclair for an Andrew Kay, founder of Kaypro. Oh, really? Okay, I'll trade you a Steve Jobs rookie card for a Dan Bricklin.

One of the clever things I said was edited out by our illustrious editor Rob Conery. Always trying to keep the show tight. He edited it out. Now, since Rob does the editing of the show, he is the garage band and I am just part of the band. I was a little curious why that remark didn't make it into the show.

Rob: Well, it's not like I was trying to censor you or anything. Well here, I'll just play it.

Scott (replay): "If you haven't heard of VisiCalc, you're a bad person. This is the spreadsheet. This is the electronic spreadsheet. He wrote it."

Rob: So, I've actually used VisiCalc in the past, and I guess that makes me not a bad person. But, the names on those geek trading cards -- I know a few of them. I mean, who doesn't know who Charles Petzold is? But, some of them I didn't know! Lee Felsenstein -- one of the great names that you dropped there. I don't who Lee Felsensten is.

Scott: Tell me, please tell me that you knew Dan Bricklin.

Rob: Well yeah, ok, I know who Dan Bricklin is. But I only know him because of your show. I honestly didn't know the name before that. I mean, is that important?

Scott: How can you be a programmer and not know who these people are? It's like flying in an airplane without knowing who the Wright brothers are.

Rob: Honestly. How much do you really need to know about these guys? I mean, what's come before. I mean, who started Compaq? Do you know the name of the person who did the first Compaq mini laptop computer?

Scott: Yeah. Well I mean, of course. Compaq was founded in 1982 by Rod Canion, Bill Murto, and Jim Harris, and then purchased by Hewlett Packard in 2002. How do you not know this?

Rob: Well, I'm just saying. Why do I need to? Who needs to know that now? They're gone. I mean, other than a little bit of trivia, who cares?

[short, scary violin interlude]

Alright, so let's skip ahead just a little bit. Scott and I got into a great discussion about history and things that you need to know. Next thing you know, we're talking about abstraction. My point was, what do I really need to know from the past in order to do my job today? Scott brought up a great point. He said, "Well, the past was where the abstraction was born." In other words, all the frameworks we use today abstract the things that were learned in the past. Something I really hadn't thought about. Let's jump ahead to that part of the discussion.

Scott: When does layers of abstraction become trivial? When they're buried so deep in the layers that it doesn't matter.

I mean, there's all these commandments, right? "Thou shalt not kill." Should we worry about the _why?_ Or, should we just focus on the "not killing" part?

Rob: Sure, but come on. That's like religion, cultural, socio-political stuff like that. They cause wars and hurt people. We're talking about computers, and software. Do you even want to repeat the craziness that came before if you think about this in a historical setting? I sure don't.

Scott: But we are repeating it. We're building giant mainframes, again, that do big, batch processing, except we're calling them "the cloud." Do we think we're doing that because it's all twenty year olds that are building the cloud?

Rob: It's interesting to bring that up, because a lot of people are likening the cloud to mainframe 2.0.

Scott: Remember the guy that said that there is at most a market for about five computers in the world. And here we are, building five computers. You know who that was?

Rob: No, I don't. Dan Bricklin?

Scott: That was Thomas J. Watson, and he was the president of IBM. He said, "There is a market for about five computers."

Alright, let's forget about those five computers. Let's think about this in terms of people.

We can look to the past, and we can look to the patterns, we can look to the computers of the past. But, why don't we try looking at the people of the past that are still around today doing innovative things. People like Ward Cunningham. People like Dan Bricklin that we talked to last week. People like Charles Petzold.

These people bridge yesterday and today. We've got the guy that wrote VisiCalc writing iPad applications. We've got the guy that invented the wiki, whose working on sensor arrays in his home. We've got the guy who wrote _Programming Windows 3.1,_ whose now writing Windows Phone 7 applications. These people made history and continue to build the future.

[interview transition]

Unidentified voice: I'm talking in my normal voice. How loud am I now?

Scott: That's perfect.

[end of interview transition]

#### Ward Cunningham

I was thinking I would go talk to Ward Cunningham. Maybe you've heard about the idea of a wiki. Well, he's the guy that invented the wiki.

Do you ever wish you had a crazy, old uncle? But, instead of the kind that would take you fishing all the time, he would take you down to the cave and show you how to burn things, and do physics experiments?

This is what Ward's house is like. You come in, and you immediately know that there's electronic parts being shipped to and from. And he says, "Let's go downstairs into the workshop." And you go down into the workshop, and it's like this wonderful episode of hoarders. But not the bad hoarders where they hoard all sorts of things that they should have thrown away. This is the good kind of hoarders where you've got fifty years of computing history in here. There's literally a PowerBook next to a brand new Mac. And a Windows machine next to an oscilloscope.

[space music interlude; dial tones and modem connection negotiation chirps]

He's got fifty projects, all running at the same time. You ask him why he's doing it, and he says:

Ward: Well, I want to understand the whole stack.

Scott: I try to think of the smartest thing I could ask. I mean, this guy's got a Master's degree from Purdue and I went to a community college. So, I asked him: What do I need to know? Do I have to understand a Turing machine in order to write business software?

Ward: Well, I think, clearly not, because there's a lot of business applications written by people who don't understand Turing machines. But, there is something that happens to you as a person, in terms of stroking your curiosity, when you discover that you can understand a Turing machine and understand why a Turing machine has something -- not a lot maybe -- but something to say about a business application. And that "something" could come in handy some time.

Scott (to Rob): Ward makes a really good point because he's saying understanding abstractions _does_ come in handy. The question is, when do you stop?

I tell this story a lot, about how my wife lost her wedding ring in the drain. My wife's a very smart person. She's got a Master's degree in business, and she has no problem understanding big concepts. But she chooses to ignore some. And one of the ones that she's chosen to ignore is the idea of plumbing.

She dropped her ring -- her wedding ring -- down the drain. And it was gone. Because, for her, at that point where the drain enters the sink and disappears, it effectively goes into a black hole.

She's not a plumber. She has no interest in plumbing. Her mental model of the way that water flows through the house is: water appears at the faucet, travels six inches, and then disappears from the universe.

My mental model goes slightly farther. I'm not a plumber. My model doesn't go all the way to the sewage treatment plant. But it does go about two feet underneath the sink to a layer in the call stack, as it were, that my wife doesn't have.

So I opened up the cabinets. I pulled the little trap U thingy. (You see how my mental model doesn't include the name of that thing?) I pulled that U-trap deal, and I rescued her wedding ring from the black hole.

And just as any sufficiently advanced technology is indistinguishable from magic, any sufficiently abstract layer is also indistinguishable from magic. So this again brings us to that question: What level of abstraction is right?

Ward: You know, I've had this conversation with my brother. My older brother got into electronics early in high school. I probably became technical just trying to impress my brother. But, he stayed for a long time at the electronics level and wouldn't do software, because he just thought what happens in software is foolish.

You can't do that for long. It's a software world. He's been drug into it. And he's been drug from the bottom up, all self-taught.

Scott: Mm hmm [expresses agreement].

Ward: And we talk about what the average person knows about how things work, and what _he_ knows about how things work. And he'd talk about it, and he's incredulous, and he just says to me, "How do they ever debug their programs?"

I just say, "Well, they don't." You know? There's bugs in the program because they simply don't have the knowledge to remove them. Or the inclination. Maybe the economic motivation for making bug free programs is simply not there.

But, he likes knowing how things work. He likes making things that work. To him, working _completely_ is something that matters.

I think of it as kind of an engineering mentality. I've worked with a lot of engineers over the years that know more about how the computer works inside than how to program it effectively. They have a reputation of writing what you might call sloppy code, or poorly factored code. Everything's in a big pile, and it just does what it needs to do. It's probably beautiful at a level below that.

I see that people who care a lot about how their code works don't have a lot of respect for the engineers that write code. It's very empowering to know what's going on at every level. There's lots of different levels in our software. My brother says, "How do you find the bugs if you don't know all the levels?"

Then I think we drift in this like, "What is a bug? Is it a bug if a program is not organized as modules?" At some point it is, because you can't build up. You debug down, but can you build up? You need modularity at every level. And discovering that modularity means you have to understand what's important at a given level.

Once you know what's important at a level, you can organize that level to serve the needs of what's important. And then that frees yourself to work at a level higher, or other people to work at a level higher. And if they choose to work at a level higher without digging down, you know you've succeeded, in some sense.

But those people won't be like you. I think that anybody who builds anything that's meant to be accessible -- whether it’s the guy who's designing a flip flop so that you can store a bit. As a circuit designer, without having to figure out how to store, you buy that package and you put it in your circuit and you've got an abstraction. Well, that flip flop has to flip when you need it to flip. And that means it has to have characteristics.

There is something you could check on Wikipedia called the metastability of synchronizers. And that is a study of when flip flops failed to flip. And what you do is you get down to the analog world, out of the digital. Now, a good circuit designer knows enough about metastability that he doesn't push his flip flops too hard.

The same thing if you're working at the highest level of business applications. You're using powerful blocks. You stick them together and you say: Well, I know this is a powerful block, but I know underneath this it's a database query. And because we have this many tables that are this big, that's database query is going to take minutes, not seconds, or milliseconds. You say: If we need to do it, we could have a button and you could press it and take a minute, but you want to think twice before you do that because somebody's going to think it's broken.

And that's where, even with great tools, the lower level can kind of leak up to the upper level, and it really helps to know. You may just need to know that that query's going to take a minute. You don't necessarily need to know why it's going to take a minute. Or, what it's doing during that minute. What's happening on the disk head, going in and out, or something. Some guy who wrote a database optimizer tried to shield you from that knowledge, and hopefully he's done a great job.

So, I would say, I like to build things at a lot of different levels of abstraction. I like to go down to the lowest level and debug things with an oscilloscope. And when I build on my own layers, I get to build real light weight. Because, I don't have to insulate myself from what's going on deep down. When I build for myself, I can make very clever things that use almost no parts to do powerful functions.

I get away with that, because I don't have to make my components so robust that when I'm working at a higher level, I can absolutely forget what's going on at the lower level.

I like to think up and down. I like to debug. I like to be building something that's running on my cell phone, that's talking to a web server on my laptop, that's talking to a microcomputer, that's talking to a little circuit. I like to be able to plug my oscilloscope to that circuit and touch my phone and watch all that stuff work.

I like to go up and down the levels and to infer what's happening. That's because I know all the levels. It strokes my sense of power.

[musical interlude (Kraftwerk's Pocket Calculator)]

Rob: Ward builds oscilloscopes. What?!

Scott: Yes. Yes. He worked for Tektronix and this was _the place_ that built oscilloscopes. This was the company that built the building blocks that allowed people to create other computers. It was huge. And it's actually down the street from my house.

Walking into Ward's basement was just like walking into this wonderful computer version of the show Hoarders. Except, he was only keeping cool stuff. It wasn't like trash bags and things like you see when you think about someone hoarding. It was just, wonderful, half-built robots and automatons, and pieces of art with servo motors and oscilloscopes and… This is the guy who's got a brand new computer next to a soldering iron. He can grab either one. Whatever tool he needs at whatever layer he needs to work at. He can just grab it and go.

Rob: I can definitely identify, though, with one thing that Ward said in the story there. If I go down deep enough… Well here, I'll let him say it.

Ward (replay): I like to build things at a lot of different levels of abstraction. I like to go down to the lowest level and debug things with an oscilloscope. And when I build on my own layers, I get to build real light weight. Because, I don't have to insulate myself from what's going on deep down.

Rob: So lately, I've really been enjoying all the light weight tools out there that are coming. Like WebMatrix for .NET, or Razor view engine. Sinatra for Ruby. The abstraction is in there and there's not this large API you have to understand. It kind of just gets you to the work. And I just mentioned this in the Sinatra series that I did, that I felt that Sinatra was a great framework for craftsman. In that, you got to get in there and write only what you needed, and write it your way. For a lot of people that makes it better.

Scott: Right! For a lot of people who like to write code and tinker, that layer of abstraction can be a pain. It's a lie. They don't like being lied to. They really want to get down and get dirty. They want to see what's happening.

#### Professor Conery

Rob: One thing I don't want to do is relive what these guys had to go through, in terms of what they needed to understand just to get their work done! Don't get me wrong. I like abstraction.

I spoke to my brother who I've mentioned on my blog a few times. He's a professor up at University of Oregon, in Eugene. Did I say Eugene right this time?

Scott: Yes, it's Eugene.

Rob. Eugene.

Scott: It's not YOU-gene. It's Eugene.

Rob: I always get that wrong. So, he's a professor of computer science up there. Check this out: This is what he had to do to log into his computer.

Professor Conery: This is a great story. Alright, it was a PGP-12. You go into the lab and it had a key. When you turn the key, that turned the ignition and it'd fire her up, because it had been shut down the night before. When it came up, it was up. It wasn't running. There was an on/off, there was a Start switch. This was well before there were any kind of crons or any kind of rebuilding memories.

What we would do, was a twelve bit word. There were twelve keys on the console. Twelve toggle switches. You'd have a switch up for a one bit and down for a zero bit.

You would toggle in the bootstrap program. The simplest one is the two liner. You'd type switch settings for the twelve bit word you want and then push a button and it'd enter that word into memory. And then you set the toggle switches for the next twelve bit word and you just hit the switch, again, and it'd go into the next word after that. Now that you got these two twelve bit words in there, that's a two line program. A two instruction program.

Then you hit the Go button, and the computer would jump to the location where you entered the bootstrap and fire up. If you did it right, that was a little two line program that said "go get the first block off of the tape and load it into memory."

And that would be your operating system. It'd fire up and there you go.

Rob: And how long did this process usually take?

Professor Conery: Well, since you did it every day or a couple times a day… Probably about one second! [laughter] You just knew…

That's a little bit of an exaggeration. In fact, it's pretty silly. Those toggle switches would be almost in position from the last time somebody keyed it in. So, you didn't have to do too much switching around. You just know what the…

And it was an interesting pattern. It was probably like… For some reason I remember the seven thousands. That would be the left three up and the right nine down, or something like that. So, you just come in and smack those things around, hit the button, and do another little one. So, a couple seconds.

Rob: How hard was it to figure out what somebody else's login sequence was?

Professor Conery: There was no login sequence. [chuckles] If you had the key, you had the computer.

Rob: That's just old technology right there. I mean, using toggles to log in to a mainframe. I guess I just don't see the relevance of that today, necessarily. Know what I mean?

Scott: Well, and that's where you get into the philosophy of it. Is he a better person? Like demonstrably and objectively a better person? Probably not. But, how can you not want to know this stuff?

He _knows_ how the login system works now. Now I suppose I could just type in my name and my password and hit enter, and just hope that some magic gnomes take my password over to the server and do it. And for all I know, there was magic gnomes.

But to really know what's happening there, understand the chain that's in place, to know that those toggles cause some hashing algorithms to do some work. That's inspiration that you can use in your work. Just the knowing of that, at your core, even if you don't consciously know it, can make you a more effective coder.

Let's do some mixed metaphors here. You're standing on the shoulders of giants, sure. Your crown has been paid for. You just need to put it on. You don't need to know any of the wars, and the drama, and the mainframes, and the mini-computers, and the Apple II that came before you. Alright. Guys like Dan Bricklin did that work for you. They fought those wars. They invented this stuff from scratch.

#### Dan Bricklin

Scott: And look, what I talked to Dan last week, what he said about developing UIs.

[musical interlude]

Dan: Back then, I had to figure out, what does each keystroke do? The state diagram, if you look at it… Some of it's on my web site, and it's in some books, like _Programmers at Work_. I have, I think, some of it in my book, _Bricklin on Technology_.

There I had to say, if you pressed the Slash key, what could you do next? If you pressed the Arrow key, what could you do next? If you pressed the Plus key? Because that's what we had to figure out. And that's how the system worked.

On today's system, more you worry about what's on the screen. What buttons are on the screen? What can you do? What can you drag? There's some of the same stuff that I did that did not make it into the books, where I haven't shared some of my early data layout.

Obviously, as a programmer, one of the most important things is what the data layout looks like. I was very concerned about that, figuring out how we were going to be storing the sheet, to be able to fit in the little bit of memory that we had. We only had about 16 K or so of memory. Sixteen thousand bytes. To be able to hold a reasonable amount of data to make this useful. So, you had to be very compact.

I was figuring out how to do that. I think Bob used some of my design for that. And for a lot of applications after that, I had to do the same things. I do that, obviously, today. I have to look at what's the data layout of how I'm doing it, just like programming has probably always been. And, you decide when you click here, what can you go to. If there are keystrokes, then you do a state diagram. So, it's always something like that.

I'm scribbling them down. I actually used paper, or sometimes do it on my application itself. We had to develop things, like invent the ruler, which you now take for granted. In the word processor, the thing with the tabs on it and all. The embedded ruler. Each of us had to invent that independently for our word processors.

This stuff just goes on and on and on. It's part of the craft. A lot of the stuff is just part of the craft. It's why some old timers will laugh at some of the youngsters who think that this is new. They think that some of the concepts are new, because they were able to do it for the first time, and they don't know people did in the sixties, and seventies, and eighties.

A lot of that wasn't saved because the computers don't continue to run. Old software doesn't always run on new computers. I've been lucky. VisiCalc was written for the IBM PC among other things. It was about a year or two, a couple of years after it first came out.

We copy protected it because that's what was done in those days. Copy protection. But, one of our employees kept an internal version of it, that was not copy protected, and kept it on one of his computers. When he left, took it with him.

He gave me that copy years later. He was into history and I had borrowed old stuff from him, and he said, "Hey, I have this old copy of VisiCalc!" Since it wasn't copy protected, I could actually use it on new machines years later.

Because the copy protection assumed certain hardware, it took advantage of that hardware to know whether it was a copy of the software or the original disk.

So, that version got put up and I have that up on my web site. Thousands and thousands of people downloaded it. They can run what was VisiCalc back in 1981. Well, apparently, Microsoft has used that as part of the test suite to see if new versions of Windows are compatible backwards. So, it's stayed compatible for many, many, many years. Which is kind of cool. But, that's highly unusual.

[musical interlude]

Rob: Yeah. Dan. Dan is amazing.

Scott: I mean don't you just feel smarter because you listened to him talk? I mean, he's just _mainlining_ information.

#### Charles Petzold

Rob: Yeah, absolutely. Something that's fascinated me as well is that… Well, I listened to the recording you did last week with Charles Petzold. 

Scott: Yeah, yeah. I talked to him a couple weeks ago, basically about that same things I asked Ward. What do we need to know?

Rob: He's amazing. This is my favorite part.

Scott: If you know how to take a C program and hand assemble it and all, are you a smarter programmer? Are you a better person? Are you…?

Charles: Umm. That I do not know. Sometimes, it goes the other way, though.

Certainly, my assembly language programming days, and my C programming days kind of overlapped. Once I got familiar with higher level structures in C, I started applying those to my assembly language programming.

I had a similar experience when I first started using the first version of BASIC for Windows and seeing how, in Visual Basic, you would design a window of controls. I started doing that kind of thing in my C Windows programming, where it wasn't so obvious.

So, I've had more the experience of going in the opposite direction; of applying high level concepts and structures in lower level languages. Whether any programmer these days has the time to start off with digital design, and then have a good foundation in assembly language, and then move up the scale from C to C++ to C#... That seems to me a little too much to ask of the education system and of the individual programmer.

Certainly, people don't seem to have the patience for that type of long learning. It was certainly different when you're encountering these things as they are introduced into the market. When you are back working when the only assembly language programming you could do at home was on the 8080 or the Z80. You encountered these things historically as they become wide spread in the market. By the time C# is introduced, you already have a couple of decades of backgrounds in all this.

I don't think you want to necessarily take a young programmer and force them to go through this entire history of building up things. For those of us who lived through it, it took twenty years to get me from 8080 assembly language to C#. [laughter] That's a long education!

Scott (to Rob): Ward likes to know the complete stack so that he can debug it. But also so that he knows which part he can rewrite his way. And basically invented the stack. He did everything that he needed to do in order to get VisiCalc to work, but he was working at a very, very low level, doing a lot of this stuff in assembly language.

In answering this question, Charles is acknowledging that there's just a whole lot of stuff to know. It's probably a bit much to learn it all.

This is something that many people can probably identify with. But what parts can we let go? As Rob and I are discussing, those who are unaware of the past are doomed to repeat it. And in that same way, those who are unaware of the lower levels of abstraction are doomed to rewrite it. That's what I asked Charles next. What things can the developer of today safely forget?

Charles: Nothing comes to mind off hand. Maybe you really do have to learn all this stuff? I don't know. There seems to be quite a few programmers who do just fine without it. Is that what's important? Well, it's important if you think of programming in a corporate sense, of delivering products to the market.

I hope that there is still a lot of programmers who have this interest in history. There's always been a retro-computing movement. I'm not sure that I personally would enjoy going back to coding for 16-bit Windows, but some people get a kick out of it.

[musical interlude]

Scott (to Rob): He's doing some great stuff. He's writing a wonderful book on Windows Phone 7. I think what makes his book special is that he's got that context. He's got twenty plus years of Windows. Gosh, almost 25-30 years of Windows.

Rob: I know, but you'll agree that he struggled a bit when he was answering that question, "What do we really need to know?"

Scott: Well, yeah, I mean he seemed to be at a bit of a loss.

Rob: I'll tell you what. One thing that struck me about the audio from Charles, and from Dan, and from Ward, is: these guys are really excited about what they're doing now. They don't really care much, or it doesn't seem like they have any nostalgic reverence for the past. They're as motivated now as they've ever been.

Scott: That's really what's surprised me. I expect that I'd be sitting down with three great uncle types. Maybe not grandfatherly -- we'll give them that respect. But you know, a slightly elder, great uncle type. And that they were going to tell me about how awesome it was in the past, and how much more the past influenced them. But, none of them seemed all that interested in dwelling on the stuff that they did before. I thought they were going to give me some wisdom as I climbed the mountain all the way up to the top. And they would just lay it on me. But honestly, they were excited about programming _today_. I'm not even sure, but I think Petzold may have been programming while I was talking to him.

Scott (back to interview with Charles): Well, you just finished a book on Windows Phone.

Charles: Right. Well, I'm still working on it. Almost as we speak, I'm actually coding while I'm going to be doing the interview. [chuckles]

Rob: It definitely sounded that way, because it took him a while to uh… when you asked him a question. And then he came out and said it! "I'm actually writing code right now." And I just love that. He's so passionate about the work he's doing. You could just tell he was wrapped up in it.

Scott: I mean, yeah. We were talking and I'm kind of hearing [muffled key stroke noises]. I'm like, "Are you multitasking?" I mean yeah, look at Dan. Dan's making this new application for the iPad. I mean, here, he'll tell you about it.

Dan: So many areas to fix. I mean, there's so many areas that are being computerized for many people for the first time. That can be helped by computers. That probably weren't as easy to do before because the hardware has advanced in certain ways, or the price has dropped substantially so that people can take advantage of it.

For example, my current product, Note Taker HD on the iPad, is for taking notes when handwriting and stuff like that on a computer. We've had that for years. I've been doing that for years.

I developed an application. I wasn't the only programmer on it, but it was a company that I cofounded, Slate Corporation back in the early 90's. We were doing a day timer for writing your daily notes and stuff; used the pen on a pen computer. The windows and things from PenPoint, GO Corporation's computers. But those were expensive and clunky.

Then the tablet PCs came out, and some other note taking applications have come up on that, like OneNote, which takes ink notes -- which has been very popular on those machines, but those machines haven't been that popular.

Finally, we have machines of sufficient size, like the iPad, for taking a reasonable amount of notes. That's now possible at a reasonable price for many people and it's becoming very popular to take notes on that. That's kind of cool, because the price has gotten down.

We still have the issue of the pens that work on the iPad aren't like the pens on, let's say the tablet PC. Which even then, had some issues with resolution. Really to do good handwriting, you need about 200 dots per inch resolution at about 200 points per second. We're not getting that on the iPad. We're getting about 60 points a second at, I guess, it's at 100 or so points per inch resolution. It feels like you have to write bigger.

What I do in my application, is I solve that by shrinking what you write down. Even though you're writing on what would have been a small piece of paper, I shrink it down and fit it on what would have been an 8.5" by 11" piece of paper with a fine pen.

They still have to solve some problems there, but it seems to be good for a lot of people. But it may not be good enough for enough people. As the hardware gets better, we'll be able to do that.

There are a whole lot of other applications that will be coming up that we've been trying for years to do, that as the computers get cheaper, we'll be able to do. For example, back in 1964, the public was exposed to something that was only in the laboratory at that point, which was video telephony, where you went to the World's Fair and you could use a picture phone. And wow!

Then you saw in the movie Space Odyssey of 2001, they showed that. And of course it was expensive to use it. They showed how expensive… It costs a few dollars to make a telephone call from the space station down to the ground.

Now, we have that with Skype, FaceTime, and stuff like that, and you don't even pay for the minutes! It runs on just about any netbook or laptop, and now a lot of cell phones.

Something that goes back to Dick Tracy's watch, with the real time video and stuff between individuals, has finally gotten cheap enough. Even though we could do it in the laboratory for the last fifty years.

#### Reflection

Rob: That is so cool. I'm literally going to go download that tonight, and I don't even care if it ends up being horrible. Dan Bricklin. Dan Bricklin wrote it.

Scott: So now we've got a whole show of us being fan boys of these guys, right? It's infectious.

Rob: Yeah, it's true. You're pulling me in!

Scott: See, now you want a Dan Bricklin trading card?

Rob: I'll gladly take the Charles and Dan trading cards. But I think Ward's got to be up to something fun and new for me to want one of his. What's he doing these days?

Scott: Ward appears to be doing things on the cheap, on purpose.

I was telling him about some of the Arduino and Netduino stuff. I was saying, "Oh man. You can do this for $25. And oh man, you can do this for $35." Each time I talked about these amazing things you could do for cheap, he would bring out something that was an order of magnitude cheaper.

He'd say, "Well sure. You could buy that chip for $15. But I got ten of these for a buck!"

He'd pull out a handful of chips and he'd say, "And I can get them all working together in some kind of biological system." He's putting together multiprocessing computers. Very, very highly specialized. And building these large sensor arrays with chips that cost him pennies. Pennies on the dollar.

Rob: It's so fascinating to me, again, that they're working this very current technology. I think each one of them has such an appreciation for what they have now because they know where they've come from.

I love Ward's point about going back into the stack. Going down as far as he needs to go, to then build back up again in his own way.

#### Learning Pascal

I asked my brother this question when I was talking to him the other night. I said, "How far back do you think someone needs to go into the stack?" In other words, how deep into the abstraction? What makes sense? Listen to the story he tells about his students learning Pascal.

[musical interlude]

Professor Conery: I remember a story when I was teaching programming languages. Teaching people about Pascal.

The common wisdom then was to keep it pretty abstract. Say, "This is a local variable. This is a global variable." Tell people the behavioral attributes of them.

One time, I remember telling a group of people, alright, I'm going to talk about implementation. I'm going to talk about stack frames. I'm going to talk about what happens when you call, it's going to push a frame. I could see the light bulbs going on all over the room.

Now this makes sense when we talk about a pointer from one frame into another and lifetimes of different things. And call by reference and all those other things that if you didn't have that understanding of the lower level, it was a little harder to explain. 

I guess that means, peel back at least one or two layers, if that makes sense. Find out what people need to know and then give them another layer or two to help put it in context.

That's a controversy in teaching computer architecture. There are people who believe strongly that you want to teach it bottom up. You want to teach the transistors and the semiconductors and work your way up from NAND gates and into registers and memories and stuff.

And there are people who say it the other way around. Let's start with the high level language stuff that people are familiar with and then work your way down to the lower levels.

The people who argue the former say people don't understand as well if you stick in the abstract levels. That you really need to have a firm grounding in something.

I don't know the thing here, I just don't. It's easier to get into the field. It's probably is easy for some people to skate by without putting too much effort into what's really going on. But if you're a serious professional, you'd definitely look into it.

Rob: Alright. Well, that was easy. You didn't even make fun of me. Not once.

Professor Conery: Oh, no. I mention you in class all the time.

I mention the story about how I discovered Ruby when there were some kids going off to the beach and you and I up in your lanai drinking beer and tapping at our laptops and having fun. [chuckles] I get a lot of mileage out of that one.

Rob: If you go down those levels of abstraction, it doesn't necessarily mean that you need to chase every single stack. If you use .NET, that's great.

One of the things that struck me when I was talking to my brother -- and I think Ward mentioned something about this to -- is, the tool sets that you begin to be able to use, as you go deeper down, the tool sets become more and more... The options sort of explode, if you know what I mean.

So, I asked my brother, if he's working on the problem of his thesis _today_, what tool would he use? And he rattled off about three or four languages.

Professor Conery: So if I need to write an application. I need to write a program. And this is going to be a one off kind of a thing, that I'm going to use myself. Believe it or not, I've gotten so disgusted with Quicken and other financial software. I must have tried like five different banking things and none of them worked for me.

I just said, screw it. Sat down and wrote my own Ruby program. I keep stuff in a database, and I've got this little Ruby program and I'm happy.

That's a tangent, but that's a good example of an application. It's a one off kind of a thing that I would do for myself. To answer your question... The abstractions in there, yeah, I guess I like the fact that the classes are easy to work with and you can go find libraries. The gems are amazing. You just go download gems and do what you want.

If it's some serious work that I need to do with a program that I'm worried about performance, then I don't use Ruby.

In our research group, we're working on a sequence alignment application. This is an application where it's got at least O(n^2) complexity. If you have sequences of _n_ letters, you can count on n^2 steps, unless you don't do it right. Biologists are dealing with sequences that are pretty long, so this is something you don't want to mess around with. You want to pay attention to performance and efficiency. So that's a C++ for me. I would just use C++ and write the code that I knew would be compiled most efficiently.

There's going to be people out there that'll laugh because C++, of course, isn't as efficient as C, or probably even FORTRAN or something like that. At some point, you've got to tell yourself [chuckles], alright! I can't mess around in these other languages because I'll just be going nuts managing memory and whatever. C++ is a pretty good compromise for me.

#### Final Thoughts

Scott: The thing that was pretty clear with each of these guys was that they would use whatever tool was awesome. They will go where the awesome is.

Sometimes the awesome is at a lower level. Like Ward, he's using small chips combined with low level languages to get high level systems built.

Or, in the instance of folks like Charles, he's using Silverlight and managed code, even though he's working on a small device.

They all have the context of history, but none of them seem to let history hold them back in their tool or language selection.

Rob: I have to say, coming into this, we were going to try and reflect.

Scott: We came in, the beginning of this show, with a focus on finding people who knew about the past, so that they might tell us about the future. What we found was three people from the past that are focused on the future. They're not worried about the past at all. I think we came in with our heads backwards.

Rob: It really makes me kind of happy listening to all of this. I guess that's not really the right word. It makes me hopeful. When I started programming, gosh, what, twenty years ago now, I didn't know that there'd really be much of a future. Everyone in programming back then seemed really young to me. I just didn't think, "Well, this is something I can do as I grow older in years and my family grows up and so on." I always just thought I'd have to do something else.

You see what these guys are doing, and, not only that, they're working on really current stuff and they're super fired up. That's kind of neat!

Scott: There's a reason there not to become a manager.

Rob: [chuckles]

Scott: I always hear about people who can't keep up because there's so much. The more and more layers of abstraction that come in, the more and more people get overwhelmed and they give up and become a manager. (With all due respect to managers that are listening.)

What I think is cool about these guys is that they know what to throw out and they know what not to throw out. They know what parts they can't know in the spec, and they choose to ignore them. They can overwrite those bytes in their head with new information.

I doubt that Dan could write VisiCalc today. He's overwritten those bytes in his head with new information on how to write a good iPad application. Ward has chosen to focus on some of that low level stuff, perhaps not knowing about some higher level things.

They're all Swiss Army knives. Maybe it's okay to not be too much of a specialist. Stay excited. And if you're not excited, find something else and be excited about that.

Rob: I'm ordering my geek trading cards today. I got Petzold, Bricklin, Ward. They're on order.

Scott: You get Felsenstein?

Rob: I have Felsenstein. [chuckles]

Scott: It's not a complete collection without Felsenstein.

#### Outro

Rob: Once again, I'd like to thank the folks at Twilio for sponsoring this episode. Twilio's the easiest way to add SMS or voice calls to your application. Visit twilio.com to get started for free. In addition, I'd like to thank the folks at Umbraco. Great open source CMS project. These people keep this show on the air by helping us with bandwidth costs and so on. Do me a favor. Go check out their sites. They've been kind enough to sponsor the show you're listening to.

Once again, this is Rob Conery.

Scott: And this is Scott Hanselman.

Rob: This has been episode six of This Developer's Life. Thank you so much for listening.
