# wastes-of-time

A collection of things that I think/know/suspect are wastes of time for one reason or another.

If something is not on this list either it was just too obvious that it's a waste of time so there
was no real question about it, or I haven't formulated any real thoughts on it yet. Most likely
it's the former.

Even though it should be obvious: These are just random thoughts and musings. If you take anything
here as fact I feel bad for you. Feel free to take it as the valid and honest opinion it's intended
to be.

## NixOS

I used NixOS once upon a time. Incredibly neat to roll back installations and have declarative
configuration, but it's a massive time sink [for me] in practice. If I were to manage many boxes
I might look into it for that, and it's possible that I'll revisit it in the future, but it's
looking like a waste of time for me right now.

## `nix`

I've used `nix` many times (meaning I've started using it, then stopped). It's, much like NixOS,
very neat in some ways but has always ended up being just additional headaches for me. `guix` is
probably better overall because a massive part of why `nix` is a time sink is actually the
horrendous language and how terrible it actually feels to use/debug and learn.

## Rust

I think Rust is likely a waste of time for most things and for most people, mostly because there
are usually better alternatives that are (likely) easier to use, learn, debug and have people be
productive in: Odin, Zig, and Go. The list could be made longer if I had used more of the offerings
in the spaces that overlap with Rust's use cases. Back in 2017 I was very excited about Rust but I
don't think it's hard to see for anyone who's been paying attention to reality that it keeps losing
in actual use cases to other languages on different axes:

- It often produces slower software than Zig. Not because of the compiler but because software
  written in Rust is much harder to make obviously fast than software written in Zig (or Odin
  since it has almost exactly the same concepts in this regard).
- It's much, much harder to use than Go and will still oftentimes actually lose out to Go in terms
  of performance, which is big. Go is a "weekend language" for the right user profile, much like
  Odin and Zig, meaning that getting up to speed with it is a weekend matter, not several months.
- The absolutely cringy community is both hilarious and just sad. With that said, community is
  overrated and absolutely does not matter for being actually productive in most cases. Long-term
  productivity doesn't come from `npm`-style communities, it comes from being able to build the
  right things and being able to actually comprehend and debug the results.


With all of the above said, Rust is absolutely the language I should've loved and used and probably
advocated for like an annoying fanboy, but somewhere along the way I started valuing actual results
over ideas/concepts/theory and Rust is a whole lot more of the latter than the former.

## Effects as types

I *suspect* that effects as types are a solution to a problem most people aren't actually having.
I don't know this for sure, but for some time now I've been under the suspicion that because there
are a few key examples where you can tell someone "Look, here is a situation where we actually can
say that this **could** be a potential problem and we can guarantee that it doesn't happen if we
express our effects in types" we get an easy pass to imply that it is an overall good idea and a
win for the software development process.

## Functional programming as a paradigm

I think that functional programming is a waste of time as a guiding light in development. There are
small key parts of it that absolutely make sense to apply in some cases, but in terms of paradigms
that are key to a language, environment or platform I don't think there is much to be gained from
focusing very heavily on it.

I have used functional programming in 6+ languages over a period of 12+ years so this is not
some idle thought I've had at a distance, but rather something I've had to face when I realized
back in ~2019 that procedural code is much easier to read, understand and change than functional
code (in practice). I happen to (most of the time) be very good at functional programming, I know my
way around it and I've used it to great effect, but I think there's something fundamentally broken
about having to "know your way around it" in the first place. Procedural code generally speaking
doesn't have this type of barrier and so it makes for easier learning, more productive usage
overall in my experience.

Now, without overreaching, I think that the above applies to whole lot more people than just me, and
I think it applies to a lot of people who would be very hesitant to even acknowledge it, or maybe
even know about it themselves.

## Haskell

It should maybe be clearer, but this one is actually just an incling... Maybe Haskell is a waste of
time? I love it, but there is no denying that it's hard to learn for people and that there is a
"hair-shirt" vibe where you're in some sense dealing with the language and its ideas more than you
are dealing with the actual problem you're trying to solve. Haskell is at its best when you're
actually just dealing with a nice `ReaderT env IO` stack and you're even mutating values and using
handles from that `env`. The more you buy into the caricature of "purity over everything" that
people think is a real thing the worse it gets.

