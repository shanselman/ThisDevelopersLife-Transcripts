#Episode 2.0.1 - Criticism
=========================
##Featuring
Rob Conery
Scott Hanselman
Ayende Rahien (Oren)
G. Andrew Duthie (GAD)
Boris Pavlovic

##Introduction
Rob: Whenever a new episode of This Developer's Life is published I listen to it immediately. This was not the case with the last one. It just made me angry. I gave up a few minutes before its end. A few days later I saw a tweet from a guy stating that although not a fan of the podcast, he loved the episode. I used his tweet and worked at his words and said "Although a big fan, I think the last episode was crap."

Scott: Ouch. The mental weight of this is literally crashing. That's not just regular criticism, that's...that's you're enjoying yourself at that point.

Rob: That quote gave me a migraine. We had to stop and I had to go and have a drink and, you know, just rest my eyes.

Scott: [laughing]

[Musical Interlude]

Scott: They say a man is what he does. So if what you do is crap, what does that say about you? Do you suck? No? Are you sure? Programmers are wound pretty tight already. We take a great deal of pride in the code we write and the work that we do. But if the work that you do gets criticized, are you not good at your job?

Guest: I started feeling really good about it. You know, he's complimenting me, I'm feeling good about how I did and all of that, and then he follows up with "but it's not you". 

Scott: Criticism is the topic of today's This Developer's Life. Stories of criticism, folks who criticize, and folks who've been criticized. But most importantly, what did they decide to do about it? Will you let criticism change your behavior? Will you suck? Or will you suck less? This week on This Developer's Life.

[Musical Interlude]

This Developer's Life is brought to you by CodeRush for Visual Studio. We appreciate their support. With consume-first declaration, powerful templates, smart selection tools, intelligent code analysis, innovative navigation and an unrivalled collection of visual refactorings all working together, your development productivity will increase dramatically. Get CodeRush. You'll be glad you did. Check them out at http://devexpress.com/coderush.

##Ayende Rahien

Scott: Just the name Ayende Rahien strikes fear in the hearts of programmers everywhere. If this guy gets you in his sights, he will reduce you to ash. It's one thing to criticize people without basis. If you actually know what you are talking about, and you have no problem telling people your opinion, well, you're a double-threat. Ayende talks big, but he can back it up, and we all learn.

Scott: So Oren, I've been reading your blog lately, and there's been a couple of times where I've noticed you picking a project and basically ripping it open.

Oren: [snickers]

Scott: Like, it's recently that you took some CodePlex project, and you knid of...you weren't mean... but you didn't go out of your way to be nice. You know, it was basically like, "Hey I'm looking at this project. I don't know this guy, I don't know these people, and here's 20 reasons why it's wrong."

Oren: Yeah. The actual story behind this set of posts is pretty interesting. I was teaching a class about nHibernate, and it was my advanced class, so part of the time we spend talking about "OK, here are the features" and part of the time we are actually talking about "OK, let's take a look at, let's review some code and let's see the what are the things that are bad in it." I basically asked all of the people in the class "OK, Give me some names of some open source projects using nHibernate and we can review them live, and that will give you the tools to be able to go about your application and figure out what you're doing wrong. The interesting piece is that one of the criticisms that was pointed at me was that one of the code bases that I was reviewing was actually written by a student. So university part of a school project.  I wouldn't have believed that, because I've seen code exactly like that in many, many places in ... application, in big companies and small companies, anything from the most on-the-edge start-up, to Fortune 500 companies that testing by rolling out once every 2 years. Once I realized that this is literally an open source project that shows, literally shows, how many projects are actually being built, I decided that this would be a good opportunity to literally sit down and break down all of the things that I didn't like about all of those projects, because if someone comes to me for a code review and I spend 2 days just going over the things that are wrong in the application, but I cannot publish that so that other people can benefit from that. When you have an open source project, well, you can do that. Actually, I think I was very careful about saying what I don't like in the code, versus saying what I don't like about the people who wrote it.      

[ominous music]


Scott: I get a picture in mind of what a person looks like on Twitter or their blog. I read their voice and I imagine that they are some skinny, pasty, programmer in his mom's basement, and now they are criticizing my code.  That's not the case with Ayende. Not only does he talk big, he is big.  He was a commander in an Iraeli jail. He's all of 6'5", 250... huge, in-your-face. Whether your reading his blog, or he's towering over you, you'll feel the weight of his words and what he has to say. It's intimidating, to say the least.    


