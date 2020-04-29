---
title: "Train Your Own Neural Network"
date: 2020-04-03T12:06:33+03:00
type: "post"
---

These days, using Machine-Learning and particularly Deep-Learning solutions in order to solve many technical challenges has become a norm.
<br/><br/>
That's mainly thanks to having access to unprecedented volumes of data, hardware advancements and acadmeic progress.
<br/><br/>
Many problems are tackled by modeling Neural-Networks, feeding them with tons of data and consequently they "learn" and turn artificially "smarter". 
<br/><br/>
While we, humans, are still smarter than our computers - we do suffer from an inferior processing speed of information.
<br/><br/>
We can't read a million books over the course of our lifetime. 
<br/>
Neither can we write a billion lines of code, 
<br/>
speak fluently 100 different languages or paint million drawings. 
<br/>
<br/>
Yet, we are still able to accomplish quite a lot.
<br/>
Much more than we think we can. 
<br/><br/>
There is the classic saying that _"Practice makes Perfect"_. 
<br/>This is partly true, because it's also that _"Practice also makes you Permanent"_.
<br/><br/>
Now usually comes the part saying that we need to do _Deliberate Practice_ consistently for many years.
The thing is that there are multitude of ways to practice deliberately. 
There is no one size fits all formula applicable to all domains. 
And of course - people are different.
<br/><br/>
I'd like this article to focus on a single _deliberate practice_ side - I  call it _"Train Your Own Netural Technique"_ technique. 
<br/><br/>
For brevity, I'll use _TYONT_ acronym for the rest of the post. 
<br/>
The essence of _TYONT_ is feeding your brain with tons of data relevant to things you care about.
<br/><br/>
I'm dividing that training data into two categories: Factual and Pattern-Oriented.
First, let's address data belonging to the _Factual_ category. 
We'll differentiate between _general data_ to _domain-specific data_.
<br/><br/>

### Factual data - _General_:
This is straightforward - it's pieces of data that are mere facts.
#### Examples:

* Historical 
<br/>
 - _When did the French revolution took place?_
<br/>
 - _Who was the president of the United-States during World War II?_

* Wisdom Quotes 
<br/>
 - _"Success is never found. Failure is never fatal. Courage is the only thing. (Winston Churchill)"_  
 - _"Education is what remains after one has forgotten what one has learned in school. (Albert Einstein)"_

* Vocabulary 
<br/>
 - _Give two synonyms to the word: decisive_

<br/>
### Factual data - _Domain specific_:
Since I'm a developer and this blog assumes its readers are too, I'll use programming factual data here but you could see how it translates 
to many other fields.

* Shortcuts 
<br/>
 - _How do I re-open Chrome's last closed Tab?_ 

* Commands 
<br/>
 - _How do I discard the local git uncommitted changes via the command-line?_

* Syntax / Libraries 
<br/>
 - _How to create a new module in that language?_
 - _What's the 2nd parameter this common-library's function signature expects?_

<br/>
![flashcards-image][flashcards-image]
<br/>
### Patterns:
Now, let's move on and talk about the more interesting category: _Patterns_.
As opposed to factual data which is well-defined - _Patterns_ aren't so.
<br/><br/>
When I'm refering to a _Pattern_ here, I refer to a core solution-technique relevant to a wide class of problems.
<br/><br/>
If there is a problem with a unique (or rare) solution that isn't translatable to other similar cases - then I'd NOT consider it as a _Pattern_.
<br/>
<br/>
Although there is no well-defined algorithm that given a challenge, could say if its solutions consist of common techniques or not - 
I'd still try my best to argue there is place for having that category. Please bear with me. 
<br/>
<br/>
So instead of writing: _"Challenges having common solutions that can be reused in many places"_ - I'd stick with the term a _Pattern_.
<br/>
I'm also aware that what one would view as a _Pattern_, another person wouldn't - and that's totaly fine.
<br/>
<br/>
What's important is that anyone will be able to possess his own classification and decide if he regards it as a _Pattern_ (or not).
<br/>

Since it's an individual discernment - here are a few examples of stuff I'd call _Patterns_:

* Math
<br/>
 - _Prove that √2 is an irrational number._
<br/><br/>
Why a _Pattern_? - The classic solution to the above is prove by contradiction. 
We assume there exists two natural numbers 𝜨 and 𝜧  having no common divisors such that 𝜨 / M = √2
<br/>
Building on top of this this - we'll eventually reach a dead-end to the assumption that 𝜨 and 𝜧  have no common divisors.
<br/>
([click here for the full proof][root-2-proof]).
<br/><br/>
I see it as a _Pattern_ since I can imagine many Math problems that would require me to use a similar technique as we did here with 𝜨 and 𝜧 .

* Chess 
<br/>
 - _Given the following board position - how Black can win in 1 move?_
<br/><br/>
![chess-puzzle-image][chess-puzzle-image]
<br/>
<br/>
Why a _Pattern_? - The solution to to this challege is pretty easy (you can try to solve it [here][chess-puzzle]).
I'd call it a _Pattern_ since there are tons of similar chess challenges that will require using the same way of thinking. 

