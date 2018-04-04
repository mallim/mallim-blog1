---
title: "How to use pandoc to generate a letter from a markdown?"
comments: true
tags:
  - pandoc
  - markdown
  - latex
  - letter
---

Really lazy to use Microsoft Word to write something. So I proceed to try pandoc with Miktex installed on Windows.

Finally, got what I need and I have to start to think how to write the letter...

<!--more-->

### Try 2

> https://github.com/mrzool/letter-boilerplate

### Try 3 

> https://github.com/aaronwolen/pandoc-letter

### Try 4 

> [Pandoc Letter Template (DIN 5008)](https://github.com/benedictdudel/pandoc-letter-din5008)

**Try 4** looks the best so far. And if you want to align everything to left, just need to do the following:

Command

```dos
pandoc --template=letter.latex example\letter.md -o output.pdf  
```

From 

```latex
\documentclass[
    foldmarks=true,      % print foldmarks
    foldmarks=BTm,       % show foldmarks top, middle, bottom
    fromalign=right,     % letter head on the right
    fromphone,           % show phone number
    fromemail,           % show email
    fromlogo,            % show logo in letter head
    version=last        % latest version of KOMA letter
]{scrlttr2}
```

To 

```latex
\documentclass[
    foldmarks=true,      % print foldmarks
    foldmarks=BTm,       % show foldmarks top, middle, bottom
    fromalign=left,     % letter head on the right
    fromphone,           % show phone number
    fromemail,           % show email
    fromlogo,            % show logo in letter head
    version=last,        % latest version of KOMA letter
	refline=dateleft     % aligns both the city and the date to the left
]{scrlttr2}
```

