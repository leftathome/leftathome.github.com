---
layout: post
title: "yard should generate markdown"
description: "It's just easier."
category: Improvements
tags: [chef, ruby, yard, yard-chef ]
---

I love documentation.  But I hate writing it.  I sense I'm not alone in this, based on the many excellent doc-generation projects
that have been built up over the years.  Perldoc blew my mind the first time I saw it, but that was nothing compared to what I
found when I got to ILM and saw how thoroughly they had embraced pydoc in their extensive internal Python codebase.  You could
basically "pydoc <any script or module>" and get a reasonable amount of documentation.  The fact that you can also generate an
entire searchable/navigable documentation site in a browser was also really cool.  When I started coding in Ruby, I wasn't
surprised to see that similar tools existed.

So, it makes sense to me that the place to document one's code is in the code itself.

Which is why it drives me up the damn wall when I look at how Chef cookbooks are currently documented.  A Markdown-formatted
README and that's it?  I haven't seen anybody truly solve this yet, though it seems the community is trying a few things --
knife plugins that create documentation scaffolding and such.  The problem with this approach is that it's still keeping the
code separate from the documentation.

That's why I was jazzed to find Rightscale's yard-chef plugin.  It extends Yard so that it understands the Chef DSL.  This
means you get documentation coverage statistics for your Chef codebase _for free!_  As the guy who's in charge of maintaining
a bunch of central Chef cookbooks for a large internal organization, that made me happy.

Currently we have three places to look for documentation:
 * The GitHub Enterprise page for the cookbook (i.e. the README.md).
 * The code itself.
 * A Confluence wiki.

Obviously, I'm writing a blog in Jekyll, so you can imagine my feelings towards Confluence.  Clearly the ideal here would be
to get yard to generate a wiki and push it to GitHub Enterprise for that repository.

Which means yard (and specifically yard-chef) needs to support not just Markdown but _GitHub-flavored Markdown_ as an output
format.  The Google says that some people have inquired into this before, but that no one is working on this right now ... 
or, at least, if they are, they're not talking.

So I'm going to give it a whirl.  With luck, I'll be able to open-source my efforts.

{% include JB/setup %}
