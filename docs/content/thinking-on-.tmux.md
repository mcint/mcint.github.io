Title: Thinking on tmux configuration - composable vs redefined configs
Date: 2022-09-08 15:58:31
Category: thinking dotfiles cli tools tmux config

Tools you use every day extend your thinking.  If you build on well-factored
tools, you gain great power.  If you build on convoluted tools, you may one day
find yourself mired in a mess.

`tmux` provides a mostly clear set of interface elements and predictable
interactions.  It's often worth configuring to get the best use of it.

## opinionated .tmux

https://github.com/gpakosz/.tmux (hereafter, dot-tmux) offers an opinionated
setup, so opinionated in fact, that you have to learn it's own Domain-Specific
Language (DSL) to manage its configuration of tmux.  As someone who continually
refines my use of tools, I think this approach is wrong.

Configuration, programming, can be done in a few ways.

Composition or configuration.

tmux offers an expressive configuration format, allowing functions and
transformations
 
Writing a language over the top of this which allows configuration through new
specially named variables as well as through direct native setting leads to
confusion.  It requires a much deeper understanding of the configuration system
to predict the effect of simple changes.  Without learning a lot more, on par
with some level of rewriting a custom config system, I find myself mired in a
mess.

The new configuration layer runs some of its changes initially, and some of its
changes after reading in the end-user config file.

I was tempted by the promise of easily available, powerful configuration
options. However, opinionated choices and an obscurring, verbose DSL in the
configuation layer make otherwise easy changes unpredictable.

Framework vs library. 


### Exploring justifications

#### Composition versus configuration.

Perhaps I experience that good configuration systems allow expression of a
"composition" of "behaviors" (nouns) of the system.

```
do behavior-1
don't-do behavior-2
```


- "Convention over configuration"
- "Convention over code"

#### Framework vs library tmux configuration, raw `.tmux.conf`, has the flavor
of a library to me. Many options are directly available.

dot-tmux has the flavor of a framework. It controls how to set most of tmux's
configuration, and clashes with options you can still set directly.


It seems possible to me that a hypothetical lib-conf-tmux could present an
opinionated set of options, that could be called before manually setting your
own overrides to the chosen opinioned defaults.
