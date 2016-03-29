---
layout: post
title:  Try with Markdown
categories: Note
tags: Eng
---
{% include base.html %}
I'm trying with the markdown
============================

And comes the h2
----------------

Here are just random words i'm writing which doesn't make sense.

Actually I heard about [MarkDown](https://daringball.net/ "Daring") All the time. So here is the tricky point, I was told [Zhihu][zhihu] is just a copy of [Quora][quora], which I can't believe!! How can [Zhihu][zhihu] be another [Tecent][tecent]!!!

Here I put a Zhihu's logo.![z logo][zlogo]

Now i'll try some `code` completion, they `&say;` this kinda things will work, COOL! It really `&#34` worked.
{% highlight matlab %}
x = extrema(3:5:end);
y = extrema(4:5:end);
rx = x./ 2.^ (octave - 1 - extrema(1:5:end));
ry = y./ 2.^ (octave - 1 - extrema(1:5:end));
figure(2);
imshow(origin);
hold on
plot(ry,rx,'r+');
{% endhighlight %}

# at all 

> I'm a big fan of Maugham,
> the first time I read his <i>Moon and Six Pence</i>
> I think it was just a masterpiece
> Allright I knew he was no 
> 
> ### Master
> but he really got tallent on telling stories.

As for the emphasis, it's quite *easy*. 
Well, the _underline_ can work as well.

If you want a really string one, use **two asterisks**, or just two __underlines__.

List, I do like list.

*  Why is 
*  Paniikii
*  So fuking Kold.
-  Anwser 
-  is that
-  windows' so thin!!!
+ is + working?

1. oh my spaghtii
2. it worked

	and how about tab?

3. I was told avoid it always!!!

And now it's the end.    

Great thanks for Markdown, Jekyll and Github. I have my own website, finally.	

[zhihu]: http://www.zhihu.com/  "A"
[quora]: http://www.quora.com/ "B"
[tecent]: http://www.qq.com/ "C"
[zlogo]: {{base}}/assets/zhihu-logo.png "Zhihu"