* Reading Code
<br/>
 - _Given high-quality logging library source code having 3K LOC - understand its inner workings_
<br/><br/>
Why a _Pattern_? - Well, that's a bit obscure. Understanding a self-contained code-base such as a logging library
entails a couple of things I'd categorize as _Pattern_. While thoroughly reading such infrastructure library 
you should expect to come across things such as:
<br/>
		* buffering: a common technique is to collect some log-entries in-memory before flushing it to disk / sending it via a socket or similar.
		* multi-threading: if the library internals can be accessed simultaneously from multiple-threads, we can see how the library 
		  protects critical sections and shared resources. Maybe it'll also have some threads in charge of deleting stale data 
		  (for example log entries that are buffered for too long). Or, flushing data might involve transfering of data into some background thread.
		* log-rotations: if we persist data to a file - we may need logic that will remove old data. Similary, if we limit each file for 10MB,
	      the code will have to prune the eldest entries or do something else (like saving new data to new file).
		* formatting: if the library expects structed-logs it might have code for formatting structs to strings.
		* parsing: for raw data, we might have parsers that will validate it and transform it to some structured shape.
		* compile-time macros: in case we're compiling for production we'd like to omit tracing code.
		* fault tolerance: Robust logging mechanism should guard against burst of logging. It'll use rate-limits of number of calls/sec. 
		  If the logging is to a remote machine, it may have wrap the calls with a circuit-breaker.
		  circuit-breaker, rate limit, memory limit)
		* tests: it's always a good place to learn how to use the library's API and get ideas.
		  <br/>
		  _How the library simulates logging failure?_ 
		  <br/>
		  _Maybe it'll use fuzzy-tests for detecting an edge-case bug._

<br/>
![patterns-image][patterns-image]
<br/><br/>
Our brain is very good at recognizing patterns. Given an image, it'll detect objects in a fraction of a second. 
<br/><br/>
_Math enthusiasts_ are able to receive a Math challenge and at once think of a few solving strategies that should be 
tackled and eliminate a couple of others. That's because they have years of accumulated problem-solving knowledge.
<br/><br/>
_Profesional Chess players_ looking at a game board will instantly infer a lot about it, weight trade-offs and have a gut feeling what are the best
options for next moves. That's owing to years of playing and encountering innumerous situtations.
<br/><br/>
_Experienced developers_ can start reading a high-quality codebase consisting of a few thousand lines of code and after a short while figure out 
their way through it. Then, they can deduce what regions lack structure and require more refactoring, suggest architectural changes,
and have a mental model of the code inside the head.
They can do that since they've read and written tons of code.
<br/><br/>
The more we'll feed our brains with varied inputs - the larger our toolbox will expand.
It means we could solve not only more problems but also more elegantly (and faster) since we'll have more choices to choose from.
<br/><br/>
## How to Train?

![brain-image][brain-image]

