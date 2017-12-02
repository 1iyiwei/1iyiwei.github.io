---
layout: post
comments: true
title: "Revision control source text lines"
---

When writing a document in a formatted syntax (e.g. Latex or Markdown) with revision control (e.g. git or svn), it is better to avoid (1) artificial line breaks in the middle of the sentences and (2) putting an entire paragraph in one line.

I usually keep one full sentence at one line, such as:
<blockquote>
A variety of applications such as virtual reality and immersive cinema require high image quality, low rendering latency, and consistent depth cues.
<br>
4D light field displays support focus accommodation, but are more costly to render than 2D images, resulting in higher latency.
<br>
The human visual system can resolve higher spatial frequencies in the fovea than in the periphery.
<br>
This property has been harnessed by recent 2D foveated rendering methods to reduce computation cost while maintaining perceptual quality.
<br>
Inspired by this, we present foveated 4D light fields by investigating their effects on 3D depth perception.
<br>
Based on our psychophysical experiments and theoretical analysis on visual and display bandwidths, we formulate a content-adaptive importance model in the 4D ray space.
<br>
We verify our method by building a prototype light field display that can render only 16%-30% rays without compromising perceptual quality.
</blockquote>

<!--
(You might need to look at the md source to see the difference.)
-->

If I violate (1) above and break lines in the middle of the sentences, it could confuse automatic spell checkers such as MS Word:

<blockquote>
A variety of applications such as virtual reality 
<br>
and immersive cinema require high image quality, low 
<br>
rendering latency, and consistent depth cues. 4D light
<br>
field displays support focus accommodation, but are more 
<br>
costly to render than 2D images, resulting in higher 
<br>
latency. The human visual system can resolve higher spatial
<br>
frequencies in the fovea than in the periphery. This property
<br>
has been harnessed by recent 2D foveated rendering methods
<br>
to reduce computation cost while maintaining perceptual
<br>
quality. Inspired by this, we present foveated 4D light
<br>
fields by investigating their effects on 3D depth perception.
<br>
Based on our psychophysical experiments and theoretical
<br>
analysis on visual and display bandwidths, we formulate a
<br>
content-adaptive importance model in the 4D ray space. We
<br>
verify our method by building a prototype light field 
<br>
display that can render only 16%-30% rays without compromising
<br>
perceptual quality.
</blockquote>

If I violate (2) above and put all sentences in one line, it could confuse line-based revision tools such as git or svn.
For example, if we just change one word, git/svn will think you change the entire paragraph, making it very hard to see the actual difference:
<blockquote>
A variety of applications such as virtual reality and immersive cinema require high image quality, low rendering latency, and consistent depth cues. 4D light field displays support focus accommodation, but are more costly to render than 2D images, resulting in higher latency. The human visual system can resolve higher spatial frequencies in the fovea than in the periphery. This property has been harnessed by recent 2D foveated rendering methods to reduce computation cost while maintaining perceptual quality. Inspired by this, we present foveated 4D light fields by investigating their effects on 3D depth perception. Based on our psychophysical experiments and theoretical analysis on visual and display bandwidths, we formulate a content-adaptive importance model in the 4D ray space. We verify our method by building a prototype light field display that can render only 16%-30% rays without compromising perceptual quality.
</blockquote>
