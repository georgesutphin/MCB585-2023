---
title: "Title"
teaching: 80
exercises: 25
questions:
- "How do I use the RStudio graphical user interface?"
- "Know when to use setwd()."
- "Where can I get help?"
objectives:
- "Get familiar with RStudio interface."
- "Understand the difference between script file and console."
- "Demonstrate useful shortcuts."
- "Know when to use setwd()."
keypoints:
- "Using RStudio can make programming in R much more productive."
- "Consider what working directory you are in when sourcing a script."
source: Rmd
---



### Introduction to R and RStudio

If we only had one data set to analyze, it would probably be faster to load the file into a spreadsheet and use that to plot some simple statistics.

But what if we have twelve files to check? What if we are running analysis that we will be repeating in the future?

**What is R?**

R is a statistical programming language widely used by working scientists that provides a broad spectrum of tools for data manipulation, statistical analysis, machine learning, and more. R is one of the fastest growing programming languages and new tools are being created all the time. 

Advantages of R:
* **Versatility** -- you can do just about anything in the data analysis world
* **Repeatability** -- Because R is a programming language, a properly designed script can be repeated and automated.
* **Community** -- Because R is widely used, there is a large and active online community producing resources, answering questions, and trying to solve new problems.

Disadvantages of R:
* **Learning Curve** -- R is a programming language. If you don't have programming experience, it can be a bit daunting.
* **Slow for one-time operations** -- R is great of any analysis that you plan to perform more than once. Other tools are better for quick, one-time projects.

**What is RStudio?**

RStudio is an integrated development environment (IDE) for R. It basically provides a convenient working environment for writing and employing R scripts. While you can work directly in the IDE provided with R, RStudio has a number of tools that make R easier to learn and interact with. We will be working exclusively in RStudio during this course.


### Installing R and RStudio

To participate in both in-class exercises and homework, you will need access to a computer with the current versions of the following installed:

1. [R software](https://cran.r-project.org/mirrors.html)
1. [RStudio Desktop](https://www.rstudio.com/products/rstudio/download/#download)

You also need to download some files to follow along with the lessons in class:

1. Make a new folder in your Desktop called `MCB585`.
2. Download [MCB585-sample-data.zip]({{ page.root }}/data/MCB585-sample-data.zip)
   and move the file to this folder.
3. If it's not unzipped yet, double-click on it to unzip it. You should end up
   with a new folder called `data`.


#### Using RStudio

Here are the basic elements of RStudio:

<img src="../fig/01-RStudio-overview.png" alt="RStudio Visual Interface" />

* Code and workflow are more reproducible if we can document everything that we do.
* Our end goal is not just to "do stuff" but to do it in a way that anyone can
  easily and exactly replicate our workflow and results.
* The best way to achieve this is to write scripts. RStudio provides an
  environment that allows you to do that.


#### Interacting with R using RStudio

There are two main ways of interacting with R: using the console or using
script files (plain text files that contain your code).

**Console:** The console window (bottom left panel in RStudio) is the place where R is
waiting for you to tell it what to do, and where it will show the results of a
command.  You can type commands directly into the console, but they will be
forgotten when you close the session. 

**Script:** The script window (top left panel) It is better to enter the commands in the
script editor, and save the script. This way, you have a complete record of what
you did, you can easily show others how you did it and you can do it again later
on if needed. To run commands from script, you can either copy-paste them into the R console, or you can use the script window to 'send' the current line or the currently selected text to the R console using the <kbd>Ctrl</kbd>+<kbd>Return</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>Enter</kbd> keyboard shortcut.

At some point in your analysis you may want to check the content of variable or
the structure of an object, without necessarily keep a record of it in your
script. You can type these commands directly in the console. RStudio provides
the <kbd>Ctrl</kbd>+<kbd>1</kbd> and <kbd>Ctrl</kbd>+<kbd>2</kbd> shortcuts allow you to jump between the script and the
console windows.

If R is ready to accept commands, the R console shows a `>` prompt. If it
receives a command (by typing, copy-pasting or sent from the script editor using
<kbd>Ctrl</kbd>+<kbd>Return</kbd>/<kbd>Ctrl</kbd>+<kbd>Enter</kbd>), R will try to execute it, and when ready, show the results and come back with a new `>`-prompt to wait for new commands.

If R is still waiting for you to enter more data because the command you entered is not yet complete, the console will show a `+` prompt. This means that you haven't finished entering
a complete command, perhaps because you haven't 'closed' a parenthesis or quotation. If you're in RStudio and this happens, either complete the command and press <kbd>Enter</kbd> or click inside the console window and press <kbd>Esc</kbd> to cancel the current command. That should help you out of trouble.


### Interacting with the console

#### Basic commands

At the simplest level, the console can be used as a calculator to directly ask for basic operations. Try a few of the following:

*To run the command, try to copy-paste each line into the console and run. Also try copying/typing each line into the script, highlighting the text (or just make sure your cursor is on the right line), and pressing <kbd>Ctrl</kbd>+<kbd>Enter</kbd>.*



~~~
# Addition
40+2
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# Subtraction
98-56
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# Multiplication
6*7
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# Division
74088/1764
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# Exponential
6.480741^2
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
# Equations with parenthetical operations
(((6 + 4) + 2)^2 + 9)/3 - 9 # You can comment here too!
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}


#### Commenting

Note above the use of `#` signs to add comment. Comments are for you and anyone coming later to read your script. Anything to the right of a `#` is ignored by R. Comment liberally in your R scripts. We will discuss best practices in coding and the use of comments more later on in the course.


#### Assignment Operator

`<-` is the assignment operator. It assigns values on the right to objects on
the left. So, after executing `x <- 3`, the value of `x` is `3`. The arrow can
be read as 3 **goes into** `x`.  You can also use `=` for assignments but not in
all contexts so it is good practice to use `<-` for assignments.

In RStudio, the <kbd>Alt</kbd>+<kbd>-</kbd> will write `<-` in a single keystroke. Let's give it a go:


~~~
x <- 42   # using <- sets the value of the variable x to 42.
y = 42    # using `=` in place of `<-` works in almost all situation (but not quite all; it is better to get into the habit of using `<-`).

# if you want to see the value of a variable, just type the variable name into the console:
x
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
y
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}

