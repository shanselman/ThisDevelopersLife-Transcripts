#Episode 2.0.1 - Criticism
=========================
##Featuring
Rob Conery
Scott Hanselman
Ayende Rahien (Oren)
G. Andrew Duthie (GAD)
Boris Pavlovic

##Introduction
Oren: Whenever a new episode of This Developer's Life is published I listen to it immediately. This was not the case with the last one. It just made me angry. I gave up a few minutes before its end. A few days later I saw a tweet from a guy stating that although not a fan of the podcast, he loved the episode. I used his tweet and worked at his words and said "Although a big fan, I think the last episode was crap."

Scott: Ouch. "The mental weight of this is literally crashing." That's not just regular criticism, that's...that's you're enjoying yourself at that point.

Oren: That quote gave me a migraine. We had to stop and I had to go and have a drink and, you know, just rest my eyes.

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

Scott: So, if every single application out there, or the vast vast vast majority of them, are failing, and they are using *your* library to do it...

Oh snap, good one Scott!


[musical interlude]

Oren: That is actually an interesting question. The problem with select(n+1) isn't because of nHibernate or anythng of this sort. Second .... As a typical example, it took me ... I was watching the LightSwitch lauch video, and during the launch video just from the blowee and the screenshot they saw 640x480 video I was able to detect that they had a select(n+1) problem inside the architecture. It's basically an issue of modelling your data correctly. 

Scott: Damn, that was a good answer.

Oren: It's not an issue about this ORM or that ORM. Just to give you some idea... Uncle Bob. You know him?

Scott: Yes, Uncle Bob Martin.

Oren: OK, yeah. So, he wrote clean code. In one of his examples about "How do I clean code?", he showed an example of how to a select(n+1). Literally that. OK, so we are talking about someone who is very, very good, in a book about best practices, and he shows, accidentally presumably, he shows an example of how to do a select(n+1). In RavenDB...

Scott: I should jump in here. For those who are not aware, RavenDB is a document database, kind of like CouchDB if you are familiar with that, written entirely in .NET by Ayende 'cause he wanted one. 

Oren: ...specifically I've decided that...so...here's the problem. We said "Can I make people fall into the put of success?" And with a lot of those libraries, I don't control them. I mean, trying to add something liek that to nHbernate is actually fairly easy and I have blog posts detailing how to do that. The problem is, that in order for you to be able to do that, you are probably going to have to break people's software. With RavenDB, because it is new, I decided to make it safe by default from the get-go. So with Raven DB, if you actually try to do stuff like that, you know, you have some leeway, but if you've passed its default limit, it's actually going to tell you "Look, you're making too many queries to that database. This probably means that you are doing it wrong. Here are the options for fixing that. If you are absolutely convinced that this is the right thing to do, here is how you can disable this warning."

Scott: Did you create the Profiler tool for nHibernate as a way to get around this issue of all of these people using the product incorrectly?

Oren: Yes. It is one of those. The actual reason I created the profile was that I was trying to...I was at a client's and I was getting really, really sick of trolling through the logs, getting the SQL statement, pushing that through SQL beautify and then pushing that into SQL Management Studio so that I could actually see what's going on. And at some point I already know what's going on, but I have to explain it to the people with be so that they will be able to follow the logic next time they have to do something like that. And at one point I literally decided "You know what? This is just annnoying; I bet I could automate this process.  So I was actualyl sitting in a room with a pint of Guinness and trying to do something and trying to see if I could make this into a workable thing. I started in October of 2008 and on of the first of January 2009 we had the beta release. And the really fun part is that in the second of January 2009 we had the first sale.  

Scott: Ayende can easily bring tears to your eyes if he locks onto your codebase and he decides to start criticizing. But, he can also bring tears of joy with the tools that he creates. I've used his profilers before and I have to tell you, they are awesome and have saved me so much time....helped me from making some pretty dumb mistakes. For a guy whose bite is largely bigger than his bark, Ayende is quite helpful

[musical interlude]

Scott: We have an expression in English that is: "You will catch more flies with honey than you will with vinegar."

