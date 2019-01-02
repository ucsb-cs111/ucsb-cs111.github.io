---
topic: "LaTeX: MathJax"
desc: "LaTeX on webpages"
category_prefix: "LaTeX: "
indent: true
---

MathJaX allows a subset of LaTeX expressions to be incorporated into web pages,
as in this example:

When $$a \ne 0$$, there are two solutions to $$ ax^2 + bx + c = 0 $$
and they are $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

The source code for that paragraph looks like this:

```
When $$a \ne 0$$, there are two solutions to $$ ax^2 + bx + c = 0 $$
and they are $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
```

Information about MathJAX is here:
* <https://www.mathjax.org/>

What enables MathJAX on this web page is this line in `_config.yml`

```
head_scripts:
  - https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML
```

If you need to make adjustments to the configuration of MathJAX, you can adjust that line,
and or add your own custom JavaScript in a particular webpage.