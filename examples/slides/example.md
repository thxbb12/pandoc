---
author: Florent Gluck - Florent.Gluck@hesge.ch
title: Pandoc Slide Examples
subtitle: This is a subtitle
date: \vspace{.5cm} \footnotesize \today
institute: \vspace{0.5cm} \tiny \textsuperscript{*}Many thanks to Prof. Ada Gavrilovska for letting me use some of the contents of her course "Introduction to Operating Systems" tought at Georgia Institut of Technology

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

blah blah \underline{blah blah} blah blah

- Default text color, \textcolor{red}{red text}, \textcolor{green}{green text},

\alert{`alert` : attention ceci est une giraffe !}

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
## Vertical space

Blah blah blah... Blah blah blah...
Blah blah blah... Blah blah blah...

\vspace{2cm}

Blah blah blah... Blah blah blah...
Blah blah blah... Blah blah blah...

[//]: # ----------------------------------------------------------------
## Avec "vfill"

Il en existe deux types de méthodes:

* **méthodes d'instance** 
  * elles sont rattachées à l'objet
* **méthodes statiques** ou **de classe**
  * elles sont rattachées à la classe 
  * utilisation sans instanciation d'un objet

\vfill

```{.java .numberLines .small}
String test = "coucou";
test.toUpperCase();
String.valueOf(1234);
```

[//]: # ----------------------------------------------------------------
## Sans "vfill"

Il en existe deux types de méthodes:

* **méthodes d'instance** 
  * elles sont rattachées à l'objet
* **méthodes statiques** ou **de classe**
  * elles sont rattachées à la classe 
  * utilisation sans instanciation d'un objet

```{.java .numberLines .small}
String test = "coucou";
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
## Blocks

\metroset{block=fill}
### \alert{This is a block}
Block text

[//]: # ----------------------------------------------------------------
## Special characters (symbols)

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

<!--
Dans les exercices pour avoir la numerotation automatique:
- installer le filtre "pandoc-numbering"
Et ecrire: Exercice +.#
-->

[//]: # ----------------------------------------------------------------
## Questions

\center
\fontsize{150}{150} \selectfont ?

\vspace{3cm}

[//]: # ----------------------------------------------------------------
## Bibliography

- Dockerfile reference (official)\
`https://docs.docker.com/engine/reference/builder/`{.verysmall}

- Best practices for writing Dockerfiles (official)\
`https://docs.docker.com/develop/develop-images/dockerfile_best-practices/`{.verysmall}

- Dockerfile tutorial by example - basics and best practices\
`https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/`{.verysmall}
