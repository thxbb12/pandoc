---
author: Florent Gluck - Florent.Gluck@hesge.ch
title: Pandoc Slide Examples
subtitle: This is a subtitle
date: \vspace{.5cm} \footnotesize \today
institute: \vspace{0.5cm} \tiny \textsuperscript{*}Many thanks to Prof. Ada Gavrilovska for letting me use some of the contents of her course "Introduction to Operating Systems" tought at Georgia Institut of Technology

# Latex colors listing: http://latexcolor.com/

pandoc-latex-fontsize:
  - classes: [tiny]
    size: tiny
  - classes: [verysmall]
    size: scriptsize
  - classes: [small]
    size: footnotesize
  - classes: [huge, important]
    size: huge
---

[//]: # ----------------------------------------------------------------
# Part 1

[//]: # ----------------------------------------------------------------
## Text styles

- **bold text**, *italic text*, `non proportional text`
- bold  \textbf{Sample Text 0123}
- upright \textup{Sample Text 0123}
- fixed  \texttt{Sample Text 0123}
- italic  \textit{Sample Text 0123}
- slanted \textsl{Sample Text 0123}
- small caps  \textsc{Sample Text 0123}
- bold and fixed  \texttt{\textbf{Sample Text 0123}}
- ~~this text is striked through~~
- Some \underline{underlined text}

[//]: # ----------------------------------------------------------------
## Text colors and alert

\small

- \textcolor{myred}{myred}
- \textcolor{myblue}{myblue MidnightBlue}
- \textcolor{myorange}{myorange Bittersweet}
- \textcolor{mygreen}{mygreen OliveGreen}
- \textcolor{mylightgreen}{mylightgreen YellowGreen}
- \textcolor{myyellow}{myyellow Goldenrod}
- \textcolor{myviolet}{myviolet Periwinkle}
- \textcolor{mypurple}{mypurple Orchid}
- \textcolor{mylightorange}{mylightorange Orange}
- \textcolor{mypink}{mypink Thistle}
- \textcolor{Red}{Red}, \textcolor{red}{red}, \textcolor{blue}{blue}, \textcolor{green}{green}

\vfill

### \alert{this is an alert!}

[//]: # ----------------------------------------------------------------
## Font sizes (1)

::: smallcontent :::
This is tiny content
::::::::::::::::::::

This is normal content, [small content]{latex-fontsize=small} and `huge code`{.huge .important}.

~~~tiny
And a piece of tiny code.
~~~

Font sizes:
```{.small}
\fontsize{6}{6}
\tiny
\scriptsize
\footnotesize
\small
\normalsize
\large
\Large
\LARGE
\huge
\Huge
```

[//]: # ----------------------------------------------------------------
## Justifying

Default ....\
blah blah

\center
A `center` paragraph

blah blah

\flushright

A `flushright` paragraph

blah blah

\centering
A `centering` paragraph

blah blah

\flushleft

A `flushleft` paragraph

[//]: # ----------------------------------------------------------------
## Vertical space with `vspace`

Blah blah blah... Blah blah blah...
Blah blah blah... Blah blah blah...

\vspace{2cm}

Blah blah blah... Blah blah blah...
Blah blah blah... Blah blah blah...

[//]: # ----------------------------------------------------------------
## Vertical space with `vfill`

There are 2 method types:

* **instance methods** 
  * linked to an object
* **static methods** or **class methods**
  * linked to the class
  * they don't require the object to be instanciated

\vfill

```{.java .numberLines .small}
String test = "hello";
test.toUpperCase();
String.valueOf(1234);
```

[//]: # ----------------------------------------------------------------
## Same as previous slide, but without `vfill`

There are 2 method types:

* **instance methods** 
  * linked to an object
* **static methods** or **class methods**
  * linked to the class
  * they don't require the object to be instanciated

```{.java .numberLines .small}
String test = "hello";
test.toUpperCase();
String.valueOf(1234);
```

[//]: # ----------------------------------------------------------------
# Part 2

[//]: # ----------------------------------------------------------------
## Bullet list

- Computer systems are **incredibly complex**
	- Hardware: transistors, chips, processors, buses, disks, network cards, GPUs, etc.
	- Software: operating systems, device drivers, compilers, libraries, applications, etc.	
- How to *manage* such complexity?
	- Through the division into levels of abstraction separated by well-defined interfaces

[//]: # ----------------------------------------------------------------
## Numbered list

1. Computer systems are **incredibly complex**
	1. Hardware: transistors, chips, processors, buses, disks, network cards, GPUs, etc.
	1. Software: operating systems, device drivers, compilers, libraries, applications, etc.	
1. How to *manage* such complexity?
	- Through the division into levels of abstraction separated by well-defined interfaces

[//]: # ----------------------------------------------------------------
## Incremental List (1)

::: incremental

Benefits of VMs:

- Single application containers --- reliability, isolation, security
- Mixed OS environments (legacy apps)
- Multi-platform application development
- Software testing and debugging
- Version transitioning

:::

[//]: # ----------------------------------------------------------------
## Incremental List (2)

Benefits of VMs:

>- Single application containers --- reliability, isolation, security
>- Mixed OS environments (legacy apps)
>- Multi-platform application development
>- Software testing and debugging
>- Version transitioning

[//]: # ----------------------------------------------------------------
## Source Code

C code:

```{.c .small .numberLines startFrom="1"}
#include <stdio.h>
#include <stdlib.h>

// Entry point
int main(int argc, char **argv) {
	int a = 10, b = 4, x = 128, y = 256;
	char car2 = (char)y;

	printf("super longue ligne pour voir comment se comporte cette daube de pandoc et beamer !!!! %d\n%d\n", car1, car2);

	return EXIT_SUCCESS;
}
```

[//]: # ----------------------------------------------------------------
## Source Code inside item list

- Pipes are powerful
- Example:
  ```{.small}
  count=`find . -type f|wc -l`
  echo "File count: $count"
  }
  ```

[//]: # ----------------------------------------------------------------
## Table (1)

\footnotesize
`docker-compose <cmd>` where `cmd` can be:

Command   Description
--------- ------------------------------------------------------
 `up`     Create and start containers (= pull + create + start)
 `down`   Stop and remove containers, networks, images, and vol.
 `ps`     List containers
 `logs`   View output (logs) from containers
 `pull`   Pulls service images
 `create` Create services
 `start`  Start services
 `stop`   Stop services
 `rm`     Remove stopped containers
 `build`  Build or rebuild services
 `help`   Get help on a command

[//]: # ----------------------------------------------------------------
## Table (2)

\footnotesize
`docker-compose <cmd>` where `cmd` can be:

-------- ---------------------------------------------------------
`up`     Create and start containers (= pull + create + start)
`down`   Stop and remove containers, networks, images, and vol.
`ps`     List containers
`logs`   View output (logs) from containers
`pull`   Pulls service images
`create` Create services
`start`  Start services
`stop`   Stop services
`rm`     Remove stopped containers
`build`  Build or rebuild services
`help`   Get help on a command
-------- ---------------------------------------------------------

[//]: # ----------------------------------------------------------------
## Table (3)

| ~~Default~~ | *left*  | **Center** | `Right`  |
|---------|:------|:------:|-------:|
|   High  | Cat 1 | A      | 100.00 |
|   High  | Cat 2 | B      |  85.50 |
|   Low   | Cat 3 | C      |  80.00 |

[//]: # ----------------------------------------------------------------
## Table with horizontal lines using LaTeX (4)

\begin{tabular}{|l|l|l|l|l|}
\hline
\textbf{Header1} & \textbf{Header2} & \textbf{Header3} & \textbf{Header4} & \textbf{Header5} \\
\hline
& & & & \\
pipo & molo & gato & blah & \\
& & & & \\
\hline
& & & & \\
& 3651 & 7821 & 9415 & 64157 \\
& & & & \\
\hline
& & & & \\
& humf & gargl & groumf & 42 \\
& & & & \\
\hline
\end{tabular}

[//]: # ----------------------------------------------------------------
## Image

\centering
![](images/01-IBM_System_370.png){ }

[//]: # ----------------------------------------------------------------
## Image with scaling
	
\centering
![](images/01-IBM_System_370.png){ width=50% }

[//]: # ----------------------------------------------------------------
## Image shifted left

\begin{center}
\hspace*{-30mm}\includegraphics[width=12cm]{images/01-IBM_System_370.png}
\end{center}

[//]: # ----------------------------------------------------------------
# Part 3

[//]: # ----------------------------------------------------------------
## Two columns

:::::: {.columns}
::: {.column width="50%"}

- **Column 1**
	- memory, user-level instr., system calls for OS functions
	- OS interface to hardware defnes view of process

:::
::: {.column width="50%"}

- **Column 2**
	- hardware characteristics
	- defnes system view

:::
::::::

[//]: # ----------------------------------------------------------------
## Footnote

Definitions[^1]:

- A **virtual machine** is an abstraction of a complete compute environment through the combined virtualization of the processor, memory, and I/O components of a computer.
- A **hypervisor** is a specialized piece of system software that manages and runs virtual machines.
- A **virtual machine monitor (VMM)** refers to the part of the hypervisor that focuses on CPU and memory virtualization

[^1]: from the book "Hardware and Software Support for Virtualization"

[//]: # ----------------------------------------------------------------
## Blocks (1/2)

- The block below **cannot** span multiple lines:

\vspace{.2cm}

\definecolor{palechestnut}{rgb}{0.87, 0.68, 0.69}
\setlength{\fboxsep}{6pt}
\fcolorbox{black}{palechestnut!50}{\textbf{Calling conventions} = Protocol defining how to call a routine}

\vspace{.7cm}

- However, this block **can**:

\vspace{.2cm}

\definecolor{palechestnut}{rgb}{0.87, 0.68, 0.69}
\setlength{\fboxsep}{6pt}
\fcolorbox{black}{palechestnut!50}{\parbox{10cm}{If we want our box to span multiples lines, \textbf{the solution is to use parbox} with a specified size (length), here 10cm}}

[//]: # ----------------------------------------------------------------
## Blocks (2/2)

\metroset{block=fill}
\begin{block}{Definition}
\textbf{Calling conventions} = Protocol defining how to call a routine\

This box can span multiples lines by default which is more convenient than the example in the previous slide...
\end{block}

\vspace{.3cm}

- This is not part of the block
- Neither is this

\vspace{.5cm}

\metroset{block=fill}
\begin{block}{Calling conventions \textnormal{= Protocol defining how to call a routine}}
\end{block}


[//]: # ----------------------------------------------------------------
## Special characters

\small

- tilde: $\sim$
- approximation: $\approx$
- power: $2^n$
- greater or equal: $\geq$
- not equal: $\neq$
- right arrow: $\rightarrow$
- thicker right arrow: $\Rightarrow$
- left arrow: $\leftarrow$
- longright arrow: $\longrightarrow$
- longleft arrow: $\longleftarrow$
- leftright arrow: $\leftrightarrow$
- thicker leftright arrow: $\Leftrightarrow$
- long leftright arrow: $\longleftrightarrow$

[//]: # ----------------------------------------------------------------
## Questions

\center
\fontsize{150}{150} \selectfont ?

\vspace{3cm}

[//]: # ----------------------------------------------------------------
## Bibliography (1/4)

\small

- Free book “PC Assembly Language”, Paul A. Carter\
\scriptsize [http://pacman128.github.io/pcasm/](http://pacman128.github.io/pcasm/)
\small

- x86 Assembly Guide, University of Virginia Computer Science\
\scriptsize [https://www.cs.virginia.edu/~evans/cs216/guides/x86.html](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)
\small

- Intel x86 JUMP quick reference\
\scriptsize [http://www.unixwiz.net/techtips/x86-jumps.html](http://www.unixwiz.net/techtips/x86-jumps.html)
\small

- x86 Instruction Set Reference\
\scriptsize [https://c9x.me/x86/](https://c9x.me/x86/)
\small

[//]: # ----------------------------------------------------------------
## Bibliography (2/4)

- Markdown and Pandoc tips\
`https://www.flutterbys.com.au/stats/tut/tut17.3.html`{.verysmall}

- Basic markdown syntax\
`https://www.markdownguide.org/basic-syntax/`{.verysmall}

- Tables in LaTeX\
`https://www.overleaf.com/learn/latex/tables`{.verysmall}

- Useful Pandoc tips\
`http://pages.stat.wisc.edu/~yandell/statgen/ucla/Help/Producing%20slide%20shows%20with%20Pandoc.html`{.verysmall}

- LaTeX colors\
`https://en.wikibooks.org/wiki/LaTeX/Colors`{.verysmall}

[//]: # ----------------------------------------------------------------
## Bibliography (3/4)

Markdown and Pandoc tips\

  - `https://www.flutterbys.com.au/stats/tut/tut17.3.html`{.verysmall}

Basic markdown syntax\

  - `https://www.markdownguide.org/basic-syntax/`{.verysmall}

Tables in LaTeX\

  - `https://www.overleaf.com/learn/latex/tables`{.verysmall}

Useful Pandoc tips\

  - `http://pages.stat.wisc.edu/~yandell/statgen/ucla/Help/Producing%20slide%20shows%20with%20Pandoc.html`{.verysmall}

LaTeX colors\

  - `https://en.wikibooks.org/wiki/LaTeX/Colors`{.verysmall}

[//]: # ----------------------------------------------------------------
## Bibliography (4/4)

### \footnotesize Free book “PC Assembly Language”, Paul A. Carter
\scriptsize [http://pacman128.github.io/pcasm/](http://pacman128.github.io/pcasm/)

### \footnotesize x86 Assembly Guide, University of Virginia Computer Science
\scriptsize [https://www.cs.virginia.edu/~evans/cs216/guides/x86.html](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)

### \footnotesize Intel x86 JUMP quick reference
\scriptsize [http://www.unixwiz.net/techtips/x86-jumps.html](http://www.unixwiz.net/techtips/x86-jumps.html)

### \footnotesize x86 Instruction Set Reference
\scriptsize [https://c9x.me/x86/](https://c9x.me/x86/)

<!--
Dans les exercices pour avoir la numerotation automatique:
- installer le filtre "pandoc-numbering"
Et ecrire: Exercice +.#
-->
