# darknetp2ptechtorwebhostimgwebsites
Where Darknet websites are hosted?
Originally Answered: Where Darknet websites are hosted ?

Let me answer your question in parts.

Legality of the dark web

Making a website on the dark web is as legal as making a website on the public internet. Of course: Using the dark web may make you a suspicious person for government intelligence services, but as long as everything is legal, you cannot be procecuted of doing anything wrong.

This is different for becoming a Tor relay, because you share information of other people. If you are the exit node of a Tor relay chain, then you may get in trouble, because you may be sharing illegal information. I will come back to the words "Tor relay" and "exit node" in a moment.

So in short: A website would be legal, but if you become a tor relay as well, it is not.

Where are they hosted?

They are hosted everywhere, yet not at bluehost (or anything other web hosting provider). If you have an internet connection, you are able to set up a webserver rightahead. This holds true for the public internet, as well as for the dark web. You can be your own hosting provider.

Usually: Software for hosting websites are Apache2 or Nginx (often with modulessuch as MySQL and PHP), or even custom-written web servers in python and node.js. This way, you can host websites at your home computer, at a server in a data center or anywhere you like. You only need a provider for a domain name like Example Domain , or you let people conntect to your IP-address http://111.222.123.111 (completely randomly chosen), which is provided by your internet provider.

Home-hosted websites are not popular, because internet connections at home do not provide sufficient bandwith to be able to host a site, and DDoS attacks are easily performed. Because Tor is slow (yes, it is), a connection speed of 200 kbits would already suffice to host a Tor site.

You are referring to http://bluehost.com. This is a web hosting provider, that makes you forget about all technical stuff that I discussed above. They provide you of a domain name, and all the software that's needed to host the website (like Apache2 with MySQL). Therefore, hosts like these are not suitable for the dark web.

In the dark web: You can set up the web server for yourself (locally), request a .onion domain (in the case of Tor) and everyone using the dark web can access your website.

You may ask yourself why .onion-websites usually have weird links. That's due to the fact that people can not (practically not) choose the domain name they want. This is due to the cryptographic background of Tor: A key is generated, and Tor will generate a .onion-domain that fits to your key. Then, you can host content over that domain, on the dark web.

So in short: Tor websites are hosted at home, or at a hosted server in a data center. Not at bluehost :P

How governments can't take them down?

I will write this for Tor. I don't know about how i2p solves this issue, but I think it's very much like Tor does.

Suppose I am not using Tor, and want to connect to the website http://Quora.com. At the moment I enter "http://Quora.com" in the browser, the browser will do "Ask for http://Quora.com's IP, and connect to it".

Paragraph 1, How Tor works, "for dummies"

When I am using Tor, I put this operation in a box 1, locked with a padlock. This box is done in another box, box 2 again, and lock it with another padlock. I send the total to someone that knows the code of box 2, and this person unboxes it, and sends the remaining box 1 to someone that knows how to unbox this. Now only you and the owner of the key of box one know what's in the box.

Now the owner of the message that I want to send, does exactly that, and sends it back in the same way. This way you get a two-way communication channel, visualised as follows:

You <--> S1 <--> S2 <--> Internet

S1 does know who the message came from, and who it's meant to be sent to, but has no clue of what's inside.

The persons S1 and S2 are called Tor Relays. The person S2 is a exit node, since he's the one who sends the messages for you.

In practice, Tor uses three tor relays before your message reaches the internet:

You <--> S1 <--> S2 <--> S3 <--> Internet

Because the Tor Relay Servers are geographically deverse, governmental interception is very impractical. If S1 is in the Netherlands, S2 is in Sweden and S3 in Canada, then these three countries need to work together to find out who the person is that sends the message, and what's inside the message. This is what the security of Tor relies on.

Also, many people that are using tor use the same relays, which makes it hard for governments to find what belongs to me, and what belongs to others. Even if data is retrieved, proving that you're the one sending it will be extremely hard.

Also by changing the tor relay chain often (such as: per website, or per visit), tracing anyone back to the origin will be practically impossible.

Paragraph 2, Tor websites

As discussed before, there are simple ways to get a Tor website in the air. The owner of the website wants to stay secure, the same way as the users of the websites do connect securily to the internet.

In the next story, I will be hosting a website on the dark web, and you want to connect to me.

As a website owner, I contact three tor relays the same way as you do to connect to the public internet. Suppose my website is wubwubwub.onion. I call the tor relays for this T1, T2 and T3.

My website <--> T1 <--> T2 <--> T3 (ok, I see wubwubwub.onion)

T3 now knows that if there's someone asking for wubwubwub.onion, that he should send something to T2, and T2 knows that he should send it to T1 that knows who I am.

Now you want to connect to my website:

You ("Give me Wubwubwub.onion!) <--> S1 <--> S2 <--> S3 (Oh, you want to connect to wubwubwub.onion.)

Either way S3 knows some relay that knows the website wubwubwub.onion, or it sends it to some other relay with the question to find that website.

You <--> S1 ... <--> S3 (I don't know this?) <--> S4 (?) <--> S5 (?) <--> S6 (Oh, I know that T3 knows wubwubwub.onion!) <--> T3 <--> T2 <--> T1 <--> My website.

We now have a bidirectional link, so I can send my website back to you. And due to diplomatic and practical reasons, governments will not be able to make a link between you and me in a structural way (such as recording your or my data).

Summary

Because governments aren't able to trace tor website owners down very well, people that host tor websites are basically untouchable. They are hidden behind a chain of geodiverse locations.

Disclaimer

This simple explanation of how Tor seems to be waterproof, but there are not-discussed and simplified technical and cryptograhpic aspects of Tor that I left to keep things relatively (*cough* I'm sorry *cough*) simple, and that I do not know about. With this post I hope that I gave you some insight on how Tor works, to which kind of people use Tor and why Tor opens doors for evil people.

It should be noted that you do not need to be an evil person to use Tor. For instance, privacy reasons and government surveillance are also reasons to use Tor. Or you are just an internet geek that wants to explore any kind of internet projects :P

2
Originally Answered: Where Darknet websites are hosted ?

Dark Websites are Hosted At Local Servers.

if i will host my website on my computer so you can say i hosted a website on my local server.

but all sites are not hosted on local servers .

if you want to make your website in your computer simple install tor and get free domain and start doing whatever you want do,

3
Originally Answered: Where Darknet websites are hosted ?

If you want to host your own website on tor here is the nice video on it.

How to Host .onion website via https://youtu.be/wFNY2ZT0u5c

optional READ

https://www.quora.com/How-do-I-host-a-website-anonymously

https://www.quora.com/Who-controls-the-darknet

https://www.quora.com/unanswered/How-do-I-find-secret-websites-on-the-Darknethttps://www.quora.com/unanswered/How-do-I-find-secret-websites-on-the-Darknet
https://www.quora.com/What-are-the-best-dark-web-sites

https://www.quora.com/How-do-I-start-a-porn-site
