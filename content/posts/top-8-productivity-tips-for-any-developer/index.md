---
title: "Top 8 Productivity Tips for Any Developer"
date: 2019-08-21T17:15:00+03:00
tags: ["productivity"]
type: "post"
---

![Headline][Headline]

One of the subjects I've always been very passionate about is productivity.
Looking for ways to do more in less time and effort is a matter of high importance.
Saving many tiny-energy exertions across a workday adds up to a significant energy saver in total.

The internet is flooded with programming productivity articles.
Isn't writing a new one is kinda unproductive? &#128521;

Well, the vast majority of programming productivity articles are very specific.
Here are some examples of the articles you should expect to find:

* Must have tools for any Mac Web developer for 2019
* Top 10 tools for any Windows programmer
* Most popular tools for Web Development

<br/>
I wanted to write an article that will focus on principles before the tools.

</br>

## **New tools come and go frequently. What stays with us are the principles!**

I've found, what I believe are the top 8 productivity principles any developer should employ.

I'll also provide with tools recommendations for Mac since I'm a Mac user.
Several of my recommendations run on other Operating-Systems as well.
Regardless of my suggestions, applying these principles to other Operating-systems or finding alternative Mac tools should be easy.

Again, what's important is sticking to the principles and not to the tools.

So let's drill down...
</br>
</br>
### **Principle #1 - Automating Workflows**

A decent amount of a programmer's time is spent on doing repetitive tasks over and over again.

Here are a fraction of some common scenarios:

* Searching Stack Overflow via Google.
* Killing an Operating-System process that hangs or just consumes too much memory due to a memory leak.
* Clearing the browser cache and refreshing our local http://0.0.0.0:8000 development page.

Part of these examples are non-direct programming tasks but are still indispensable for any professional programmer.
For example: Looking for the time-zone/weather in other parts of the world.

Many of these repetitive tasks involve a sequence of steps:

* When looking for help at _Stack Overflow_, we need to go to the browser first and make a search via some search-engine.
Then, we'll select one of the top results which will probably direct us to a  _Stack Overflow_ page,
even if we didn't add the term `stackoverflow` explicitly to the search itself.

* In order to shut down a frozen Operating-System process, we first need to look for its process id (PID) and then execute a kill command.
(or go to a process explorer GUI, find it there and ask for killing it).


Fortunately, there exist various tools dedicated to automating these manual repetitive actions.

If you're a Mac user then, macOS ships with a tool called [Automator][Automator] that lets you create very complicated workflows.
I can't say more on that tool since I didn't actually use it. I use another one-stop-shop productivity tool called [Alfred][Alfred] which I'll mention a few times
during the course of this piece.

[Alfred][Alfred] is a versatile productivity app for Mac users. It's one of the most popular productivity Mac apps for years, and for a good reason!
One of the key strengths of Alfred is Workflows.
Here is an image for illustration: ![Alfred Workflow Image][Alfred Workflow Image]

Basically, each tool has its own strengths and it depends on the situation.
To my understanding, [Automator][Automator] is more [IFTTT][IFTTT]/[zapier][zapier] style tool. [Automator][Automator] hooks into to low-level Operating-System events,
while [Alfred][Alfred] mainly glues different components together and start running when we command it to.

Tools like [Automator][Automator]/[Alfred][Alfred] are general-purpose Workflow tools. Each has its own pros.
There are also other, niche workflow tools/features. I use vim macros when I find a text-editing recurring pattern I'd like to automate during my work.
A classic example for using a vim macro would be scanning a list of words separated by a comma, surrounding each with quotation marks.

If you use tools like Excel, then I know its comes with full-featured programming-language called [VBA][VBA].
The internet has articles about people that automated most of their day-work leveraging [VBA][VBA] magic!

Sometimes the best workflow solution is essentially writing code. Usually, it'll be a small script consuming less than 100 LOC like a build script.
Other times, it'll be coding a small mini-project.

The key point to take is that if you find yourself manually repeating a workflow-oriented process, think whether it can be automated using a general-purpose Workflow tool
or using some ad-hoc software or if developing a solution from scratch will do the trick.

What's important is to stay alert and open for new automating opportunities.

<br/>

### **Principle #2 - API & Inspection tools** 

* **API Tools**

