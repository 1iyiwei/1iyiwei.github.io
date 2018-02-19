# Program committee statistics #

Jump to the bottom for a short, visual explanation.

## from Aaron Hertzmann ##

For those of you who’ve been on conference program committees, you know how sometimes you have a “good batch” of papers, or a “bad batch”? The CVPR 2018 program chairs sent out this nice little bit of statistical analysis to the ACs:

Folks,

1) As you work through your batches of papers, here's some
stuff to keep in mind.  Some ACs will have weird batches of
papers. This note to work a sum to give you some sense of
how those batches are distributed.

2) I'll use rough numbers in every case, and approximate
like crazy. We have 3300 submissions.  The usual accept rate
is about 25%  (often rather lower, but small details in the
number don't make much difference).  This doesn't mean
that, in your pool, 25% of the papers should get in.  Here's why:

  - you get a random sample of (say) 30 from a population of
     3300

  - assume each paper has a hidden 0 or 1 (reject/accept).
     The population mean is 0.25 (i.e. 25% get in).

  - the mean in your sample is a random variable, whose mean is
          0.25,     but whose variance is (0.25*0.75)/30

  - the usual stuff about normal distributions, binomial approx,
    etc. yields:

          about 70 AC's have accept rates between .17 and .33
           about 12 AC's have accept rates from .33 to .41
           about 12 AC's have accept rates from .08 to .17
           a few AC's have accept rates greater than .41 OR less than 0.08

3) This is rough stuff, because your sample isn't random, etc. etc.
Also, it isn't a license to run wild.  But it does mean that under
reasonable rough models, some ACs are pretty much guaranteed
rather strange pools.  The effects won’t change much if you
change the accept rate within reasonable ranges, too.  If you're fairly sure your pool is odd, there's no need to be rattled.

4) We'll keep track of statistics like this and keep ACs up
to date during the meeting.  We'll also be watching to support
ACs with odd pools so we and they are really sure the
pool (rather than the AC) is odd

## a simpler and less formal explanation ##


A truly random distribution would be like a white noise:
<a href="http://datagenetics.com/blog/february52018/index.html">
<img src="http://datagenetics.com/blog/february52018/random.png">
</a>
i.e. image black dots are good papers and while regions are bad papers, and the 2D domains are the paper ids.

As a committee member, you are assigned a random sub-window of the domain.
If you shift the window around, you will get clumps of clusters or voids.

If you expect a "reasonable" distribution for all committee members, you are talking about a blue noise:
<a href="http://datagenetics.com/blog/february52018/index.html">
<img src="http://datagenetics.com/blog/february52018/udl.png">
</a>
