---
layout: page
title: latex-y tips
permalink: /resources/typescript/
---

I stopped using Word documents for various reasons, one of them is to have consistent pieces of writings. As page number increases, the amount of time I spend on correcting layout in Word increases exponentially. LaTeX provided me a lot of tools to create easy pipelines (and also a lot of problems to procrastinate.) I believe the graph below describes what I can say in pages quite easily.

<center>
<img src="../../images/latex-word.jpeg" alt="latex vs word complexity" width="400"/>
</center>

Right now, I mainly use a combination of R, markdown, yaml, and LaTeX to write my documents. I can easily integrate my code and my results without the hastle of copy-paste. Still though, if I am collaborating, I either only use Google Docs or LaTeX.

As for IDE, I mainly use VScode. I use Rstudio only if I need to show other people what they need to do. Even though I love VScode, I would not recommend anyone who does not have spare time to ditch Rstudio. However, when I am working with Stan, LaTeX, MD, R, python, Rmd, files together, VScode is way superior than Rstudio. I plan to share step-by-step migration from Rstudio to VScode in the future.

In this page, I share my resources/templates in scientific reporting and typescriting. I will mainly use overleaf links.

## LaTeX

**First steps**: This [tutorial by overleaf](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)) was perfect for me. It took me from complete beginner to somewhat able to create certain documents. It is not perfect, but it will put many things to their right places. After you complete all three courses here, you should be able to create a basic document in LaTeX with citations, items, graphics. After this point, it will come own to what you want to do and what resources you can find online. Another [good tutorial](https://ptmartins.info/latex/) is prepared by Pedro Tiago Martins.

**Intermediary steps**: I believe this step is where you want to familiarize yourself with packages and what they can do for you. I will mainly talk about linguistic-related packages. Packages are set of function and macros that will help you do fancy stuff like, trees, tables, ordered linguistic examples, which otherwise would require a lot more energy. Actually, the main reason I started using LaTeX was to be able draw better trees.

I used a lot of _tree-drawing_ packages. The best, in my opinion, is the <span class="foc">forest</span>. This [tutorial by Guido Vanden Wyngaerd](http://tug.ctan.org/info/forest-quickstart/forest-quickstart.pdf) is awesome. It shows many examples of quite different set of trees, and they are all accompanied by their code. Still, to this day, I open this tutorial and check it quite often. I advise using this standalone program called [jsSyntaxTree](http://www.ironcreek.net/syntaxtree/) to practice tree drawing. For more advanced trees, I really like [this tutorial by Antonio Machicao y Priemer](https://www.linguistik.hu-berlin.de/de/staff/amyp/latex20sfb/07-l4l-math2-trees-handout.pdf). It has extremely cool trees and tricks that you can use with forest package.

Then there is the question of _interlinear glossing_. LaTeX has solved many problems and headaches related to numbering and aligning when it comes to linguistic examples. It might be the main reason, I still do not use markdown completely and fall back to LaTeX. Nothing does it better than LaTeX, for sure. I mainly use two packages: <span class="foc">langsci-gb4e</span> or <span class="foc">linguex</span>. If I am doing something fast-paced ad have results quickly, I use linguex. It is easy to introduce to any environment, it does not have many dependency conflicts you can just write ```\usepackage{linguex}``` in the preamble and start using it. Its syntax is also very straightforward. [This documentation by Wolfgang Sternefeld](http://mirror.ox.ac.uk/sites/ctan.org/macros/latex/contrib/linguex/doc/linguex-doc.pdf) is quite useful.

However, if I am preparing a document for a submission, term-paper, or in general if I want to have more control, I use langsci-gb4e. It has many functionalities already included in it, and to me, customizing langsci-gb4e code is easier. [This documentation by Sebastian Nordhoff](https://ctan.mines-albi.fr/macros/xetex/latex/langsci/documentation/langsci-gb4.pdf) summarizes what you can do with langsci-gb4e quite concisely. One thing that is important with langsci-gb4e, you cannot just slap ```\usepackage{langsci-gb4e}``` in your document. First, you need to put ```langsci-gb4e.sty``` file in your working environment, which you can download [here](https://ctan.org/pkg/langsci?lang=en). For these reasons, I generally advise people to use linguex. It is easier to get into it. There are also many people using it, so finding answers to you questions are a lot easier.

When it comes to _semantics_ or _logic_, I am not very picky. The package called <span class="foc">stmaryrd</span> does everything I want. [This webpage](https://www1.essex.ac.uk/linguistics/external/clmt/latex4ling/semantics/) gives basic usage of it. I also have [this file that includes math symbols]("../../images/mathmode_latex.pdf") bookmarked, I originally found in on Michael T. Putnam's website.

When it comes to _phonology_ or _phonetic symbols_, there is no replacement for <span class="foc">tipa</span> package. It is very easy to use: put ```\usepackage{tipa}``` in your preamble and then you can introduce phonetic typescripting via ```\textipa{}``` command. [Package documentation](https://www.tug.org/tugboat/tb17-2/tb51rei.pdf) is great, and I frequently use it. However, I mainly check this [cheatsheet]("../../tipacheatsheet.pdf") that I found in  Pedro Tiago Martins' website. I usually use additional commands that I introduced for narrow and wide transcripts: ```\newcommand{\nt}[1]{\textipa{[#1]}}``` and ```\newcommand{\wt}[1]{\textipa{/#1/}}```.

I rarely type _tables_ by hand. There are many websites that can generate tables, but I use [this specific website](https://www.tablesgenerator.com) that I found ages ago. I also try to have tables printed automatically via R code using Rpackages like kable or kableExtra.
