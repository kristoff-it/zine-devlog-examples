# Zine Devlog Examples
A few examples of how to setup a Devlog with Zine.

Read the blog post: [Critical Social Infrastructure for the Zig Community](https://kristoff.it/blog/critical-social-infrastructure/)


## The examples 
This repository contains three examples of how to setup a devlog with Zine.
The most notable thing about this approach is that by using a page as an
append only log, you can generate an RSS feed that has an entry for every 
heading you add to your page. 

The three examples differ in the following manner:

- `simple/` shows the most basic setup: easy but infinitely growing.
- `rolling/` shows a setup where old entries are forgotten. This example uses
  a fixed number of entries as a cut-off, but other implementations could decide
  on age or other constraints (Zine might need to gain a couple more builtin functions
  for certain usecases, if you encounter limitations in Zine reach out and I'll
  try to unblock you).
- `archive/` shows a setup where, by pre-sharding by year, you can easily archive
  old entries to avoid creating an endlessly growing page without losing content.

## Usage

Enter the directory of the example you want to inspect and run `zig build` to see 
what the example compiles to. The output will be located under `zig-out/`.

Note that the build script is provided for convenience only, to create a proper 
Zine website I recommend checking out the more complete documentation available 
at https://zine-ssg.io.

It is also recommended to put your devlog under `/devlog/` if possible. If 
you're using the term devlog for something else already, feel free to do as you
see fit. Just pointing this out as the examples put the devlog under `/index.html`
for convenience.

Note that if you have already an exising website, with its own static generation
logic, you could consider temporarily integrating with Zine only for the purpose 
of generating the devlog page (and feed), in which case the end result would look
very similar to what this repo is doing.

Lastly, take a look at the following websites for more examples:

- https://github.com/ziglang/www.ziglang.org ([devlog](https://ziglang.org/devlog/2024/))
- https://github.com/kristoff-it/zine-ssg.io ([devlog](https://zine-ssg.io/log/))

These last examples might be interesting because they will show you how to setup
RSS entry titles depending on your neeeds, which is someting that ultimately depends
on what you want to make most convenient for you.