So... how to _TYONT_?
<br/>
Again, let's split it again into _Factual-data_ and _Patterns_.
<br/>
### _Factual-data_ Training:
In order to _TYONT_ with facts, you first need to decide what you kind of information we want to remember. 
You may want to extend your vocabulary, learn a new language, remember quotes and list goes and on.
My advice is to start with one or two topics as most.
<br/>
Then you should use the [Spaced-repetition][spaced-repetition] technique
in order to optimize what to study and when. This will assist you with remembering the most in less time and retain it better. 
<br/>
<br/>
I think it's a shame that most people aren't familiar with Spaced-repetition. It's so powerful and rewarding. 
I highly recommend using [anki][anki] for applying it. You can think about it as your agent that throws at you flash-cards with questions
and asks you to answer them. In order to make it as effective as you can, you're encouraged to create your own cards. 
It will assist with remembering the data most effectively.
<br/>
<br/>
In case you want to expand your vocabulary - [Super-Memo][supermemo] is the best Spaced-repetition resource I know of. 
Not only it asks you a question - after you ask to review the answer, it will pronounce it.
Additionally, The app offers synonyms to the desired answer - another major advantage of this app.
<br/>
<br/>
Spaced-repetition can be super-effective for programmers as well. A classic use-case is making flashcards for keyboard shortcuts or shell commands.
Another good usage is having flashcards for Syntax. It's true that we have _Google_ and _Stackoverflow_ and great IDEs extensions with auto-complete
and such. However, if you find yourself looking yet again for a standard-library function that you did already twice over the past week - 
it might be a good indiciation to walk the extra mile and try saving the next hop to _Google_.
<br/>
<br/>
I personally strive to know I'm able to open a text editor having no plugins and just start coding.
Don't get me wrong here - we are paid to solve problems not memorize stuff that can be picked up easily.
I'm suggesting that we're able to streamline common stuff that we repeatedly do. It's up to anyone to pin-point what's 
the stuff that seems to slow him down. 
<br/>
<br/>
Moreover, I'd argue that most devlopers are using a single dominant programming-language in at-least 80% of their time and a handful of keyboard shortcuts 
(or worse - using the mouse). Imagine the ROI boost of being fulent with syntax or shortcuts you're using repeatedly on a daily basis.
The real benefit won't be the time-savings - it'll be the context-switches reduction.
You'll find yourself much less wandering and consequently staying in focus.
<br/>
<br/>
Now that we've covered the Spaced-repetition based training -  we're left with the _Patterns Training_.
<br/>
### Patterns Training
The answer to how to _TYONT_ using _Patterns Training_ is unsurprisingly less obvious.
It's true that we can create flashcards for math riddles in a few cases, 
or take a Chess board and turn it into a flashcard. That'll be feasible, but not always - life isn't that simple.
<br/>
<br/>
For example, let's return to reading source code. 
Flashcards won't assist programmers here (maybe in learning keyboard-shortcuts for code navigation). 
The path to getting better at such a skill should be to tailor it to your own needs.
One idea can be commiting to reading 1000 lines-of-code of a GitHub project on a daily basis. 
That will surely make us somewhat better at reading code.
<br/>
<br/>
But we can _TYONT_ better. Let's instead be more specific. Say that we want to improve code understanding of a specific domain that interests us.
We could look for famous GitHub Open-Source projects in that domain. It's preferable that code be written a in programming-languages we know.
Then we can pick one or two projects and start reading them. 
<br/>
After managing to walk through 1-2 similar projects, the 3rd one will become easier to grasp. 
It's important to see code written byb different great developers. Programming is a craft and there's always 
more than a single valid way to do stuff. Code projects associated with the same domain, will usually have some overlap.
It could be shared terminology, similar domain abstractions for representing things.
<br/>
Sometimes the same problem could be tackled in a completely different ways - this is very educating to see completly other ways
of approaching the same problem. For example, one could solve a programming challenge of [Advent of Code][aoc] and then read a variety of solutions.
Further than that, reading solutiosn coded in different programming-language can assist with developing more mental models (i.e: _Patterns_).
Thinking in more pradigms is necessity in order to get better (both in writing but also in reading code).
<br/>
And of course - while reading high-quality code and planting more Patterns seeds inside our brain, we get to learn how to do thing with style.
It means how to write more idiomatic code, structing the code-base, naming things better and more.
<br/>
<br/>
As a side-note: learning from others is one of the best ways to get better.
<br/>
Whether its going over a Math challenges solution in a book, reading other people's code,
having a real-person mentor that you can ask questions and similar - All these are super effective.
<br/>
This piece attempts to raise the awareness around the _TYONT_ technique.
</br>
Its effectiveness doesn't get the place it deserves right now.
</br>
The article by no means argues that anyone can be good at math, a professional chess player,
a world-class musician or a top-notch developer. 
You still need to have some talent, passion, persistence and doing many other things in order to achieve greatness.
</br></br>
In the past a Math enthusiast could buy mostly the Math books available in his local-store.
Maybe in some circumstances he could grab a book overseas - But how he would be familiar with the existing books? (There was no internet).
Today, a Math enthusiast can go to _Amazon_ or similar and order any existing book.
If there is an online content in a foreign language - he can use translator.
</br></br>
In the past if you wanted to be good at Chess you'd need access to good teachers.
Today, you can just go to [chess.com][chess-com] or a similar website and play for free 
against millions of people or try solving some chess challenges.
</br></br>
Programmers in the past couldn't use Open-Source in their work, let alone read code by people outside.
Today, anyone has access to billions of lines of code.
</br></br>
Thanks to the internet - we have access to an infinite volume of information.
</br>
One of the byproducts is that learning from others has never been easier. 
</br>
You can _TYONT_ and accomplish more than you think you can and as a bonus have fun too.
</br></br>
Let's Train Our Own Neural Network! 😉


<br/>
### Related Links:
* [Expertise is ‘Just’ Pattern Matching][expertise-is-just-pattern-matching]
* [Spaced repetition][spaced-repetition]
* [Ultralearning Environments: Why Where You Learn Determines How Much You Learn][ultralearning-environments]
* [Thesaurus][thesaurus]
* [SuperMemo.com - Learn fast and forget about forgetting][supermemo]
* [Execute Program - Learn programming tools fast. Then remember them][executeprogram]

[brain-image]: images/brain.png
[flashcards-image]: images/flashcards.png
[patterns-image]: images/patterns.png
[chess-puzzle-image]: images/chess-puzzle.png

[spaced-repetition]: https://en.wikipedia.org/wiki/Spaced_repetition
[churchill-quotes]: https://www.keepinspiring.me/winston-churchill-quotes/
[ultralearning-environments]: https://www.scotthyoung.com/blog/2019/01/03/ultralearning-environments/
[expertise-is-just-pattern-matching]: https://commoncog.com/blog/expertise-is-just-pattern-matching/
[supermemo]: https://www.supermemo.com/
[thesaurus]: https://www.thesaurus.com/
[anki]: https://apps.ankiweb.net/ 
[executeprogram]: https://www.executeprogram.com/
[chess-puzzle]: https://chesspuzzle.net/Puzzle/49337
[chess-com]: http://chess.com/
[root-2-proof]: https://www.homeschoolmath.net/teaching/proof_square_root_2_irrational.php
[aoc]: https://adventofcode.com/
