---
title: "Markdown Test"
date: 2018-03-21T19:03:09+05:30
tags: [ "golang",  "markdown", "test2"]
tags_weight: 1
---

## Markdown Plus

Markdown Plus ("M+" or "mdp" for short) is a markdown editor with extra features.


## Apps

We currently ***don't*** accept donations.
The best way to support our development is to buy our apps.

### Markdown Mate

<a href="/"><img src="/images/logo.png" width="100px"/></a>
[Markdown Mate](/images/logo.png) is a markdown previewer, it's not going to replace your favorite editor but handles everything about markdown.

# Table of Contents

[toc]

Note: Only `h2` and `h3` are shown in toc.

## Mastering Markdown

Markdown allows you to write using an easy-to-read, easy-to-write plain text format, which then converts to valid HTML for viewing.

[Mastering Markdown Guide](https://guides.github.com/features/mastering-markdown/).


## ~~strikethrough~~


## ++insert++


## ==mark==


## Subscript: H~2~O

You can also use inline math: `$H_2O$`


## Superscript: 29^th^

You can also use inline math: `$29^{th}$`


## Emoji: :panda_face: :sparkles: :camel: :boom: :pig:

[Emoji Cheat Sheet](http://www.emoji-cheat-sheet.com/)


## Fontawesome: :fa-cab: :fa-flag: :fa-bicycle: :fa-leaf: :fa-heart:

[All the Font Awesome icons](http://fontawesome.io/icons/)


## `print 'hello code'`

    evens = [1, 2, 3, 4, 5].collect do |item|
      item * 2
    end

{{< highlight javascript "style=monokailight,linenos=table" >}}
$(document).ready(() => {
  $('pre code').each((i, block) => {
    hljs.highlightBlock(block);
  });
});
{{< /highlight >}}

[Code Formatting](https://help.github.com/articles/markdown-basics/#code-formatting)


## Tables and alignment

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |

[Table Syntax](https://help.github.com/articles/github-flavored-markdown/#tables)


## Task list

- [ ] a bigger project
  - [x] first subtask
  - [x] follow up subtask
  - [ ] final subtask
- [ ] a separate task

[Task List Syntax](https://help.github.com/articles/writing-on-github/#task-lists)


## Abbreviation

Markup is based on [php markdown extra](https://michelf.ca/projects/php-markdown/extra/#abbr) definition, but without multiline support:

*[HTML]: Hyper Text Markup Language
*[W3C]:  World Wide Web Consortium
The HTML specification
is maintained by the W3C.


## Footnote

Here is a footnote reference,[^1] and another.[^longnote]

[^1]: Here is the footnote.

[^longnote]: Here's one with multiple blocks.

    Subsequent paragraphs are indented to show that they
belong to the previous footnote.


Here is an inline note.^[Inlines notes are easier to write, since
you don't have to pick an identifier and move down to type the
note.]

[Footnote Syntax](http://pandoc.org/README.html#footnotes)


## Mathematical formula `$y = x^2$`

Inline math: `$\dfrac{ \tfrac{1}{2}[1-(\tfrac{1}{2})^n] }{ 1-\tfrac{1}{2} } = s_n$`.

Math block:

```katex
\oint_C x^3\, dx + 4y^2\, dy

2 = \left(
 \frac{\left(3-x\right) \times 2}{3-x}
 \right)

\sum_{m=1}^\infty\sum_{n=1}^\infty\frac{m^2\,n}
 {3^m\left(m\,3^n+n\,3^m\right)}

\phi_n(\kappa) =
 \frac{1}{4\pi^2\kappa^2} \int_0^\infty
 \frac{\sin(\kappa R)}{\kappa R}
 \frac{\partial}{\partial R}
 \left[R^2\frac{\partial D_n(R)}{\partial R}\right]\,dR
```

[Mathematical Formula Syntax](http://meta.wikimedia.org/wiki/Help:Displaying_a_formula)


## AsciiMath

Inline AsciiMath: `@(1/2[1-(1/2)^n])/(1-(1/2))=s_n@`

```AsciiMath
oint_Cx^3 dx+4y^2 dy

2=(((3-x)xx2)/(3-x))

sum_(m=1)^oosum_(n=1)^oo(m^2 n)/(3^m(m3^n+n3^m)
```

```ASCIIMath
phi_n(kappa) = 1/(4pi^2 kappa^2)
 int_0^oo (sin(kappa R))/(kappa R)
 del/(del R)
[R^2 (del D_n (R))/(del R)] del R
```

[AsciiMath Documentation](http://asciimath.org/)


## mermaid charts

### Flowchart

```mermaid
graph TD
A[Christmas] -->|Get money| B(Go shopping)
B --> C{Let me think}
C -->|One| D[Laptop]
C -->|Two| E[iPhone]
C -->|Three| F[Car]
```

[Flowchart Syntax](http://knsv.github.io/mermaid/#flowcharts-basic-syntax)

::: warning
Adding many flowcharts will slow down the editor.
:::

### Sequence diagram

```mermaid
sequenceDiagram
loop every day
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
end
```

[Sequence Diagram Syntax](http://knsv.github.io/mermaid/#sequence-diagrams)

::: warning
Adding many sequence diagrams will slow down the editor.
:::

### Gantt diagram

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d

section Critical tasks
Completed task in the critical line :crit, done, 2014-01-06,24h
Implement parser and jison          :crit, done, after des1, 2d
Create tests for parser             :crit, active, 3d
Future task in critical line        :crit, 5d
Create tests for renderer           :2d
Add to mermaid                      :1d

section Documentation
Describe gantt syntax               :active, a1, after des1, 3d
Add gantt diagram to demo page      :after a1  , 20h
Add another diagram to demo page    :doc1, after a1  , 48h

section Last section
Describe gantt syntax               :after doc1, 3d
Add gantt diagram to demo page      : 20h
Add another diagram to demo page    : 48h
```

[Gantt Diagram Syntax](http://knsv.github.io/mermaid/#gant-diagrams)

::: warning
Adding many gantt diagrams will slow down the editor.
:::

### Class diagram

```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

Class diagram is powered by [mermaid](https://github.com/knsv/mermaid).

::: warning
Adding many class diagrams will slow down the editor.
:::


## Custom Container

Markup is similar to fenced code blocks. Valid container types are `success`, `info`, `warning` and `danger`.

::: info
You have new mail.
:::

::: danger
Staying up all night is bad for health.
:::


## Definition list

Term 1
  ~ Definition 1

Term 2
  ~ Definition 2a
  ~ Definition 2b