With that said, Haskell has too many things in common with everything else on the list to not be
mentioned. At least it's not Rust, though.

Also, lest anyone get the wrong impression, OCaml isn't even in the conversation with its barren
runtime and absolute lack of good tools to use in the language. `STM`, lighweight threads, etc.
are way beyond what OCaml has to offer. I'd honestly rather use F# than OCaml for pretty much any
project, so Haskell being a maybe on this list is not some indication that OCaml would ever be
relevant. You might say OCaml is such a massive waste of time it's not even on the list (like OOP).

## Most of Elixir

Elixir isn't the absolute win that people think it is and I'm prepared to say that it's probably
overall a waste of time over Erlang. The good parts are all just Erlang and usually they come with
a bad makeover that obfuscates what is actually going on. Erlang is much, much easier to learn, use
and understand than Elixir. `mix` is great, some of the configuration stuff is legitimately nice and
I like the testing bits, but most of the libraries are written badly by people who lost their way a
long time ago (Phoenix comes to mind) and have ended up encouraging macro madness for no good
reason.

As an aside Erlang was supposed to get something out of all of this but if you look at it critically
certainly the library bits aren't nearly as much of a win as people think they are. Phoenix isn't
usable outside of Elixir, Ecto isn't usable outside of it. If you look at the ecosystem more and
more you realize that there really isn't that much of a win to these libraries existing outside of
the Elixir bubble.

I'm prepared to say that going with Erlang over Elixir could save you manyears in the long-term in
training, development and maintenance. You might have a harder time hiring people and maybe you're
running a stupid startup that needs mega growth, but maybe in that case you should just use Go
instead. That way you can get popularity and productivity instead of hipster hype.

## Macros

Think Lisp macros, not C macros. At this point I'm almost certain that macros are overall a net loss
in even small teams and that the problems that they're supposed to solve are better solved in
extreme cases with external code generation (actually good tooling) or just writing more, normal
code. In my head there is an idealized hypothetical team of 5 amazing and motivated programmers who
can move mountains with Common Lisp having very little macro discipline and certainly this is
reflected at least somewhere in the world outside of this hypothetical... But I'm not sure that
team couldn't produce the same or more (and maybe better) results with a much more restricted
toolset over time.

I realize that I'm advocating for a mega-boring language and toolset here, but while I honestly love
the kind of power that you can get with macros (Scheme/Racket, etc.) I don't think it's
realistically even a net win for only myself, let alone a team.

Have fun, though; I would never argue for having less fun as a lifestyle in the name of discipline.
There are better uses of your time than "being pragmatic and reasonable" in your free time if you
actually just like using things that people argue are not those.

P.S. If you just hired/contracted a team of 5 Common Lisp programmers who love Common Lisp and want
to use all of it, don't tell them they can't use whatever they want. You're just wasting morale and
you'd be an idiot to waste this opportunity to get tons of free productivity (from happiness) out of
a motivated team. Even worse, forcing them to use your stupid JVM stack or whatever is going to be
a painful experience for everyone involved.

## Kitchen sink languages

There is a certain type of language creator or community that seems determined to put everything
under the sun into their language. Things are accumulated and appended to the language either to add
new possibilities or to fix problems created by some previously added thing. The result is a messy
and almost unlearnable language that has more features than anyone should be forced to learn and
certainly more than anyone should be using even across multiple projects.

If you come across a language known for (or being obviously) a kitchen sink language I think you
should turn around. It is almost certainly a waste of time to use it.

Some languages are of course already established and have lots of users, lots of support out there
and so on; C++ comes to mind. Learning C++ is perhaps *not* a waste of time. Some languages push
through a critical barrier of popularity and seem to succeed despite their obvious kitchen sink
nature. Seeing one that doesn't fit either previous criteria, it's very hard to not consider it a
waste of time.