Also note that when you assign a value to a variable, a new object is created in the Environment panel (upper right). This panel lists all *objects* in your *workspace*. Note that whenever you make an assignment with `<-` or `=`, R creates a new object in memory. Your workspace is simply the collection of objects currently stored in memory that are available to access in your current R session.

Now that we have assigned a value to a variable, we can use that variable to calculate other things:


~~~
x + 3
~~~
{: .language-r}



~~~
[1] 45
~~~
{: .output}



~~~
2*(x + y)
~~~
{: .language-r}



~~~
[1] 168
~~~
{: .output}



~~~
z = y + 2*x
z
~~~
{: .language-r}



~~~
[1] 126
~~~
{: .output}

What happens if you don't complete a line:

~~~
100 + 
~~~
{: .language-r}



~~~
Error: <text>:2:0: unexpected end of input
1: 100 + 
   ^
~~~
{: .error}

R hangs with a `+` in the console, wainting for you to finish your thought...

~~~
1
~~~
{: .language-r}



~~~
[1] 1
~~~
{: .output}

All better.


You can use the `ls()` command to list all variables currently defined in your workspace.


~~~
ls()
~~~
{: .language-r}



~~~
[1] "args"          "dest_md"       "missing_pkgs"  "required_pkgs"
[5] "src_rmd"       "x"             "y"             "z"            
~~~
{: .output}


> ## What is allowed or not allowed with variable names?
>
> Try assigning values to the following variables. Which work and which do not? What is 
> causing the erros?
>
> ~~~
> min_height <- 1
> max.height <- 1
> _age <- 1
> .mass <- 1
> MaxLength <- 1
> min-length <- 1
> 2widths <- 1
> celsius2kelvin <- 1
> ~~~
> {: .language-r}
>
> > ## Solution
> > 
> > The lines in <span style="color:blue">blue</span> work, the lines in
> > <span style="color:red">red</span> fail:
> > * <span style="color:blue">min_height <- 1</span>
> > * <span style="color:blue">max.height <- 1</span>
> > * <span style="color:red">_age <- 1</span> --> error; starts with a symbol
> > * <span style="color:blue">.mass <- 1</span>> --> no error --> the . results in a 
> > hidden variable
> > * <span style="color:blue">MaxLength <- 1</span>
> > * <span style="color:red">min-length <- 1</span> --> error; "-" is an operator
> > * <span style="color:red">2widths <- 1</span> --> error; starts with a number
> > * <span style="color:blue">celsius2kelvin <- 1</span>
> >
> {: .solution}
{: .challenge}


#### Cleaning up

Try clicking on the brush icon in the Environment panel and clicking <kbd>Yes</kbd> in the po-up box. What happened to your variable? What happens if you try to display the variable in the console?


~~~
x
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}



~~~
y
~~~
{: .language-r}



~~~
[1] 42
~~~
{: .output}

You can also remove variables one at a time.


~~~
x = 3
y = x + 2
z1 = x - y
z2 = x + y

rm(x)
rm(y)
rm(list = ls()) # remove all variables currently in environment
~~~
{: .language-r}


It is generally good practice to start off each session with a clean slate. When you start RStudio, the Environment will be clear (unless you load a previously saved workspace). If you are finished with one analysis and starting another, it is a good idea to clear you Environment. That way if you reuse a variable name (e.g. `x`) you won't accidentally end up using the value stored in your workspace during the previous analysis.


#### Working directories in R