Almost any developer has some connection to at least one HTTP connection during his workday (sorry if the pun wasn't funny). Be it faking an HTTP request for testing,
or triggering some running code on a server endpoint. Good HTTP interface (a.k.a API tool) is mandatory.

I highly recommend using [Paw][Paw]. Most people use [Postman][Postman], which is more feature-heavy. [Postman][Postman] also has running load-testing capabilities and many integrations.

![Paw image][Paw image]

<br/>

Once you use an API tool, make sure you save request files for future use.
This can be a huge time saver if you mess a lot with the same API endpoints, only changing parameters instead of synthesizing from scratch each time
you need. Additionally, sharing files between team members is important. You may want to have some shared place with widely used requests.
It's can also serve as a complement to your knowledge-base of the system.

If you work with higher-level popular protocols like gRPC you'll probably find matching UI tools that will suit your needs.

* **Inspection Tools**

On other occasions, you may want to be passive and just sniff traffic and record the packets for later investigation or for replaying traffic.
When I really needed a good proxy for inspecting data for Mac, I've used [Charles][Charles].
Many years ago I've played a bit with [Fiddler][Fiddler] on Widows. It outgrew to support any popular Operating-Systems.

This item won't be complete without mentioning the classic [Wireshark][Wireshark] of course.
As you probably know, each Operating-System comes with built-in command-line tools such as tcpdump / curl.

<br/>

### **Principle #3 - Clipboard History** 

Did it ever occur to you that you pasted some text into your IDE file just to realize that the Clipboard had another more recent content while you
had no longer access to the previous Clipboard data?

Not anymore. Using a Clipboard history is a must-have tool!

I'm using [Flycut][Flycut] but there are more alternatives for Mac. Actually, [Alfred][Alfred] has a Clipboard History feature built-in.
Even if you have a Clipboard history integrated within your IDE. It's still advisable to have a cross Operating-System Clipboard History tool.

A small tip: if you're a Mac user and wants a very nice utility for selecting text and copying into the Clipboard, I highly recommend [PopClip][PopClip].
This tool has many extensions. Like, selecting a word and asking for a Dictionary translation, or selecting a word and opening [Dash][Dash] on that word.

<br/>

![Flycut image][Flycut image]

<br/>

### **Principle #4 - Text Expansion & Abbreviations**

* **General Text Expansion**

The classic usage of text expansion is writing an abbreviation representing a longer text-blob and then the text expander semi-magically substitutes the abbreviation
for the expanded text.

Programmers can benefit from text-expansion a lot in the context of code snippets.
I'm currently not using a Snippets Manager, although I might use one someday. BTW, [Alfred][Alfred] comes with a Snippets Manager out of the box too.

I mostly use text expansions for visiting links like Google Docs I frequently visit.
My text expander software for Mac is [aText][aText]. You probably guessed right that [Alfred][Alfred] offers it's own Text Expansion feature which I didn't try yet, but I bet it's awesome.

![aText image][aText image]

* **Command Line**

In the command-line, I use many abbreviations aliases for longer commands (defined in my **.zshrc** dot file).

For example: Instead of writing **git reset HEAD --hard** for a local Git repository, I just write **grhh**.

If I need to merge branch **develop** onto the current branch, I just type **gmd**.
Or instead of opening vim with the **vim** command, I just insert **v**.

* **Side Note**

As a side note. Another tool in the realm of writing text is called [Grammarly][Grammarly].
It's an AI-powered writing assistant. I use it all the time when composing emails (also for fixing mistakes while writing this blog post ;) )

![Grammarly image][Grammarly image]

<br/>

### **Principle #5 - Instant local Search** 

People are flooded with data. And we're the programmers are no exception to that.
In order to shorten the search time looking for a piece of information, we must have good search tooling.

What do we search?

* **Files / Directories / Apps**

Well, that's relevant for any computer user. Search is the most used feature of [Alfred][Alfred].
I prefer it over _Spotlight_ which comes with macOS.

![Alfred Search and Browse][Alfred Search and Browse]


* **Fuzzy-Search the Command-line History**

The command-line is a programmer's best friend. We execute tons of commands during any single programming session.
We usually repeat some recently used command, but not necessarily the very last one, making us press ↑↑..↑ in order to find the desired command.

The cool way is to fuzzy-search our Command-line history.
I'd like to recommend an awesome tool called [fzf][fzf].

This gem lets us enrich our Command-line history with search-as-you-type (a.k.a fuzzy-search/incremental-search) capabilities.
Not only that, but it also has another great feature for searching for a file by name with a preview mode option.
So if we search for a file we can see it's preview in order to make sure that's what we seek for prior selecting it.

This treasure is supported by any Operating-System and even has an official vim plugin called [fzf.vim][fzf.vim].
(I believe there are non-official plugins to other IDEs).

![fzf gif][fzf gif]

<br/>

If you're a zsh user, a super-handy plugin is [zsh-autosuggestions][zsh-autosuggestions].
I use [zsh-autosuggestions][zsh-autosuggestions], and when I type a command, I get suggestions from my Command-line history
which makes finding most commands a breeze without even asking for the assistance of [fzf][fzf].

So [fzf][fzf] + [zsh-autosuggestions][zsh-autosuggestions] make an unbeatable couple together!

We use Command-line a significant fraction of our work. Being able to search our Command-line history is truly a must.

* **Offline Documentation**

One of the most frequent actions while programming is questioning "What's the syntax for doing _X_ in programming language _Y_?"

Instead of Googling for a syntax keyword or for some example showing how to use the standard library, it's suggested to have offline documentation ready for instant search on our machine.
It can save loads of time and reduce context-switches substantially while programming.

I use the most popular offline documentation tool for Mac called [Dash][Dash]. It comes with documentation sets for almost every programming-language
and also for many popular libraries. It also has integrations with any known IDE. Not only that, but you can add custom documentation of libraries
since [Dash][Dash] connects to many Packages Managers too.

For activating [Dash][Dash], most of the times I'm using the [Dash Alfred Workflow][Dash Alfred Workflow] for _Search & Open Dash_ via Alfred's prompt (it's super useful).

<br/>

![Dash image][Dash image]

<br/>

### **Principle #6 - Knowledge Management**

Inspired by the famous [GTD method][GTD] for organizing knowledge, I'm using a _TODO list_ app to ease my mind and offload tasks out of my brain.
Each time I'm thinking about something I need to do, I first add it as an item to my _TODO list_ app.
Later, this item might be translated into a GitHub issue or even a roadmap / technical-debt document.

For the past several years, I've been using [Clear][Clear].
I'll probably move to another app sometime since the last update was in 2016, and because I feel it lacks some features.
But overall, it does the job!

<br/>

![Clear image][Clear image]

If you want to have fewer tabs hanging open in your browser and gain more focus, please consult using [Pocket][Pocket] for saving articles for future reading.
It will help you clear your mind and focus on the current relevant tabs.

You may also use a Sticky Notes app for jotting down pieces you'll probably want to move later for another long-term representation usage.
And Speaking on long-term use, I'm a long-time avid user of [evernote][evernote]. Some people use [evernote][evernote] as their TODO list app too.
Whatever works for you, just make sure you don't overload your brain with information, you can let someone else store for you.

Knowledge Management can't be complete without mentioning a backup platform Dropbox/iCloud/GoogleDrive style.
Anything mentioned in this article is encouraged to be backed-up. Some of the apps have a **Connect-with** to a Cloud-provider integration,
thus making the backup process smooth.

<br/>

### **Principle #7 - Keyboard Shortcuts**

You probably know the keyboard shortcut for saving the current file changes in your IDE.
But do you know for example the shortcut for re-opening your last closed browser tab?

I believe that if one finds himself using the Mouse too often when a Keyboard shortcut exists, then he should struggle to start it.
The best technique for memorizing these Keyboard shortcuts is by using a Spaced-repetition flashcards software like [Anki][Anki].
[Anki][Anki] is available for any operating system (Mac, Windows, Linux, Android, and iOS).

I'm a big fan of [Anki][Anki] and it helps me much learning new things (Keyboard shortcuts is a good use-case) and retaining them for long-term use.

A side-note: speaking about flash-cards. Spaced-repetition is the best way to extend your language vocabulary.
For that I deeply recommend [SuperMemo][SuperMemo].

Putting the time to learn and memorize useful Keyboard shortcuts can have a tremendous positive impact on productivity.

<br/>

### **Principle #8 - Reading Code**

Apart from writing code, it's very important to have our reading and navigating an existing source code a pleasant experience.
When I read other people's code I usually prefer to read it outside of an IDE (it's just a personal taste).

<br/>
If I browse a GitHub repository I sometimes use [Octotree][Octotree] but I usually prefer to go with [sourcegraph][sourcegraph].

I really like [sourcegraph][sourcegraph] navigation and searching features. [GitHub has recently launched](https://help.github.com/en/articles/navigating-code-on-github) their take on code navigation, so we should expect it's only the
beginning of something big.

I recently came across a tool called [codestream][codestream] that lets you have an inner chat on the code within your IDE.
Although I didn't try that tool yet (vim support is upcoming), I believe it can be a great assistant for reading code since it lets you add bookmarks (called [codemarks][codemarks]).
[codestream][codestream] also integrates it with other tools like Slack and many issue-tracking tools.


![codestream image][codestream image]

<br/>

Make sure you enjoy a good reading experience while reading other people's code. It can mitigate this already mentally demanding process.


<br/>

**Summary**

In this article, I've summarised what I believe, are the top 8 productivity principles each programmer should aim to apply.
I'm humbled by the infinite number of tools and tricks available for us to apply these principles.

I believe that using these principles, can not only speed our work but also increase our joy and sense of fulfillment.

I'd like to thank you for reading this article!
<br/>
I hope you enjoyed reading it, and if you did please share it with your friends / Co-workers programmers.
<br/>
  Thank you!

<br/>

Links:

1. [Alfred][Alfred]
1. [Dash][Dash]
1. [Paw][Paw]
1. [Postman][Postman]
1. [Charles][Charles]
1. [Fiddler][Fiddler]
1. [Wireshark][Wireshark]
1. [Flycut][Flycut]
1. [PopClip][PopClip]
1. [aText][aText]
1. [fzf][fzf]
1. [Grammarly][Grammarly]
1. [Anki][Anki]
1. [SuperMemo][SuperMemo]
1. [GTD][GTD]
1. [evernote][evernote]
1. [Clear][Clear]
1. [Pocket][Pocket]
1. [Octotree][Octotree]
1. [sourcegraph][sourcegraph]
1. [codestream][codestream]
1. [https://github.com/YaronWittenstein/productivity-tips-for-mac](https://github.com/YaronWittenstein/productivity-tips-for-mac)


[Headline]: https://miro.medium.com/max/880/0*SHZhejMPJFYc-vzd
[Automator]: https://support.apple.com/en-gb/guide/automator/welcome/mac
[IFTTT]: https://ifttt.com/
[zapier]: https://zapier.com/
[Alfred]: https://www.alfredapp.com/
[Alfred Workflow Image]: https://miro.medium.com/max/720/0*WSpawlEVG4QfapTu
[Alfred Search and Browse]: https://miro.medium.com/max/594/0*itSuJ8G8toe5wGUa
[VBA]: https://en.wikipedia.org/wiki/Visual_Basic_for_Applications
[Dash]: https://kapeli.com/dash
[Dash image]: https://miro.medium.com/max/1280/0*OCNkvNfsyLZCAez1
[Dash Alfred Workflow]: https://github.com/Kapeli/Dash-Alfred-Workflow
[Paw]: https://paw.cloud/
[Paw image]: https://miro.medium.com/max/1300/0*K2eo-r9NMlY7WvLu
[Postman]: https://www.getpostman.com
[Charles]: https://www.charlesproxy.com/
[Fiddler]: https://www.telerik.com/fiddler
[Wireshark]: https://www.wireshark.org
[Flycut]: https://apps.apple.com/us/app/flycut-clipboard-manager/id442160987
[Flycut image]: https://miro.medium.com/max/1280/0*7F6_jU2sVlB_uIz8
[PopClip]: https://apps.apple.com/us/app/popclip/id445189367
[aText]: https://www.trankynam.com/atext/
[aText image]: https://miro.medium.com/max/915/0*d7XvRHjvJe8Gzgks
[Grammarly]: https://www.grammarly.com
[Grammarly image]: https://miro.medium.com/max/800/0*x9N5XofCZX36y1n1
[fzf]: https://github.com/junegunn/fzf
[fzf gif]: https://miro.medium.com/max/768/0*EXVV-YcIydVzZoy1
[fzf.vim]: https://github.com/junegunn/fzf.vim
[GTD]: https://gettingthingsdone.com/
[Anki]: https://apps.ankiweb.net/
[SuperMemo]: https://supermemo.com
[Karabiner]:https://pqrs.org/osx/karabiner/
[evernote]: https://evernote.com
[Clear]: https://apps.apple.com/us/app/clear-tasks-reminders-to-do-lists/id504544917
[Clear image]: https://miro.medium.com/max/560/0*pUE_P3T4BRJgDJNw
[Pocket]: https://getpocket.com/
[zsh-autosuggestions]: https://github.com/zsh-users/zsh-autosuggestions
[Octotree]: https://www.octotree.io
[sourcegraph]: http://sourcegraph.com
[codestream]: https://www.codestream.com/
[codemarks]: https://www.codestream.com/codemarks
[codestream image]: https://miro.medium.com/max/968/0*2DJKHCLV5UBBXiHw.gif
