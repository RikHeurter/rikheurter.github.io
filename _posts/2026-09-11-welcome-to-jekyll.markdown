---
layout: post
title:  Starting the preparation of the thesis
date:   2026-09-11
categories: General weekly review
---

So for whomever is reading this page. This is my very first web page on which I will be recording my progress of my masterthesis and whatever problems I run into. I am specifically putting this on this web page with 3 different reasons:
 - I noticed during the writing of my bachelor thesis that it is rather nice to actually always inform my supervisors what I have been working on (I did it via e-mail that year);
 - This time I might be working together with supervisor, but possibly also other researchers. Thus in order to also inform them on what I have been working on.
 - To have a nice way to read back on what I had worked on at specific points, so that I can possibly show during the presentation of my master thesis what I was working on at what time. 
I will probably regret this decision later on, but for now it is more than a little nice to just jot down my (non-intrusive) thoughts. 

Anyway this week I have mostly started reading [this](https://leanprover.zulipchat.com/#narrow/channel/508986-Quantum-information/topic/Quantum.20Computing.3A.20Organizing.20the.20community/with/619559617) thread on the lean zulipchat and of course setting up this thesis.

It was already nice to know that there are a bunch of people now that are interested in formalising some form of quantum computing algorithms in Lean and importantly, that this is also not a trivial task to do in a nice way: The trade-off between the most general case of infinite dimensional circuits versus the specific case of finite dimensional circuits is apparently big enough that it isn't completely clear what the best choice here is.

Similarly it is to a certain extent sad that there is still no proper direction chosen on where, and how, to formalise quantum algorithm. Specifically to what extend we will try and put theorems "upstream" in physlib/mathlib versus in CSlib, which if I understand it correctly seems to be the home where we will actually work on the specific algorithms.

Also reading through some of the posts in the thread it was interesting to see that probably the best way to write these algorithms is using monads, just like is the "natural" way of writing stateful functional programming languages (which Lean belongs to). This was something I did expect, but still to see it in action is fun to say the least.

To end, after having written my first blogpost let's get to talking about writing my thesis, or more aptly what boundaries I think I will set for myself. At first I wanted to look into using agentic AI to formalise theorems, but the longer I am considering that the more I am thinking that I will probably not like that. Compared to my bachelor thesis wherein (probably to my detriment) I did not use AI in anyway whatsoever, I will at least plan on using on the UvA's AIChat. Mostly to look up how to do x,y or z in Lean which I didn't yet know about. I think I am very much at the stage of learning LEAN that using LLMs for look up is moreso to get introduced to new methods to improve/shorten my LEAN code than letting the computer solve the problems for me [^1]. It will be sad to leave my AI-free hermit life after me though :'(.
---

[^1]: At the very least I hope so. In my bachelor thesis' code I wrote down wayyyy too many `apply?` to get possibly further + using the creation of a lot of short rewrite hypothesis and then using simp. At least after having learned `show_term` I now know how to already clean up a lot of this code.



<!---You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
--->