Your *working directory* refers to the file path on your computer where the current session of R will go to look for files. You need to have any external data that you are working with in a file in your working directory in order to load it into R (or know how to specify a different location, if it isn't in your working directory). Any output (data or charts) that you save in R will also be stored in the working directory by default unless you specifcy a different location on your computer. 

A collection of scripts and data in R are defined as a *Project*. Among other things, the project will define the default working directory. Let's try staring a new project:

1. In RStudio, click **File > New Project...**.
2. Click **Existing Directory**.
3. Click <kbd>Browse...</kbd>.
4. Navigate to your *MCB585* folder and click <kbd>Create Project</kbd>.

RStudio will reload with a clean working environment. If you click on the **Files** tab (lower right panel), you will see that the current folder is you *MCB585* folder, and that RStudio will have created a new file called **MCB585.Rproj**.

In the future, you can either just open this file from you file explorer to load you MCB585 project, or you can open it from RStudio by clicking **File > Open Project...**, navigating to your *MCB585* folder, and selecting the **MCB585.Rproj** file.

You can change the active working directly by using the function `setwd()`. For example, we can set the working directory to our *MCB585/data* folder using the following command:


~~~
setwd("./data")
setwd("data") 
~~~
{: .language-r}



~~~
Error in setwd("data"): cannot change working directory
~~~
{: .error}



~~~
setwd("..") 
~~~
{: .language-r}

Note that unless you specify the entire path, all entries will be relative to the current working directory. Relative navigation:
* '.' = the current working directory
* '..' = the directory one level above the working directory (i.e. the Desktop in our case)
* Note that "./data" and "data" both mean "go to the *data* folder inside the working directory"

If you are unsure what your current working directory is, you can define the entire path:


~~~
setwd("C:/Users/<username>/Desktop/MCB585/data") # Windows
setwd("/Users/<username>/Desktop") # MacOS
~~~
{: .language-r}

**Caution for Windows users:** If you copy a file path from Windows Explorer and paste it into `setwd()`, you have to change the backslashes ("\\") used in Windows to forwardslashes ("/"). R interprets "\\" as a type of special type of character called an *escape character* rather than a part of the string. If you don't replace them, you will get errors:


~~~
setwd(".\data")
~~~
{: .language-r}



~~~
Error: '\d' is an unrecognized escape in character string starting "".\d"
~~~
{: .error}

We can also ask R what the current working directory is using `getwd()`, and ask for a list of files in the current directly with list.files():


~~~
getwd()
~~~
{: .language-r}



~~~
[1] "C:/Users/sutph/Documents/GitHub/MCB585/_episodes_rmd"
~~~
{: .output}



~~~
list.files()
~~~
{: .language-r}



~~~
[1] "01-R-RStudio-setup.Rmd" "data"                  
~~~
{: .output}


> ## Be careful when using `setwd()`
>
> One should exercise caution when using `setwd()`. Changing directories in a script file can limit reproducibility:
> * `setwd()` will return an error if the directory to which you're trying to change doesn't exist or if the user doesn't have the correct permissions to access that directory. This becomes a problem when sharing scripts between users who have organized their directories differently.
> * If/when your script terminates with an error, you might leave the user in a different directory than the one they started in, and if they then call the script again, this will cause further problems. If you must use `setwd()`, it is best to put it at the top of the script to avoid these problems.
> The following error message indicates that R has failed to set the working directory you specified:
> ```
> Error in setwd("~/path/to/working/directory") : cannot change working directory
> ```
> It is best practice to have the user running the script begin in a consistent directory on their machine and then use relative file paths from that directory to access files (see below).
{: .callout}


#### Installing and loading packages

R comes preloaded with a decently wide range of functions for basic data manipulation, but you will inevitably want to do something more interesting. There are many, many 'packages' that are available online for download. Each package is a set of related functions designed for a specific area of analysis. For example, later in the course we will use specialized packages that contain functions for power analysis (the `pwr` package) and survival analysis (the `survival` package). 

To use a package, you have to do two things:
1. **Install** -- Download the package from an external source, and make the functions accessible to R and RStudio. This is accomplished with the `install.packages()` function and only has to be done just per computer.
2. **Load** -- Installing the package does not immediately allow you to access the associated functions. You first have to load the package into your local workspace. This is done with the `library()` function.

Let's give it a try:


~~~
install.packages("pwr")
~~~
{: .language-r}



~~~
package 'pwr' successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\sutph\AppData\Local\Temp\Rtmp0ywEkG\downloaded_packages
~~~
{: .output}



~~~
install.packages("survival")
~~~
{: .language-r}



~~~
package 'survival' successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\sutph\AppData\Local\Temp\Rtmp0ywEkG\downloaded_packages
~~~
{: .output}



~~~
library("pwr")
library("survival")
~~~
{: .language-r}

Generally a Google search will let you find packages for just about any type of analysis. Generally these come from one of two sources (which R mostly takes care of automatically, with a few exceptions):
* CRAN for basic R packages
* Bioconductor for biological packages


{% include links.md %}