Oren: Mmm hmm.

Scott: Do you have any concern that you may be turning off new programmers with a reputation of being scary?

Oren: Uh, I am not sure that I am following the logic. 

Scott: Everyone has their public face. And, I work consciously at being a nice person and avoiding too much conflict, what I perceive as the wrong kind of conflict, for fear that I might make the programming world, the programming community, less accessible to new people. I want newbies to feel welcome and encouraged. Just as you're not supposed to hit a child, you maybe shouldn't hit an adult. By cultivating a critical persona, do you think you might make people afraid to use your product?

Oren: Uh, no. No. I actually have several problems with that statement. The first of them is the assumption of responsibilty for my actions to the whole programming community. The seocnd problem is that there is another saying "If you can't stand the heat get out of the kitchen." And I look at that to the point where, OK, you have some code out there. Either it's going to be open source, it could be a closed source project. It is my responsibility to tell the truth about this piece of code as it stands. It would be dishonest to try to cover it up. You also have to understand the cultural differences. For the most part I say what I think. I know that in the States you tend to be much much more heavy sugar-coated. I'm sorry, I just don't follow that.  I literally have to ask for translation of some corporate-speak stuff. Do you have any idea how hard this this? "OK, sorry, I get that you are trying to say something here, that you aren't saying with real words. Can you just tell mw what you mean?" And you keep trying to avoid saying that directly. It's really annoying. 


Scott: So, Americans, being adverse to being straight with people, for fear that they might hurt their feelings, is annoying. So, you're saying that because your culture is Israeli, you have a culture of both openness but also you enjoy arguing and you enjoy a critical eye and your'e not too worried about hurting people's feelings because you are telling the truth.  "The code sucks, you wrote the code, I hope you get better at writing code."

Oren: I don't think that I actually used the term "sucks". Not for open source projects

Scott: [laughs] Well, you *have* said on your blog: "Hell. Pure hell." You've said, you called it "The sins"... 

Oren: Oh yeah, I like that. "The wages of sin."

Scott: The wages of sin. You know, let's say, that as an American reading your code, it's excellent criticism. It's almost like, in America our most famous film critic is named Robert Ebert, and he is an extremely kind and well-thought of critic. But sometimes when he sees a movie that is just so horrifically bad, he starts to criticize it, and he gets into the critcism. He kind of wallows in it, like a pig in slop, and begins to have a lot of fun with the criticism. And when a movie is so horribly awful. You've had some criticism where you've said "I would hide this code in a distant, distant corner of my codebase."  And, "Are you kdiding me?"  Here's an example: "The mental weight of this is literally crashing." That's not just regular criticism, that's...that's you're enjoying yourself at that point. 

Oren: That code gave me a migraine. I'm serious, OK. We had to stop, and I had to go and have a drink, you know, and just rest my eyes, becasue trying to follow the code was just so complicated.    

[musical interlude]


Scott: There was a great movie a while back with Adam Sandler, he's the guy that did the movie about the Israeli guy, 

Oren: Zohan.

Scott: Zohan, yes. So he had another one that was called, I think it was called, "Happy Gilmour". And he was in a trivia contest, and he was doing, like, "Jeopardy". And he answered the question, and the guy stared at him and said "I am stupider having heard your answer."  Like, just sitting here, you have literally made me a stupider person because you made me listen to that crap. 

Oren: [laughing] Yeah. I use something similar when I am watching reality TV: "I can literally feel my IQ slipping down."

Scott: [laughing] So there is fun in criticism, though.  When does it go from being criticism to tearing something down because it is just so bad? And do you every catch yourself, and you say "I am writing this blog post and I am being too mean and I neeed to back off?"


Oren: Yeah. Usually when I am reviewing Microsoft Project.

Scott: [laughing]

Oren: That is actually an accurate statement here. There are times when I actually see something and I make allowances for open source projects, mostly because they are open source and no one actually is paid to do them. But, if you go to LightSwitch, for example...
 

