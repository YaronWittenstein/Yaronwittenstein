---
title: "Vim and Emacs can be BFF"
date: 2020-02-07T09:46:44+02:00
tags: ["productivity"]
type: "post"
draft: true
---

## Short History

The year was 1976.
<br/>The two most gigantic text-editors the universe has ever known sprang into existence.
Subsequently, one of history's most ruthless wars has started.

On one side stood vi (succeeded later by vim) -</br> a small and agile text-editor based on modal-editing.
<br/>
<br/>
On the other side of the battlefield stood emacs -</br> a tall and stout operating-system having a feeble text-editor (some argue it had no text-editor at all...). 

Who will ascend the throne and be the best text-editor has ever lived?

The years have passed, and new wanna-be text-editors rivals were born.
<br/>
A partial list contain names you may have heard of such as: SublimeText, Atom, VSCode and IntelliJ.

They tried everything to get some traction, but vim and emacs stayed in a league of their own.
Desperately, they started mimicing elements of these two, without much success.

vim and emacs started to accept they are both here to stay and that no one will be pronounced a winner. 
Hatred has slowly (but steadily) declined and been substituted with mutual-respect.
Each party recognized the strengths of the other. 

Although there are no surviving evidences today, the two started to like each other.
It was all a matter of time until some official collaboration will occur. 
<br/>
## My turning point

I've been a vim user for a couple of years and as much as I loved (and still do) vim, its extensibility has always bothered me.
Vim plugins are written in Vimscript, which is notoriously known for being an inelegant language.

I've never found a good excuse to go and learn it. It just didn't feel fun.
The community plugins creators is pretty concentrated around a small number of people. 
I believe that VimScript is one of the primary reasons for that.
</br>
Additionally, vim has been maintained by a single person - Bram Moolenaar. On a past interview, he has been asked 
_"How can the community ensure that the Vim project succeeds for the foreseeable future?"_ and his answer was _"Keep me alive."_

That attitude was the trigger for a few people to fork vim in 2014 and start a big rewrite under the name [neovim][neovim].
Its motivations were mainly to improve code quality, add async capabilities to the infrastructure and isloate the core from the UI.
That isolation, will yield us client-server architecture for the plugins system. New plugins could be coded in other programming-langages
since they will will talk in RPC to the vim-core.

That seemed very promising but instead the community has been polarized into vim and neovim users.
Instead of joining forces, there are now plugins targeted only for one editor. Other plugins target both, sometimes at the expense of increased maintenance.
Things may worsen in the feature as each editor roadmap will steer into different directions. 

The above made me reserach whether I should be on vim or neovim for the long-term.
In parallel, I've researched more about emacs and its exensiblity features which is famous for.
emacs is being extended by a lisp dialect called emacs-lisp, or elisp for short.
Using lisp for writing a bit of code was very appealing. Not only it looks beautiful (way more than VimScript) but emacs itself is super extensible.
The concepts of keymaps, commands, buffers, regions, modes, hooks just clicked. It just felt right.
But with all due respect for the above, vim modal-editing is invincible.

emacs has a very popular vim emulation called `evil` (branded as `The extensible vi layer for Emacs`).
I was skeptical at first, but gave it a try. And it was surprisingly very smooth, like using vim inside emacs without really knowing emacs.
The more I played with it and the more research I've done into emacs plugins I got convinced that I'd like to make the switch into emacs backed by evil.
Instead of choosing vim vs neovim, I've decided to learn elisp so that I'll have more control over my IDE.

## Making the switch

Recently, I've finally made this transition. So far I'm very pleased with this change. I've learned the basics of emacs-lisp by solving a few vimgolf puzzles
in emacs-lisp ([repository link][vimgolf.el]) and reading documentation. My emacs configuration is pretty minimal right now as I'm still making my first steps
but I expect it to grow over time ([repository link][dotemacs]).


Today, I don't see vim and emacs as enemies anymore. 
<br/>I belive that each one can learn from the other.
<br/>
### I actually think that vim and emacs can be BFF.

![bff-image][bff-image]


[bff]: https://en.wikipedia.org/wiki/Best_friends_forever
[dotemacs]: https://github.com/YaronWittenstein/dotemacs
[vimgolf.el]: https://github.com/YaronWittenstein/vimgolf.el
[neovim]: https://neovim.io/
[bff-image]: images/bff.png 
