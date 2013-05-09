---
layout: post
title: "Railsconf 2013 Highlights"
date: 2013-05-08
comments: true
categories: [Conferences]
author: Arturo Contreras
author_url: https://twitter.com/art_k5
---

# Keynote and Rails 4
![Railsconf](https://pbs.twimg.com/media/BJSdOFeCMAEvWFG.jpg)

This year, AllPlayers.com was kind enough to send me to this year's amazing Rails Conference that was held in Portland, OR and where I have gathered valuable ideas that will potentially help our company's processes and where I met awesome people that have run into the same problems that plague us and some possible solutions to help our company grow and become a leader in web applications technology.

I consider myself fortunate to have assisted such an event and thought to summarize some of the key points covered in the talks, this by no means intends to highlight the most important or better talks but rather what I believe to be more relevant to us as an emerging technology company.

The first [keynote](http://www.justin.tv/confreaks/c/2246896) given by David Heinemeier Hansson ([@dhh](https://twitter.com/dhh)) focused on discussing the reasons and motives behind the creation of Rails and where Rails is going with version 4, important aspects of this new version are covered nicely in this [tutorial](http://net.tutsplus.com/tutorials/ruby/digging-into-rails-4/). Key points include:

*    Good Frameworks and abstractions, not inventions.
*    Key to ROR community embraces and accepts the difficulty of change.
*    Objective is to make web faster to combat main competitors of web (HTML), which are development of applications (iOS, Android)

### [Embrace Javascript](http://www.justin.tv/confreaks/c/2246947) - Yehuda Katz [@wycats](https://www.twitter.com/wycats)

Yehuda Katz, better known as wycats, presents a sort of counter argument to DHH and tells us to embrace our javascript, meaning that all web applications require javascript and some even have close to 1MB of javascript and some developers tend to hide that javascript and not really pay any attention to structure and organizing that code, people tend to think that they will just sprinkle some javascript on top of their server side application to make it nicer when really that sprinkle turns out to be a huge part of the app itself. Some interesting points he makes are:

*    Don't hide your javascript. most if not all web apps have huge amounts of javascript and frameworks like Rails tend to consider javascript as just a sprinkle on top of the server side code.
*    Ember.js and Backbone.js are similar to initiatives started when PHP was just a sprinle of code to present web applications and Rails was created to present conventions, DRY code and organizable structures.
*    Lastly, wycats reinforces the need of developers to "Be Proud of Your Javascript" as you are proud of your app (server) code.

### [Stables vs Volatiles](http://www.confreaks.com/videos/2415-fhc3-stables-and-volatiles) - Michael Loop [@rands](https://twitter.com/rands)

Michael Loop talks about the stand out personalities that he has worked with in his carreer at Borland, Netscape and Apple. He can classify people into two major categories, Stables and Volatiles.  Volatiles tend to invent a lot of stuff while stables tend to like to organize and actually make it into a product.  You need both of these types to have a succesful startup company.  Volatiles tend to create something and then slowly grow and stay in maintenance mode because they tend to want to protect what they've built and when that happens is that volatile types get bored and thats when developers tend to stray away from the company.

*    Developers tend to have a 3 year lifecycle at their jobs, Why? Most developers are somewhat volatiles types that want to change/improve/innovate and after about 3 years they start feeling stuck and turn stable and thus feel uninspired.
*    A lot of companies might try and get rid of their volatiles thereby making the company stagnant and developers unmotivated.
*    Solution is to try and create an environment where both volatiles and stables coexist to create new and innovative products while maintaining structure and organization.
*    One innovative course is to allow developers a 1 month period every 2-3 years to completely isolate themselves/team and start with a clean slate to create whatever they want, thus helping companies keep their innovators and possibly use the “flying toaster” being created.


Now, to give an overview of how each day went and the key aspects of each talk.

*	John Duff talked about how [Shopify scales rails](http://www.slideshare.net/jduff/how-shopify-scales-rails-20443485).
	- Knowing what to scale by measuring and quantifying performance (New Relic, Splunk, StatsD)
	- Analyze one request and one process and how long that takes, along with how many RPM (Requests per minute).
	- Scale by upping the number of workers and reducing the response time of each request.
	- Use Resque to process jobs like payment processing, sending emails, geolocation, import/export, indexing for search.
	- Split out standalone services as needed, independently scaled, limit to what is necessary.
*	Zach Briggs of testdouble.com gave a brief talk about how we can improve as developers
	- Memorize a good tutorial https://github.com/garybernhardt/sucks-rocks
	- Write down our googles.
*	Testing HTTP APIs in Ruby by Shai Rosenfeld of EngineYard
	- Best way to test a server/client HTTP API is by using a mocking system like Fog, have isolated fake servers.
	- Mimic the API with a fake server, have slim code and keep it simple by focusing on return values and not necessarily on internal processing.
*	Object-Oriented Lessons for a Service-Oriented World by Chris Kelly of New Relic
	- Constructing a Network-based application software and coordinate systems to interact with each other is the goal of a service-oriented architecture.
	- Cache is very important so cache control and e-tag are a first order feature.
	- Hypermedia is a series of constraints, basically link relations of rest responses.
*	[Real Time Rails](http://slid.es/bcardarella/real-time-rails/) by Brian Cardarella
	- Real-time is just one of the areas where node.js has outpaced rails
	- Puma web server is emerging as the popular web server for rails because of its concurrency of being able to handle many requests at the same time.
	- Frameworks like Ember (and other) are growing and need a strong backend solution.
*	Embedding sinatra on a rails application by Jose Valim
	- You can easily create a one file rails application embedding aspects of sinatra in your rails application.
	- Uses may include testing rails code, quickly setting up and testing gems, learning how the whole rails stack initializes and how middleware can help.
*	Rails vs the Client Side by Noel Rappin of Table XI
	- Historically JS has been avoided by Rails, slowly getting better frameworks.
	- Decide where to build and have most of your application logic, on Server(Rails) or on Client (Ember).
	- Do ember.js and node.js still need Rails? Maybe, use Rails::API, having Views extracted.
	- Both argue that their system is simpler, less complex.
	- Simplicity is being able to deal with components separately (Rails).
	- Simplicity is using simple structures (Ember).
	- With rails, server side sometimes sends JS, HTML, JSON and code logic tends to get duplicated between server and client.
	- In client side apps, you only need to go to the server on new requests, minimizing server interaction improves speed on lagged connections.
*	Designing Great APIs by John Dal
	- As developers we want the API to have a design.
	- Correlates API design to politics and the english language (George Orwell).
	- A good API is minimal, gets out of the way, direct and almost don't notice it (REST) and is consistent.
	- Design for the edge cases, middle will take care of itself.
	- Make sure API is honest and returns message with correct code.
	- Invest in delight and performance features.
*	Describing Your World with Seahorse by Trevor Rowe of AWS Services
	- Services should be Entities not side effects of your application
	- Seahorse is a Service description language, it has a gem that you can install in your rails app and extend the Seahorse class to better define your public API and automatically generate documentation with Seahorse compatible automatic documentation like YARD. Guzzle PHP uses it.
*	Services and Rails, the stuff they don't tell you by Brian Morton of Yammer
	- Goal is to achieve components that scale individually
	- Throw resources where needed
	- Independent updates
	- Easier to change components
	- Build dummy components to work on individual services
	- Cross-functional teams 2-10 people 2-10 weeks
	- Have a support rotating team for maintaining existing features.
	- Move the data so the service owns it, use your services as indexes, just store IDs.
	- Moving data means duplicating, chances are you can't have downtime to move data.
	- Use vagrant to make it easy for developers, close to production, running services locally, keep up with rapidly changing services, don't need knowledge of services.
	- Handle unavailability, transactions aren't free, API's are much harder to change (versioning).
	- Complex systems fail, know what happens is service is down.
	- Have standarized tools for deployment and monitoring.

### LINKS

*	[All the talks](http://www.justin.tv/confreaks)
*	[Cool Overview](https://medium.com/ruby-on-rails/6061138c2f70)
*	[Links Day 1](http://blog.smartlogicsolutions.com/2013/04/30/22-links-from-railsconf-2013-day-1/)
*	[Links Day 2](http://blog.smartlogicsolutions.com/2013/05/01/22-links-from-railsconf-2013-day2/)
*	[Links Day 3](http://blog.smartlogicsolutions.com/2013/05/02/31-links-from-railsconf-day-3/)
*	[Links Day 4](http://blog.smartlogicsolutions.com/2013/05/03/4-links-from-railsconf-2013-day-4/)