Oren: And there are problems with the code. And I am looking at those sorts of things and saying "OK, this is wrong."

Scott: How do you separate the person from the code? I mean, I could imagine myself as a young person reading your blog, and if I saw that you decided to review my application, I, maybe I would cry. 

Oren: [laughing] OK, Scott, if I tell you that...OK, here's a very simple example. If I tell you that a demo that you do is unrealistic, and it's going to misstate people, that is a professional criticism on a piece of code that you are doing. If I tell you that you're stupid, that is a personal criticism, and probably an insult. That is how I make the distinction... talking about a piece of code, talking about an architectural decision, and talking about the people behind that decision.         


Scott: But aren't we extensions of our code? We are extensions of our actions. I mean, people always say that talk is cheap, show me the code. And we also have the saying that "Actions speak louder than words." If a person does a stupid thing, how do you separate the person from the thing?

Oren: [huffs] Very easily. Let me ask you this. If I sat you down and made you draw a picture of a house (like using pen and paper and crayons or whatever), then I took that piece of paper and I send it to the Gughenheim Museum for it to be criticized. Presumedly, since I haven't seen you draw, they would laugh it out of the museum. Is this a correct assessment?

Scott: [laughing] It's possible that it may.

Oren: OK, obviously they might decide that this is the next thing in mdern art, but we leave this aside. Now, would you be offended that your drawing isn't considered to be equivalent to Van Gogh?  

Scott: No, because I don't want to be a professional artist and get paid for it. But, if I was a starving artist, and truly believe in my heart-of-hearts that I was good, I would be sad, because it's like a person who wishes that they were a great basketball player, and they try out and they try out, and they can't get it, and the caoch says "You know, son, it's not gonna happen for you. You need to pick a new thing. "     

Oren: Yeah. You're 5 foot 10, no 5 foot 1, so it's not going to happen. 

Scott: [laughing]

Oren: The main thing is that I am focusing on a single aspect, in those code reviews, I am focusing on a single aspect in the application.  In the reviews that I am talking about, I was focusing on data access. But the application isn't data access. It's not just that. Think about it. In just about 90% of the cases, most of the errors that they find are related to a SQL statement being generated from the view. So, this is incredibly common. One of the reasons this is happending is that when you are working on the view, you are working on the system architecture. When you are working on that level you tend to be focused on a single item at a time. So when I am working on the user interface of the system, what I am actually going to do is to try to create a good UI, try to put down corners? somewhere, and all of these sort of things. The last thing on my mind, most of the time, is "OK, does this piece of HTML general a SQL statement?"   You see where I am going here?

Scott: [agreeing] Mmhm.

Oren: So, that is one of the problems when you start talking about... OK, so I am criticinzg this and I might have criticized it and said this is the wrong way of doing something. But I don't consider that to be the whole thing. Just to give you some idea, in all of my applications, I put circuit breakers inside of the application. So when I am doing something stupid, (not if, but when I am doing something stupid), the system will detect that and warn me. I actually have a good blog post, it is called "Shocking Rob Conery". And I think it was in 2007 I had an argument with Rob about using a ?. And, in that blog post, I actually show a message that says something like "Only 30 queries are allowed for this web request, but 743 queries were executed. Please fix this."       

Oren: And this is a piece of code that I wrote in a system that I control thoughout. And one of the reasons that I don't feel any problems in saying that something is wrong is that, well, it IS wrong, it is going to be wrong. I don't care who is writing it. Because if I, who is doing data access, views, basically every week, and can't look at a piece of a code without actually considering a modification because I've been living and breathing that stuff for years, can make those sorts of mistakes, then anyone will.

Scott: [agreeing] Mmhm.


[musical interlude]

Oren: It got to the point that in one of my classes, that I say " OK, what is the next application?". And I look at the code and it was complicated and it really annoyed me, you know? It's like the 6th application that we are reviewing today. So I told them, "OK, let's just find select(n+1) and then we just get out of here. I don't care to do a review of this code". And they started laughing. And I said, "What's so funny?". And they said "You just said let's find a problem. We don't know if there is a problem." And then I told them "Well, you know what's happened? Every single application that I saw had at least one select(n+1) problem, down to the simplest, most trivial application possible.  

Scott: So, if every single application out there, or the vast vast majority of them, are failing, and they are using your library to do it...

Oh snap, good one Scott!


[musical interlude]

stopped at [14:58]










