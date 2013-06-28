---
layout: post
title: "Upgrade Complete"
description: "Well, that didn't take long."
category: Improvements
tags: [yard chef yard-chef documentation best-practices ]
---

Okay, today is the day that I somehow got cookbook attributes into yard-chef.
The results are very interesting.  For starters, I now have reasonably
accurate statistics about how many "things" in my Chef repo are documented.
The number is _shockingly_ low, of course.  But now that I can generate
documentation and docstring coverage stats, I can graph it and shame people
into writing documentation.  Best of all, today I tested publishing a
documentation site using GitHub Pages (for Enterprise!) and it works well
enough that I don't think it will be necessary to muck about with emitting
markdown.

Cookbook (AKA Node) Attributes are listed in the upper-right of the yard
documentation site and searchable.  If you choose to document a whole Chef
repository's worth of cookbooks, you'll see all the node attributes in one
place and clicking on any of them will zoom you to the appropriate cookbook
page to view its docstring _and_ the source file / line, just as if you
had defined a new Ruby class method.

I really think this is going to be a great way for people to document their
cookbooks (particularly those who have experience in "proper" Ruby 
development).  It also makes it possible for somebody (say, Opscode) 
to set up a community yard-chef doc server that does for cookbooks 
what rubydoc.info does for Ruby gem documentation.

"So, Steve, where's the code?" you ask.  Ah.  Well.  It belongs to my
employers.  I'm getting approval to release it back to the community
now.  I hope to have an update on that soon.

{% include JB/setup %}
