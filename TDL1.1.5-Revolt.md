### Revolt

(Voice-over) Rob: On January 25th of this year, 2011, the people of Egypt decided they'd had enough. They assembled throughout the country, they came in force to Tahrir Square. And approximately 3 weeks later, Egypt's president of over 30 years, left office. 

(Voice-over) Rob: This was a different kind of revolution. It didn't center around a singular enigmatic, separatist leader. Or a significant historical event. It didn't have the energy of a religious revolt. It wasn't a coup, the military didn't involve itself necessarily until Egypt's president, Hosni Mubarak, stepped down from power.

(Voice-over) Rob: What happens in Egypt is what happens when people can freely communicate, without the confines of government control. They know where to show up, when, what's happening, what the government might be responding with, and then how to get around that response. They communicated using the tools that you and I would: texting messages on their cell phones, using Twitter, updates on Facebook, posting to their blog, and other social media. 

(Voice-over) Rob: Setting up for this episode, I watched a lot of video of Tahrir Square, and what's striking is how many people have their cell phones out. Their video cameras, they're texting, they are taking pictures, they're updating their Facebook. They're sending tweets on Twitter, they are letting each other and the world know what's happening to them.

[Musical interlude]

(Voice-over) Rob: It's an interesting time to be a developer, especially in Egypt. That's the subject of this week's show; looking at the Egyptian Revolution through the eyes of an Egyptian developer. Scott Hanselman catches up with a developer he met when he as in Cairo last year. Then it led to this week's topic: Revolt.

Excerpt televised statement by Omar Suleiman: "My fellow citizens, of these hard circumstances our country is experiencing, President Mohamed Hosni Mubarak has decided to waive the office of the President of the Republic and instructed the supreme council of the armed forces to run the affairs of the country."

[Brief exchange between Scott and unidentified female voice]
Scott: Um, I'm looking at a picture of you on Facebook in front of a Tank!

Unknown: So uh, oh yes, yes, uh good citizens I had to take food to. And I had to get that food to my [can not understand @2:45]

[Musical interlude]

