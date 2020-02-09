---
title: "Vim and Emacs can be BFF"
date: 2020-02-07T17:00:00+02:00
tags: ["productivity"]
type: "post"
---

## Short History

The year was 1976.
<br/>The two most gigantic IDEs the universe has ever known sprang into existence.
Subsequently, one of history's most ruthless wars has started.

On one side stood vi (succeeded later by vim) -</br> a small and agile text-editor based on modal-editing.
<br/>
<br/>
On the other side of the battlefield stood emacs -</br> a tall and stout operating-system having a feeble text-editor (some argue it had no text-editor at all...). 

Who will ascend the throne and be the best IDE that has ever lived?

The years have passed, and new wanna-be "the best IDE" rivals were born.
A partial list contains names you may have heard of such as SublimeText, Atom, VSCode and, IntelliJ.

They tried everything to get some traction. Trying to mimic elements of these the two giants was without substantial success.

vim and emacs stayed in a league of their own and started to accept they are both here to stay and that no one will be pronounced a winner. 
Hatred has slowly (but steadily) declined and been substituted with mutual-respect. 
Each party recognized the strengths of the other.

Although there is no surviving evidence today, the two started to like each other.
It was all a matter of time until some official significant collaboration will occur. 
<br/>
<br/>
## My turning point

I've been a vim user for a couple of years and as much as I loved (and still do) vim, its extensibility has always bothered me.
Traditionally vim plugins were written in Vimscript, which is notoriously known for being an inelegant language.

I've never found a good excuse to go and learn it. It just didn't feel fun (more like half-backed cake).
The community plugins creators seemed concentrated around a small number of people, and I believe that VimScript is one of the primary reasons for that.

Additionally, vim has been maintained by a single person - Bram Moolenaar.
In a past interview, he has been asked 
_"How can the community ensure that the Vim project succeeds for the foreseeable future?"_ - and he answered with _"Keep me alive."_

That attitude over the years was the trigger for a few people to fork vim in 2014 and start a big rewrite under the name [neovim][neovim].
Its motivations were mainly to improve code quality, add async capabilities to the infrastructure and isolate the core from the UI.
Having such isolation would yield us client-server architecture for the plugins system. New plugins could be coded in other programming-languages
since they will talk in RPC to the vim-core.

That seemed very promising but instead, the community has been polarized into vim and neovim users.
Instead of joining forces, there are now plugins targeted only for one editor. Other plugins target both, sometimes at the expense of increased maintenance.
Things may worsen in the feature as each editor roadmap will steer into different directions. 

The above propelled me to go and research whether I should pick vim or neovim for the long-term or maybe check other options?
Any decent IDE has some basic vim emulation extension. I was especially curious to dig what vim over emacs looked like.

emacs has a very popular vim emulation named [**evil**][evil] (branded as **The extensible vi layer for Emacs**).
I was skeptical at first but gave it a try, and surprisingly things went smooth.
It really felt like using vim inside emacs without actually really knowing emacs.
The more I played with it, I got convinced that I'd like to make the switch into emacs backed by evil.
Instead of choosing vim vs neovim, I've resolved that emacs is what I was looking for.

In parallel, I've researched more about emacs and its extensibility features which are its forte.
emacs is being extended by a lisp dialect called emacs-lisp, or elisp for short.
Leveraging lisp for writing some code was very appealing too. 
Reading about "the emacs way" of doing things using keymaps, commands, buffers, regions, modes, hooks just clicked. It just felt right.
But with all due respect emacs, without having evil I'd never considered moving to emacs.
vim modal-editing is just invincible. 
<br/>
<br/>
## Making the switch

Recently, I've finally made this transition. So far I'm very pleased with this change. I've learned the basics of emacs-lisp by solving a few [vimgolf][vimgolf] puzzles
in emacs-lisp ([repository link][vimgolf.el]) and reading documentation.

My emacs configuration is pretty minimal right now as I'm still making my first steps
but I expect it to grow over time ([repository link][dotemacs]).
<br/>
<br/>

**Today, I don't see vim and emacs as enemies anymore.** 
<br/>**I believe that each one can learn from the other.**
<br/>**I actually think that vim and emacs can be BFF.**

![bff-image][bff-image]


[evil]: https://github.com/emacs-evil/evil
[dotemacs]: https://github.com/YaronWittenstein/dotemacs
[vimgolf]: http://www.vimgolf.com/
[vimgolf.el]: https://github.com/YaronWittenstein/vimgolf.el
[neovim]: https://neovim.io/
[bff-image]: images/bff.png 
