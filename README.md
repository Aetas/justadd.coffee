# justadd.coffee
My website experiment.

At present this is just a quick Bootstrap template.  
I'm using Bootstrap over something like Angular because you don't even need a brain to start with it (I mean that as a compliment) and I don't care much for web development. (no offense to web people)

I don't know what I want the end product to look like as of writing this so it will probably take longer than it needs to.

Yeah, I need to do a lot of research on how to categorize pages/elements in Bootstrap. The whole "do it right the first time" thing is probably the worst when it comes to coding. Still important but to a point.

So much CSS in every flavor. This was also originally made for one page sites, unlike what I'm doing with it.

I should really deploy a local host to test things on. Maybe I would spend more time playing with it if I didn't have to push things live.  
^ That was a good idea. Unsurprisingly.

**Now** I really need to update my images file structure. Probably by category or tag.

One thing that would benefit me greatly would be adding a tag to display featured thumbnail images above posts.  
Unlike the type: photo tag, I would be able to set it separate from the featured/bg image. Many preview images would look like shit as a background/wrapper. I'll have to figure out how to do that. Still, shouldn't be hard. Maybe after I've gotten some things up and I don't feel like I'm hosting someone else's work.

## Next up:
Convert to multi-page layout. Might actually switch to a different layout in general. Probs a better idea. I'd need to learn Jekyll or Ghost or some such though.  
Which would be both easier and more boring.

Yeah, I don't think I'm going to do Ghost/etc. No blog-like layout (who needs interaction anyway?) but a portfolio-style post.

Update:  
~~Looks like I might just go with Drupal. It's going to take a bit of reading-up though. I'm itching to do Trusty Rusty Rows as well.~~

I double-dog lied. I'm actually ditching Drupal and really any real/feature-complete CMS framework for a lovely jekyll outline that Michael Rose made and I shall adapt.  
Reasons for skipping CMS Town:  
1. My hoster is not that great for Drupal. It's reputedly slow. Sure my website is the smallest thing ever but that only makes the decision easier. Why do I need a whole goddamn blog management system to keep track of like, 5 pages. 'Compile' to static sites? Yes please.
2. Compiler. I just like compiling things. Sure they're kinda assholes but they're also super cool. And it's not a real compiler, it's pretty much just an interpreter.
3. Speed. Because you gotta go fast, I don't care if you can 'afford the tradeoffs' or 'the internet runs on string algorithms, you can't win with scripting languages anyways.' Using a compiler feels like victory and dammit I'm going to type `bundle exec jekyll install` and appreciate everyone else's hard work.
4. The dev space is very flexible and typically is no further than a `yum install ruby jekyll && gem install bundle` if they are not already installed. CMS platforms are kinda a pain.
5. Lots of support. Sure there are more supported things in this world but I'm not looking for much here. Yay templates and people who like javascript who aren't me!

Misfortunes (I'm sure this list will grow as I learn):
1. Page syntax is Markdown. Great for some things, far too simple for others and I'm not quite sure how to hack together a html page and guarantee that it plays nice with all the sass/less/js.
2. That's all for now.


## License
The MIT License (MIT)

Copyright (c) 2016 Derek Prince

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
