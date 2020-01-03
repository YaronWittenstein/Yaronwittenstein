---
title: "The Importance of Unlearning"
date: 2019-06-27T22:17:31+03:00
tags: ["education"]
---

![Headline][Headline]

The world of software is changing constantly at a very fast pace.
Yesterday’s axioms might be tomorrow’s anti-patterns.

Newborn technologies rise to popularity and most of them will become obsolete sooner than expected and hardware advancements make game changers
for things that were considered as science-fiction a few years ago possible.

The only certainty is that we don’t know what the future will bring us.
<br/>
<br/>

## Emerging Technologies
Here is a partial list of recent years emerging technologies:

**1. Blockchain**
<br/>
Needless to say that blockchain has a good chance to disrupt the world as we know today
<br/>
<br/>
**2. Machine Learning Renaissance**
<br/>
The increase of Hardware capabilities brought a new wave of tools and disruption to many industries that take advantage of Machine Learning
<br/>
<br/>
**3. Containers**
<br/>
Now it’s much easier to deploy self-contained isolated components to the cloud. Containers orchestration infrastructures that only giants like *Google* had in-house are now publicly available for everyone (Kubernetes is the king here for now but the future will bring new tools for sure)
<br/>
<br/>
**4. WebAssembly**
<br/>
The motivation is to have one universal bytecode that will be used not only on the browsers but on everything (desktop/smartphones/god knows).
This technology will transform the portability of software between platforms
<br/>
<br/>
**5. Rust**
<br/>
One of the most innovative programming languages ever invented,
makes system programming a real joy. The most loved programming language in *Stack Overflow survey* for the last 4 years
<br/>
<br/>
**6. Elixir**
<br/>
The solution to how to make Erlang virtual machine (called BEAM) mainstream, mainly thanks to its Ruby-like syntax and great tooling
<br/>
<br/>
**7. Serverless**
<br/>
Why deploy containers to the cloud when we want only a single function that doesn’t need to be up 24x7?
<br/>
<br/>
**8. GraphQL**
<br/>
REST API is not ideal for every problem, many data models are actually viewed better as a graph and this protocol plays nicely with them
<br/>
<br/>
**9. Redis**
<br/>
The innovative key-value database having so many data-structures.
The most loved database in *Stack Overflow survey* for the last 3 years
<br/>
<br/>
**10. Kafka**
<br/>
Distributed commit log that serves as the single point of truth of a system data. It makes it very easy to add/remove independent producers/consumers for our system architecture.
Thanks to Kafka it's easy to select a checkpoint and *“re-play”* historical data.
<br/>
<br/>

On the one hand, it’s an exciting time to be a software developer.
On the other hand, it means that in order to keep up, we must not stop learning or we’ll become irrelevant

<br/>
I’ve always loved (and still do) learning.
<br/>
I love reading technical books (I own too many).
<br/>
I love reading beautiful pieces of source code.
<br/>
I always seek for ways to be more productive and get out of my comfort zone.
<br/>

**But, I think there is one important thing that people often overlook and is the importance of unlearning things**
<br/>
<br/>

## Unlearning
Unlearning means we need to accept that there might be more than one solution to a given problem, and this solution might be counterintuitive for us.
<br/>
<br/>
It also requires humility and willingness to start over in order to gain a new perspective and extend our toolbox.

Let’s review again the above list of technologies:
<br/>

**1. Blockchain**
<br/>
In order to understand how blockchain technologies work, we must forget about the centralized middleman model.
<br/>
<br/>
**2. Machine Learning**
<br/>
For example, we need to accept here that computer neural networks can output results which we’ll be impossible for us to understand exactly where they came from
<br/>
<br/>
**3. Containers**
<br/>
Containers disrupted the DevOps world and are the key reason for the micro-services architecture explosion. Without them, we’d stay with more monolithic systems.
<br/>
<br/>
**4. WebAssembly**
<br/>
Will open many opportunities, the obvious is using new programming languages for Frontend Programming. Another world of possibilities will be consuming WebAssembly libraries and using them within our applications. For example, a Rust program that will initiate a WebAssembly runtime hosting other wasm programs that were originally coded in Golang/Swift/other)
<br/>
<br/>
**5. Rust**
<br/>
Learning the Rust programming language [requires us to think on resources differently][rust-can-be-difficult-to-learn] in terms of borrowing/ownership.
<br/>
<br/>
**6. Elixir**
<br/>
[The Let it crash][the-zen-of-erlang] philosophy of Erlang asks us to accept unknowns and that things will break and prepare for them from the beginning
<br/>
<br/>
**7. Serverless**
<br/>
Asks us to stop thinking only about services but also about single functions. It opens new opportunities to save money since we only pay for when the usage of a function (which might not be available 24x7)
<br/>
<br/>
**8. GraphQL**
<br/>
Requires us to accept that REST isn’t always the best for every scenario and that sometimes there is actually a graph. (I personally think that starting from a REST API and gradually move towards a GraphQL is less risky for a green-field project)
<br/>
<br/>
**9. Redis**
<br/>
Requires us to represent data in many more shapes: Key-Value / Hashes / Set / SortedSets / Lists etc.
<br/>
<br/>
**10. Kafka**
<br/>
Once we start viewing our [system data as a log][every-software-engineer-should-know-about], we can think more about replaceable components on our system. For example, we can easily add a new consumer and make it process data and spill it into a new database and know it won’t interfere with the rest of the system.
<br/>
<br/>


Unlearning is a continuous inner fight. If done properly can be a huge enabler and if not, then we risk missing growth opportunities.
<br/>
<br/>
_A change in perspective is worth 80 IQ points_
<br/>
_- Alan Kay_


[Headline]: https://miro.medium.com/max/715/1*XqvZXIMCxaob-BdWNV2AOw.png
[every-software-engineer-should-know-about]: https://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying
[the-zen-of-erlang]: https://ferd.ca/the-zen-of-erlang.html
[rust-can-be-difficult-to-learn]: https://www.influxdata.com/blog/rust-can-be-difficult-to-learn-and-frustrating-but-its-also-the-most-exciting-thing-in-software-development-in-a-long-time
