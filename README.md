# Django Examples
This is a series of examples on best practices and anti-patterns when working with Django. 

> Apologies for any grammar and/or spelling mistakes. As English is my first language they’re hard to avoid.

## Import Information
Some of the examples that I’ll be writing here are explicitly anti-patterns. Please, please, please double check to ensure that you understand what is on the screen before simply copy and pasting it into your code.

## Ancillary Applications
I’ll be using a number of other applications in some of these examples. Most of these are predicated on working within a POSIX environment.

As time allows, I will attempt to help any Windows folks along. But be aware that everything presented here is done so from a Linux first point-of-view. The application code *should* be agnostic. But some of the debugging and other utilities may not have Windows analogs.

## Contents

My intention is to have this be a shallow dive into the wonderful world of Django. As such, I will **not** be documenting every aspect of, what I consider to be, secondary aspects of a web application. This includes the transportation layer, database backends, load balancing, and other, more production-y sorts of details.

What I would like to get across is showing (and heavily documenting) some of the things you can do with this framework and some of the more notable extensions.

## Setup

Most folks will eventually create a setup unique to them. This is great. I continually see and hear questions like, "Which IDE is best?". The answer is, whichever one lets you code most efficiently. Same with the debug tools. And the versioning tools. And the CI/CD tools. And…you get the picture. 

I’ll briefly go over *my* particular setup. All of the code in this repository *should* be setup agnostic. 

### Development
* Terminal emulator: [Alacritty](https://github.com/alacritty/alacritty)
* Text editor: [Neovim](https://neovim.io/)
* Python Shell: [iPython](https://ipython.org/)
* Package Management: [pip](https://pypi.org/project/pip/)

### Debugging
* Python debugger(s): [pudb](https://pypi.org/project/pudb/) and
  [ipdb](https://pypi.org/project/ipdb/)
* Traffic analyses: [mitmproxy]
* API debugging: [insomnia

### Devops
* PubSub server: [mosquitto]
* Container engine: [Docker]
