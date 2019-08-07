---
layout: lesson
root: .
---

Welcome to MCB 585! This course is offered by the Molecular & Cellular Biology Department at the University of Arizona. 

MCB585 is an advanced graduate course focused on quantitative approaches to biological questions. Students will learn how to acquire, access, and interact with large biological datasets. The course relies heavily on learning and utilizing the R Statistical Programing language, but students are not expected to have programing experience upon entering the course. The course is broken up into two parts. The first part will focus on introducing R, using R in basic statistical operations, and approaching and manipulating large datasets. This section incorporates elements of experimental design and appropriate application of statistical tests as a frame for learning R. The second section focuses on extracting quantitative information from image data and applying the statistical tools from the first section on this data.

**Instructors:**

*   **George Sutphin**, Assistant Professor, Molecule & Cellular Biology
*   **Andrew Paek**, Assistant Professor, Molecule & Cellular Biology


**Course Goals:**

Students will be able to:
1.	Use the R programing environment to approach basic problems biological sciences.
2.	Apply basic biostatistics methods, such as selecting and employing an appropriate statistical test and conducting a power analysis based on preliminary data.
3.	Access, manipulate, and analyze large biological datasets.
4.	Segment and extract quantitative information from imaging data.

**Course Requirements:**
1.  Attendance in class sessions.
2.  Participation in discussions and in-class exercises.
3.  Reading assignments, completed before class.
4.  Computer exercises before and during class.

## Prerequisites
>
> MCB585 is an advanced course intended for second-year graduate students.  The pre-requisites for the course are:
> 1.  One year of graduate-level coursework
> 2.  Two core courses required for the MCB, BIOC or CMM PhD
{: .prereq}




<!-- 
The best way to learn how to program is to do something useful,
so this introduction to R is built around a common scientific task:
data analysis.

Our real goal isn't to teach you R,
but to teach you the basic concepts that all programming depends on.
We use R in our lessons because:

1.  we have to use *something* for examples;
2.  it's free, well-documented, and runs almost everywhere;
3.  it has a large (and growing) user base among scientists; and
4.  it has a large library of external packages available for performing diverse tasks.

But the two most important things are
to use whatever language your colleagues are using,
so you can share your work with them easily,
and to use that language *well*.

We are studying inflammation in patients who have been given a new treatment for arthritis,
and need to analyze the first dozen data sets of their daily inflammation.
The data sets are stored in CSV format
([comma-separated values]({{ page.root }}/reference.html#comma-separated-values-csv)):
each row holds information for a single patient,
and the columns represent successive days.
The first few rows of our first file look like this:

~~~
0,0,1,3,1,2,4,7,8,3,3,3,10,5,7,4,7,7,12,18,6,13,11,11,7,7,4,6,8,8,4,4,5,7,3,4,2,3,0,0
0,1,2,1,2,1,3,2,2,6,10,11,5,9,4,4,7,16,8,6,18,4,12,5,12,7,11,5,11,3,3,5,4,4,5,5,1,1,0,1
0,1,1,3,3,2,6,2,5,9,5,7,4,5,4,15,5,11,9,10,19,14,12,17,7,12,11,7,4,2,10,5,4,2,2,3,2,2,1,1
0,0,2,0,4,2,2,1,6,7,10,7,9,13,8,8,15,10,10,7,17,4,4,7,6,15,6,4,9,11,3,5,6,3,3,4,2,3,2,1
0,1,1,3,3,1,3,5,2,4,4,7,6,5,3,10,8,10,6,17,9,14,9,7,13,9,12,6,7,7,9,6,3,2,2,4,2,0,1,1
~~~
{: .source}

We want to:

*   load that data into memory,
*   calculate the average inflammation per day across all patients, and
*   plot the result.

To do all that, we'll have to learn a little bit about programming.

> ## Prerequisites
>
> Learners need to understand the concepts of files and directories
> (including the working directory).
> We often use RStudio to teach this lesson, but it is not required.
{: .prereq} 
-->