(Voice-over) Scott: This Developer's life is brought to you by CodeRush for Visual Studio. We appreciate their support. With consume-first declaration, powerful templates, smart selection tools, intelligent code analysis, innovative navigation and an unrivaled collection of visual refactorings all working together, your development productivity will increase dramatically. Get CodeRush, you'll be glad you did. Check them out at [devexpress.com/coderush](http://devexpress.com/coderush).

[Musical interlude]

#### Introduction

(Voice-over) Scott: I came back from Egypt with pictures and pictures and pictures of my friends: my friends in front of laptops, my friends in front of PowerPoints, my friends in front of code. Now a year later, I have pictures of them in front of tanks.

(Voice-over) Scott: Remon Zakaria, a community organizer, a big man on campus; He was .NET for me while I was in Cairo. People orbited him, and he orbited people. In front of a tank. Ahmed Remy, a gentle giant, incredibly kind, incredibly thoughtful, always focused on the next big thing. Reem Ahmed, slight, tiny little thing, holding a giant flag of Egypt. In front of a tank. It's her Facebook picture now, a new Facebook picture to go with a new country.

[Musical Interlude]

(Voice-over) Scott: So many stories from so many friends. I wish we could include all of them.

#### Act 1

Remon Zakaria: [Laughs] It's a different experience not to be able to go online and, you know, see the news, check your email for every now and then. It's different, to be honest.

(Voice-over) Scott: This is Remon Zakaria.

Scott: How did you get through that? I mean what did you... did you... did you develop new systems and have people - you couldn't text each other. You - did you have phone, what we call phone trees?

Remon: Actually you know what? No, we did not have that but I was just working, me and another guy, we were working on, you know torrents, right?

Scott: Uh-huh

Remon: Yeah, it's like peer, peer-to-peer... you know, network. So what we did is, you know the torrents, we were working on the torrents idea. But I wanted to make it sort of like peer-to-peer phone calls, peer-to-peer Internet. So we wanted to, to have this very small application that you can deploy on all your phones. So you work with .NET, Java, all the net devices that we have. That's why I was working with a Java developer, he's of [? @6:08] from his high school. 

Remon: And you know it's very simple, so when somebody starts it looks around, it scans all the IP range that he is in. And, if he found anyone else around him, you know they get connected and synchronize their messages between each of theirs. So when whenever anyone writes any message, the whole network gets, gets it. So it's sort of like a mini-Twitter, if we can say so. Because the phones were working on the GPRS, but they working internally. So you, you could have accessed them, the mains and networks and IPs inside of Egypt, but you could not go outside.

Scott: Ahhh

Remon: Exactly. Yes, so they were like blocking the main gateway of whole Egypt. But still you can access your peers. So what I wanted to do is I scan all of my peers, and, and the IP range above it. You know, just one IP range above it, and find everyone else who is using the same application. And all of us sync, just synchronizes all of the messages that we have. So you get like tons of messages, like what's happening exactly now. And, like the real ones, because you know the news has not been very... unbiased, if we can say that.

Scott: Mm-hmm

Remon: They were like extremely - "Oh, everything is good, blah blah blah" or just "Oh, everything is crisis, there is a crisis, there is something, you know people dying like ten times, you know ten persons a minute" or something like that. From Jazeera, there were like two networks, the national TV and Jazeera. You know, there is a network [? @7:53] that regularly had Egyptions so they were very happy that we were having revolution. Like, "Ok, the network is down" and so on.

Remon: So the networks, the networks was not very robust. So we wanted to do this application to, you know, share the messages between us. There was no SMS, there was no Internet, there was just GPRS connection and [? @8:16] and that's it.

[Musical interlude]

Remon: We were almost finished, but then they got, the President, the former president, got this speech that he will die in Egypt and he doesn't want anyone else to... You know "I'm an old man, please, you know, take pity on me." and stuff like that. "I'll just finish my year, my round, and that's it." and they got the Internet back on the second day. It was on Wednesday, it was on Tuesday night, and they got the Internet back on Wednesday, so we didn't really need it.

[Interlude of protest sounds]

(Voice-over) Scott: This is such a classic software engineering thing to do. I mean, they've cut you off from the Internet, your country is in chaos, how can you solve this problem with software? In the old days it would have been ham radio. All the ham radio people would have gotten together and they would have fixed this thing. But today we've got software.

(Voice-over) Scott: They've shut you off, and you're all alone on your own subnet. Except, the subnet isn't your organization, it's your country. So they build this application that scans up a couple of levels from their subnet and says "Is there anyone in Egypt that's running this application?" They build a big, peer-to-peer IRC thing in order to move the revolution forward. It's incredibly clever, and I love it, because it's exactly what I would have done.

Remon: If something happened like this again, I think this application would be handy. This would be important, oh maybe we can sell this to Libya or something, this would be good.

Scott: [laughs]

Remon: They need it, the guy is crazy over there, he is even worse than ours.

Scott: That's really interesting, so there was a problem, the entire Internet was shut down and you guys needed to decide "We need to solve this problem." And you're engineers, so of course you want to solve this problem in software. 

Remon: In softwares, exactly.

Scott: Oh clearly, clearly, "Oh, the Internet is shut off? Our country is falling apart? We're kicking the President out? Well, we're all on the same subnet, let's make a chat program." That's amazing.

Remon: Exactly. And it's not a simple chat program, it's a smart one. It goes online, it goes through the subnet, scans all the ports, and all the IPs. Just a specific range of random ports, so no one can block it. So port like 10, 19, 48 - just random, random set of ports. And when you go in, you connect, you synchronize your post messages. So if you talk to Person A, and I talk to Person B, when I and you synchronize ourselves, we get the whole messages of the four of us.

Scott: Wow, that's amazing!

Remon: It was, it was interesting. You know, I don't know the saying in English, but when the need is, when you need something, this is when you can invent it. This is the main time that you can invent this thing that you need.

Scott: Right, we say "necessity is the mother of invention."

Remon: Exactly, "necessity is the mother of invention." That's the one. 

Scott: Wow, how has it been doing business while this is happening? I mean you, you still want to, you still want to do work. I mean you're a business, you're ready to write software. 

Remon: Exactly, yeah, actually it was a bit strange, but the Internet went down on Friday, that's January 28th. And we just learned about it, like really early in the morning. So I wanted to, I drove to the company and I wanted to check if we could do anything before we go flying but really couldn't do anything. 

Scott: Mm-hmm

Remon: Once I went there, everything was already down, and also the mobile phones at the same time.

Scott: Hmm

Remon: So yeah, we actually at this time, we had like three deliveries. Of course we didn't make any of them. But luckily we were working ok the week before, so customers were like... a bit, you know, annoyed, and they were a bit freaked out, but most of them went back again after the Internet came back. Most of them went back again to work with us. We actually gained some new customers as well. That was very good.

Scott: Really? So, I mean, did you lose more or gain more? I mean, when I would think that most western countries would want to run in fear. "Oh, your country is in crisis, I don't want to do business with you now."

Remon: Well, actually, that did happen, you know a lot. But most, most of them like... so, we had customers that were terminating business like "we're stopping now", but some customers like finished, finished the projects, like we were having deliveries this week that we went down. And, like we finished the finished, the delivery has been finished anyway, but they didn't want to renew the contract, like having more projects.

Remon: So I went to the speech, the support Egypt speech. We did work good, we were of a benefit to you, and I'm living in Egypt now, and I know it's safe, and we need you to go back and help us. You know, so if I was helping your business for a couple of years, and you know that I'm good, and we had just such a crisis that ended well. We have, we kicked off our president, so you know that, how persistent and stubborn the Egyptian are now, which is good. And you need to go back to working with us. And actually most of them, the one that had projects, they came back, and we won new customers that would actually, the past, this week, we got like three new customers, which is very good.

[Musical interlude]

Remon: The people actually, when they start outsourcing, and working with off-shore companies they have even little sense of adventure. But, not very big one, but at least they can risk that "Oh, we're going to send our source codes all over the sea" and "who knows, we didn't see those people." So what they did, they actually did take the risk working with us, and they know it's fine. So when we told them again: "It's fine, come on, come over back and keep working because we need, we really need your business now." Because of our economy, tourism, and everything. They actually went back, and some of them were maximizing their businesses.

Remon: We're still, we're still not stable, like all of the companies here, whether they are working internally or externally. I am having a friend who works, who builds software for tourism companies. And you can imagine the crisis that he is in now. Like there is no tourism action in Egypt now at all, almost. Now people are just, you know, we just were talking the past two weeks like a couple thousands are coming back and people are coming, still coming [unintelligible @15:56] places like this. But still they need some time to go back and start looking for software again, you know, for the companies. So we've been hit, but not the worst.

Remon: You can come here, you can try working with us. People now are very, very persistent, and they have this amazing, amazing power that they want to prove themselves and start over again. I'm not meaning "start over" by, you know, just because of the revolution, but start over because all of us has discovered a "new us" inside us. You know, if this is 'Englishly' correct...

Scott: Mm-hmm

Remon: We have discovered, rediscovered ourselves again, and everyone of us now, like, they were regretting that they spent the past years - 30 years - in fear and did not say anything. Now they... we see, and we know that we can do something, and we can do huge things with the mass, the mass amazing size of coverage that we have about what we did in Egypt. We are extremely proud now, and want to prove to people that we want to do something. We want to show you that we are very, very, very good. And this is new Egypt now, you need to work with the new Egyptians.

[Muscial interlude]

Rob: For most people, a revolution is something they watch from a TV screen. It happens to people, in a land far away, who you probably don't have much in common with. Remon is just like me, he is just like you. What if there was a central figure to this revolution who wasn't a religious leader, wasn't a great inspirational speaker, was a [not understood @17:59], a marketing executive from Google. These people are just like us, they are us.

[Musical interlude]

#### Act 2

Remon: I was talking with Stephen [not understood @18:13], and he used to say: "Hey, you're second world now, because you have a Starbucks" so maybe, maybe that's right for the people who likes a Starbucks.

Scott: [Laughs]

Remon: I'm ok with anything [unitellible @18:24] you know, gets our ranking up. So whatever you want to send in here, send it please.

[Laughter]

Scott: Yeah [Laughs], that sounds like Stephen.

Remon: Oh yeah, you know but he got married, right?

Scott: Yeah, I saw on Facebook, I thought that was fantastic. That's funny, I always learn about important things like that from Facebook and Twitter.

Remon: [Laughs] Yeah, you're a big country my friend.

Scott: Yeah, yeah. It was, it was interesting also to hear that Facebook played a bigger part, plays a bigger part in Egypt and in social media than Twitter does. That Twitter is where "the elites" hang out, but Facebook is where a huge, huge portion of the country stays. Like -

Remon: True, true....

Scott: That's where it all happens. So they were saying that they would make the update on Twitter, but they would feed it...

Remon: ...To, to Facebook

Scott: ...To Facebook

Remon: Yes, yes, and actually, you know that national democratic party that, the ruling party that used to be here...

Scott: Mm-hmm

Remon: ... They had this committee, of people, that goes on Facebook and tried to mislead people. So they go with different names and try to say some comments "Oh, Egypt is still good, the President is fine, blah blah blah" and they do not say directly, but they say in twisted way. And this was extremely, extremely dangerous, because people would like, people got confused. Lots, lots of people got confused.

Scott: Hmm

Remon: Yeah, and this is why Twitter was even better because they didn't knew that Twitter exists. Or just they weren't being dis-influential because you're on Twitter, you're following people that you really like what they are thinking, and you know them most likely. But then Facebook like, you know, you can add tons of friends that, just people requesting to add you "Oh, maybe I saw him or her, so I'll just accept it." Twitter is way, way, way different. And this is why they were were being pushed outside of Twitter. And the thing, the very very good thing is Twitter really, really helped in Jan 25th, you know the day Jan 25th, not the revolution, because you know the... I don't know what the name, the "police"? The ones who used to fight the rights and stuff like that...

Scott: Mm-hmm

Remon: They were waiting for the people to who were talking on Facebook, so they were saying "Oh, we'll meet in front of the university" - so they were, they were waiting for them over there. So you see when someone goes in with his mobile and he sees this people all over the place, the police, he just tweets "Guys, the police is over here, just go to X through Y and Z."

Scott: Mm-hmm

Remon: That's it, so it's like real-time communicator and this is how we could, we could gather ourselves and being big. You know, the protest was huge, but they wouldn't be able to do this if they went to the assembly points that used to be. So it's a simple person going off the metro, underground, and sees the police. Just send a tweet, and everyone else tweets it, and that's it!

Scott: Mm-hmm

Remon: So, this is why we managed to be a big, big protests on the 25th, and this is how we managed to be bigger on the 28th. This is exactly why that is happening.

Scott: Why does it feel like it happened in 18 days? It seems like it really happened over a couple of years.

Remon: Oh yeah, tell me about it. We were like, everyday we were umm... when you see it now, after we are done, it's a very, very short period. Like 18 days is less than a month, to throw off a system that has been on for thirty, more than thirty years. It's strange. So what we were... at the beginning of every day, we were like thinking of what would happen. Everyone has his doubts, to be honest, and everyone had these confusions. It was really, really, extremely confusing inside. 

Remon: And there was big problem that happened as well that the national TV, the state TV, used to say things that the elder people think is true. So, they were from another generation, you know, from the 50's, and this was only, the only media that they can see. So, anything the TV says, then it's 100% true. So you can imagine me, me myself, I was in my home, working online, trying to... figuring out what happened from following way, way too many people...

Scott: Mmm

Remon: ... and thinking it over and, you know, "linking the dots together." And my family, who are, by the way, working at the national TV, they were like 100% believing that the people at Tahrir Square... our estimates, are, you know, they're like unemployed, poor, bad people, which is exactly the opposite. But this is what was the TV saying: "These people are causing chaos, these people are bringing our economy down, these people, these people..." So we, we practically had fights everyday, like for more than a week.

Scott: Mmm

Remon: Like, yeah, and I was the good one, I had some friends that has been kicked out their homes. So this is why they stays at Tahrir like day and night, because they don't have any place to go. Like, their parents kicked them out.

[Musical interlude]

Remon: I actually met like four of them, they were staying the night, spending the night, at Tahrir because they didn't have no place to go. So this is why if you saw the night shots, you would see many people because most of them were like kicked off their homes and stuff like that. They want to stay...

Scott: Wow!

Remon: Yeah! Yeah, yeah, they want to stay, they want to, you know, "make a statement" if we can say so. It was, it was very good. And, personally, here, at DashSoft we had even of our office boy... he used to come here, and you know we work from 8, so he comes here from 7:30 or something and leaves at 5, and then goes to Tahrir to spend the night over there...

Scott: ...Wow...

Remon: ... and then comes back again the second day.

Scott: I wonder if you feel like you own your country more, you own the revolution more, if you were in the square.

Remon: Yes, yes, extremely.

[Musical interlude]

Remon: When I went the first day, the first day I went was the Tuesday before, you know, the camels went in and all this stuff...

Scott: Mmm

Remon: ... This was the first day I went in after like, huge fights with my parents to let me go out. Because, you know, because of the old presence got broken and all of that, and we were protecting our homes. But once I felt, once I felt it safe to go in, and [not understood @26:24] my family, I just went in. So this was the first day, and when I went back, I went with people and friends and I've seen all the political and religion... and religious parties in...

Scott: Mm-hmm

Remon: ...in Tahrir Square. It was, it felt, to be honest, it felt like the US. I was in New York, having lunch, and I just see people from all, you know, Asians, black Americans, caucasian, Indians, everyone. Just, everyone just passing by in New York. It was, it was just... it felt, it felt strange. Because this was the first time that they see all, all you know, the nationalities in the same place. I felt the same when I was in Tahrir, but that time I saw all the ideas. I've seen Muslim brotherhoods, I've seen the guys who, I don't know, Caliph? Caliph are the guys who follow the way, the exact way of the prophet Mohammed...

Scott: Mm-hmm

Remon: The prophet of Islam, they exactly follow the same way, like 1,400 years ago -

Scott: They are very devout, and very, like, a hasidic jew is very specific about Judaism, they are very specific about Islam.

Remon: Exactly, yes exactly. So I saw Caliph, I saw Muslim Brotherhood, I saw the medium [unintelligble @28:03] parties like they're ok, they're not very extreme. I saw the National Democratic Party, I saw some of them. They were protesting against their party, which was cool. And I, actually I saw everyone. 

Remon: This time, this day I had an interview with Thomas Friedman and I had like five interviews, and everyone was asking us "What do we think?" and Why.. why we, you know, "What do we think?" and "Why did are we staying here?" and "What do you want?" and I told him: "It's a very simple thing, everyone came here wants to say something, I'm OK, I have, I'm running a company, I have a nice car, I have a nice apartment, I'm OK. Like I don't need money, and I have a good education. But I'm here because I'm 28, 27 years old and I want to elect another president before I die."

[Musical Interlude]

Remon: After being in Tahrir, I felt like washed out. You know, being seen, all of these people are the same place. Talking to them, we actually, I was part of the people who held the prayer at Tahrir. And I was organizing some of the blood donations, because people were needing blood. Once I went there and I saw Caliph, these Caliph guys looking strangely at how the Christians are praying and, you know, they were like looking very, very, very curious about what we're doing, and trying to ask themselves and stuff like that. This was very good. 

Remon: Now you can see that there people in Egypt that they were not even open to each others and see how did they live. This is why you expect that there would be tension and stuff like that...

Scott: Mmm

Remon: But, seeing those people, like all in the same place, and all saying "Please God" at least - all of them. Like Christians and Muslims and everyone, saying "Please God, do this" - It was, it was awesome. And when all of us, the people said, "Long live Egypt!" and we're all one hand, you know, when you hear like couple of millions screaming the same thing, "Long live Egypt!" at the same time, they were screaming, not shouting, everyone, not chanting, everyone's like saying from the heart, like really from the heart: "Long live Egypt!" This is like, you know, not only gives you goosebumps, it just, it washes you from inside out. You feel that you have your country back again when you see everyone, can you imagine? Maybe you could have been in, you know, a party or something like, you know when you have thousands of people at the same place, at the same time...

Scott: Mm-hmm

Remon: And they're all chanting the same song? You know the feeling of everyone saying the same thing at the same time? Multiply this by ten, at least. This is, this is how we felt inside Tahrir Square when we all, we all saying "Long live Egypt!" or "Tahya Masr!" in Arabic. Tahya Masr: T-A-H-Y-A, "Masr" is "Egypt": M-A-S-R. This was strange, you know, very, very, very, very powerful.

Remon: And after the revolution succeeded, and, of course I went to the streets with my all friends celebrating as well. And on the second day, when the President has quit, has resigned, I went the second day to Tahrir Square and I had like, tons of photos of what's happening. And I, you know, I went like 6:00 in the morning, very early, and there were people standing over there. Over the bridges, there were bridges you know very close to Tahrir Square. Six foot [unintelligible @32:17] bridge.

Scott: Mm-hmm

Remon: I parked my car, everyone was parking his car at the bridge, like there was no traffic still. And I started seeing people getting their families, you know, children and wives, and stuff like that. And it was their first time to come over and see who are the guys who did this to Egypt. It was very, it felt extremely great when, when you explain to people what you've been part of. Like, "Guys, this is why it was happening, these are the people that's happening" and you see the fire, the fire in the eyes of the protesters, who were very proud of what they did.

Remon: I saw people, their eyes were sparkling when they explained to other people what happened, and how they slept, and how they've been beaten, and how they beat back. It was, it was life changing experience, if I can say that.

Scott: Yeah

Remon: Yeah, we were extremely proud. We felt that this is our country, and that we should take care of it.

Scott: What do you do the night that you, you're in the square, and you hear that he's going to step down. How do you go to sleep that night? I mean, how do you even go to work the next day? What do you...?

Remon: [Laughs] No, actually no, no one had slept that night. So, I'll tell you what happened exactly. So we were, we had this huge amount of rumors that he was leaving on the Thursday night, and actually the CRA said this, and everyone, everyone saying that he was stepping down. And he actually, he was stepping down that day, but his son like changed his speech and forced him to do another speech that he's not stepping down.

Scott: Uh-huh

Remon: So, I went to Tahrir that day, and I'm not sure if you've ever seen this or not, have you seen a very crowded bus?

Scott: Uh-huh

Remon: Like, you know buses, a very crowded one that you skip ten people "excuse me" to go through. It was even worse than that. In a huge square, you can imagine the amount of people that were there. Seriously, people got hurt from people sometimes stepping on them.

Scott: Wow

Remon: Yes, exactly, that was, it was that crowded. So we were waiting, and waiting, and waiting, then I went to the guards, because you know there was sort of like the scouts, the scout boys. There were guards around the perimeter to search people, and making sure that no one, you know, carrying weapons or anything. No one is trying to sabotage what's happening now. So I stayed with them, I had my phone and I used my headphones as... to use my phone as a radio.

Scott: Uh-huh

Remon: And we got the speech, and I start listening, and repeating to the people around me what the President is saying. And I was, this was like one of the most depressing moments in my life, like I say words I don't really understand anything, it doesn't mean anything to me. I keep listening and saying, listening and saying, like automatically. And then once it's just done, the speech has been done, he's not stepping down, and everyone was like getting crazy.

Remon: They actually went to the state TV, [unintelligible @35:51] it's really, really close to the Tahrir Square and the Egyptian museum. And they went to the place, the TV, and people start marching from Tahrir Square to the President's palace. The people was chanting that he must step down, the President must step down, the people wants the President to step down.

Scott: Mm-hmm

Remon: Everyone was outraged, and very, very, very depressed. And I when back this home, this day, I was like... I didn't know what to do, but we all agreed with one thing: That people will live in Tahrir Square. They actually started to build bathrooms, you know, and Pizza Huts. Pizza Hut and Hardees, they were having, you know -

Scott: [laughs]

Remon: Yeah, actually they start building inside Hardees. They start putting in bathrooms, and start getting more tents. And we now we're living here, no one is going to touch this land. And you can imagine more than 2 million people at the same place, and more than 500,000 are staying, and not leaving. Like 1/4 of them, and another quarter us are moving to the national, you know, to the President's palace.

Scott: Uh-huh

Remon: The army was very confused, at least this is what I see from my point of view. That if they now, they can do like what the Gaddafi is doing now, they're shooting their people or they're just forcing this president to leave. And this is what happened. I wasn't there, a friend was there, and he said that they moved the tanks, you know the tanks have this huge gun, they were aiming at the protesters. And then, just like that, they switched; they turned the guns back to the palace.

[Brief musical interlude]

Remon: Everyone was like chanting and screaming this means that the army is with them now, and actually, yes, that's what happened though. All the tanks now are aiming at the palace, and people were like "Yes and no, make Egypt only if Egypt" and "Tahya Masr" and, yeah, and then the president came... the vice-president came and say the President is resigning.

Excerpt of televised statement by Omar Suleiman: "President Mohamed Hosni Mubarak has decided to waive the office of the President of the Republic and instructed the supreme council of the armed forces to run the affairs of the country."

[Musical interlude]

Remon: We were exploding, exploding of pride, that day.

Scott: Mmm

Remon: This is at least the reason I can say you cannot see the people on the streets; a humongous number of people. I have never, I've never seen this people in the streets at the same time happy. This was the first time in my life I see this. So, yeah, people... no one, no one has slept that day. 

Scott: Mm-hmm

Remon: I went back at like 2:00 or 3:00 in the morning, and 6:00 in the morning, I couldn't stay more than 3 to 4 hours, and I went back to Tahrir and started telling people what we did, and this is what we did for you. You welcome, now no need to "thank you" - we all did it for us, and you welcome. People were like, "Oh, so you see this is the place that has been been burned, and these are the errors the people were making." And some of them went to, actually went inside Tahrir Square and it was the first time they see it this way.

Scott: Mmm

Remon: You know, we're having all the protesters, and everyone. It was, it was just awesome. It was awesome explaining to people what you did and what you've been part of. You just, you know, this is when you know that this is your country, and no one can even force you to do something like this, you know, to give up this right again. Now we understand why, I personally understand why the Americans, when you say "fight for freedom" - when you guys fight for freedom for yourself inside the US. I know now why it was meaning so much, even in the, you know the civil war, and all of that. Now I know what you guys were feeling right there.

[Musical interlude]

#### End Credits

(Voice-over) Scott: Many, many thanks for the folks that were involved in today's show. Certainly Rob Conery, for his amazing editing and music choices. Also, our volunteer editors: Besnik Belegu, Jon Galloway, Marsel Dupris [spelling? @41:14], and Troy Howard who helped some audio problems that we had. Most of all, thank you to Remon Zakaria for telling his story, a story that could have gotten him in trouble before the revolution, but now a story that we can share on This Developer's Life. Thank you.

[Music]

(Voice-over) Scott: And again, a big thank you to the folks at CodeRush for Visual Studio for helping support This Developer's Life. CodeRush has the fastest rename, the fastest "find all references", the fastest test runner. When it comes to creating, modifying, and refactoring code, nothing's faster than CodeRush. It's been on my Ultimate Power Tools list since forever. Get CodeRush, you'll be glad you did, check them out at [devexpress.com/coderush](http://devexpress.com/coderush). We appreciate their support.

[Music]
