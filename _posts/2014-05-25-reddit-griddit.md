---
layout: post
permalink: reddit-is-flawed
title:  "Reddit is Flawed - My Attempt at Fixing it"
date:   2014-05-25 00:17:00
description: "Reddit's voting based system works for only a part of the site. Reddit favors captions and titles over the images themseves. I attempted to fix that."
tags: [programming, reddit]
image:
  feature: rcats.jpg
comments: true
---

This isn't a post about [Reddit's flawed algorithm](http://technotes.iangreenleaf.com/posts/2013-12-09-reddits-empire-is-built-on-a-flawed-algorithm.html). This is a post about a fundamental flaw that affects most of the 2.5 million redditors and has been there since the site started.

![](http://i.imgur.com/8D2H0RB.jpg?2)

As it is right now, Reddit favors text more than any other form of content. Even for image-based subreddits (like r/cats, r/pics), the primary emphasis is on the submission title or caption and not on the image itself. All you see if a small thumbnail of the image itself. Most of the times, a crappy image wil hit the frontpage based on a clever title. **That is the flaw** - judging an image based on its title.

As such, it isn't very hard to garner tons of karma with almost no effort:

1. Choose an image-based subreddit with a lot of activity
2. Browse through a few pages on the "hot" page of the subreddit. Keep note of what people seem to like
3. Find an image that is slightly relevant to the topic of the subreddit
4. Think of a caption for the image. Doesn't have to be accurate but must contain keywords from step 2.

Bingo! Watch as the holy river of karma flows in.

But wait, there's more: The basic principles of web design suggest that to give value to your user, consuming the content should be obvious to the user. The current design of Reddit forces the user to click an extra link to consume the primary content of a subreddit. No UX book would ever, ever, ever recommend this.

### So what should happen? How can this be fixed?

I think it's not something that the community can fix by themselves - it's a problem with the platform. Reddit is inherently built to be a platform to support discussions about a central topic. This, however, doesn't hold true so much for images. People should upvote an image (memes, gifs) if they like it. There's hardly ever any scope for some meaningful discussion there.

So here's what I suggest: strip everything from image-based subreddits but the images themselves. I took some time to [prototype](http://karan.github.io/griddit) this:

[![](https://raw.githubusercontent.com/karan/griddit/gh-pages/screen.jpg)](http://karan.github.io/griddit)

The basic idea is the same - share pictures. Currently, the app pulls images from the subreddit you search for, and displays them in a more pleasant and user-friendly way.

Some things I'd like you to notice:

1. It's content first - there's no fillers, no crap. Only the content that the user want to consume.
2. The emphasis here is on the images and not on the title or the user who submitted them.
3. If the user likes the image, they can click through to the thread and have a discussion there.

Now obviosuly this isn't a perfect prototype. What's missing is:

1. No upvoting. I think it's important to have voting feature embedded in each image block. I didn't do this because this add more complexity than I wanted to have in a weekend project.
2. Performance issues. Imagine loading 20 high resolution images at the same time. On an average system, your browser would crap its pants. I've done some stuff to make *griddit* very efficient and fast, but obviously there's more that can be done.
3. No support for albums for now.

## Conclusion

*griddit* is my vision of what image-based subreddits should look like. It's not perfect. It's not the best solution either. If you don't agree with me, or have feedback about *griddit*, please leave a comment below.

If you think you agree with me, please consider sharing this post. Spread the word.

![](http://i.imgur.com/I6bLwbh.jpg)