Scott: I am going to jump in quickly one more time. If you don't know what LightSwitch is, it's a new offering from Microsoft that essentially is a wizard-driven forms over data generating application. So if you have a database, you can use LightSwitch to work with it. It'll actually generate a form-based application on the web, or just basically on the desktop. It was met with more than a little head-scratching from the development community, especially Oren, who decided to review it and found a few issues with it.

Oren: So with LightSwitch I was *very* annoyed. It literally took me 2 hours to write 5 blog posts about different aspects of why this is wrong.  Like, not just "There is a bug when you are doing something", but "You literally ignored basic truths about how to make software".  Like the fallacies of distributed computing. And those sorts of things really, really annoy me. When you have an expectation of one thing, and you get something completely different. I had a similar reaction walking into multiple teams, and the team kept sending me crap.  So at that point I sat down and wrote a very, very angry email pointing out that 6 breaking changes, after I have specifically requested "Don't touch this piece of code", is somewhat ridiculous. And then I just let it sit for a few days until I was calm enough to read it without...you know...OK, let's tone it down just a bit, we don't have to tell them that they are morally bankrupt or something like that 

Scott: [laughing] "Intellectually dishonest".

Oren: Yeah, I think that honestly that particular team was just lazy. It was really annoying. I don't like to be the dumbsling team from somewhere. Especially when it's under active development, and the only contractor you can get for them is 

Oren: I'm actually trying very hard not to go to the "morally bankrupt" level of criticism. I think that I can strongly disagree with someone about their professional behavior. "So I think that you have made a serious mistake in designing this piece of code", like that. So I'm able to disagree about that, without carrying that disagreement in a personal level. At least I hope I am able to do that. And I think that is the most important aspect of being able to criticize software without actually taking that criticism to a personal level.     


Scott: mmm. How important do you think it is, when criticizing, to balance the criticizm with the correctness? Like you had a post on analyzing data access behavior, and you have a tendency to show huge amounts of...like...when you find bad code you paste it in, you say "Look at this! That is the sound of a database administrator dying."  How important is it to balance that with "And here's how it should have been done."? Because I see a lot of criticism, but I don't see a lot of "This is how it should have been done."

Oren: I have 4700 posts. Out of them, roughly 50% are "This is how it should be done." Another issue is that it is actually very hard to give critical advice. Right now we are writing a sample applications for RavenDB, another one. And the guy is writing that and actually sat down and started writing... And I said "OK, I don't want anything extraenous here, I want to make it simple." And he asked me "Why? This is how I build these sorts of things?" And I told him "Yes, but that distracts people from the purpose of this sample application."  And that is not a decision I would make if we were building a bigger application, for example. And that will be the decision I will be making if we are making a still bigger application that is distributed (we have services, we have web apps, those sorts of things). So it is actually very, very hard to try to give advice on...

Scott: Have you released a sample application, like the "Northwind for nHibernate"? Like, "here is how to do a correct application"? Like a complete File --> New Project, like, the whole thing?              

Oren: The problem is that you have to make too many assumptions. For example, how do you handle things like services? Because here is the problem:  when we are talking about "ok, let's do a rapid application", well, there isn't that much for nHibernate. Let's say we are talking about an MVC application. OK, so where do you open and close the session? Done. That's literally 15-20 lines of code tops. 


Scott: But isn't that 15-20 lines of code that bothers you, that you are currently in the process of getting rid of? 

Oren: Absolutely not. What bothers me is different architectural decisions. For example I see a lot of people trying to hide that they are using nHibernate. 

Scott: I should make it clear here that what Oren is talking about is the abstraction of nHibernate, which is an ORM (data access tool) that is popular in the Microsoft .NET arena. He's not talking about being ashamed of it. Although if you were ashamed of using it, I wouldn't blame you. Oh, was that critical of me? 

Oren: And it invariably ends in pain, because they don't get anything from that. They hide nHibernate features, then they actually misuse their own API and get some horrible results. It used to be the case that I would come into a shop and my work would be to fix up their interpretation of nHibernate.  Now my work is, OK, let's look at why I cannot help you.   



stopped at [34:06]








