431 Lab 03
================
Due **2021-09-27** at 9 PM \| Last Edited 2021-08-18 10:57:17

## Deadline

Lab 03 has 10 questions, all of which you need to complete by the
deadline posted on the [Course
Calendar](https://thomaselove.github.io/431/calendar.html). We don’t
give extensions on Labs. Instead, we use the [Late Work
policy](https://github.com/THOMASELOVE/431-2021/tree/main/labs#late-work)
to deal with Late work on Labs.

## Getting Help

You are welcome to discuss Lab 03 with Professor Love, the teaching
assistants or your colleagues, but your answer must be prepared by you
alone. Don’t be afraid to ask questions, using any of the methods
described on our [Contact
Us](https://thomaselove.github.io/431/contact.html) page.

## Learning Objectives

1.  Continue to practice and refine visualizing data in an informative
    way, with attention to the center, shape, and spread.
2.  Use various approaches to obtain numeric summaries to assess
    distributions
3.  Use visualization to describe the relationship between two
    variables.
4.  Use visualizations to assess the adequacy of a Normal distribution
    model.

## Getting Started with Lab 03

To start, create a directory on your computer for `lab03` following the
suggestions we provided in Lab 02.

-   Into that `lab03` directory, you will download the R Markdown
    Template for Lab 03, which is called `YOURNAME-Lab03.Rmd`. This
    should be useful to you in the same way as the Template for Lab 02
    was. After you download the template file to your directory, you
    will want to rename it to substitute in your actual name in the file
    name, rather than `YOURNAME`.

As in Lab 02, after you’ve downloaded the relevant files, open RStudio,
and use the **File** … **New Project** … **Existing Directory** menu to
create an R Project in your `lab03` directory in which you will do all
of your work for Lab 03.

## The R Markdown Template for Lab 03

We have provided an R Markdown document template for this assignment
called `YOURNAME-Lab03.Rmd` that you should use to complete your work.

-   The template is part of the [Data and Code
    repository](https://github.com/THOMASELOVE/431-data) for the course.
    Follow the instructions posted there to download all of the files
    you’ll need in a ZIP file, including the template to an easy place
    to find them on your computer (we suggest a `431-data` subdirectory
    in your `2021-431` directory.) Then copy the template into your
    directory for Lab 03, specifically, that you created earlier. That’s
    probably the easiest approach.
-   The template provides some coding hints, which we hope you’ll make
    use of.

You should build your response to all ten questions as an R Markdown
file using the `YOURNAME-lab03.Rmd` template provided. Use the Knit
button in RStudio to compile your work and create the HTML output.
You’ll want to do this multiple times as you go, to identify potential
problems quickly.

## The Data for Lab 03

There are two sets of data used in this lab.

### The `penguins` data

In Questions 1-5, we’ll be using the `penguins` data (note: use the
`penguins` tibble, and not the `penguins_raw` tibble for this Lab)
contained in the `palmerpenguins` package in R. The complete citation is
…

Horst AM, Hill AP, Gorman KB (2020). palmerpenguins: Palmer Archipelago
(Antarctica) penguin data. R package version 0.1.0.
<https://allisonhorst.github.io/palmerpenguins/>. doi:
10.5281/zenodo.3960218.

Additional information on the data are provided by Allison Horst at the
github site linked above. In particular, you’ll find a nice cartoon of
[the three species of penguin contained in the
data](https://github.com/allisonhorst/palmerpenguins#meet-the-palmer-penguins)
and a detailed [description of the bill
measurements](https://github.com/allisonhorst/palmerpenguins#bill-dimensions)
that are worth your time.

### County Health Rankings data

In Questions 6-9, we’ll be using additional data from the [2021 County
Health Rankings Data](https://www.countyhealthrankings.org/) that we saw
back in Lab 02. We have compiled a larger data set called
`lab03_counties.csv` which you will find in our [Data and Code
repository](https://github.com/THOMASELOVE/431-data). This data file
contains all of the counties and a dozen of the available variables in
the full County Health Rankings data.

# Part A: Palmer Penguins (Questions 1-5)

## Question 1 (8 points)

We are interested in the body mass (in grams), `body_mass_g`, of the
penguins included in these data. Create a visualization of this variable
that will help us evaluate its center, shape, and spread, using
appropriate labels for all axes, and a useful title for the
visualization.

## Question 2 (8 points)

Identify the mean, standard deviation, median and interquartile range of
the penguin’s body mass (in grams). Do not simply report R output but
(in addition to presenting your code and the resulting output) state, in
complete English sentences, your results.

## Question 3 (8 points)

Given your visualization in Question 1 and the numeric summary in
Question 2, please discuss the center, shape, and spread of the body
mass of the penguins. Does it seem that body mass follows a Normal
distribution? Would it be more appropriate to examine the mean or median
in this setting, and why?

## Question 4 (8 points)

The dataset also contains information on the penguin’s species
(`species`). Now, build a visualization and a numeric summary to examine
body mass across the three species types.

## Question 5 (8 points)

Given your findings in Question 4, what can we conclude about the body
mass across species?

# Part B: County Health Rankings (Questions 6-9)

## Question 6 (10 points)

Take a random sample of 750 counties from the County Health Rankings
Data provided in `lab03_counties.csv`. As part of this work, use the
command:

    set.seed(20212022)

so that each of us selects the same sample of data. Name this random
sample `chr_sample` in R. Select only the following variables: `state`,
`county_name`, `adult_obesity`, and `food_insecurity`.

Once this is done, demonstrate that Cuyahoga County in Ohio is in your
sample and that the mean of `adult_obesity` is 0.3345.

## Question 7 (10 points)

We are interested in looking at `adult_obesity` as an outcome. Build a
visualization and describe the center, spread, and shape of the
distribution of this variable. Does a Normal model for this distribution
seem appropriate? Why or why not?

## Question 8 (10 points)

Now we’d like to examine the relationship between `food_insecurity` (our
predictor) and `adult_obesity` (our outcome). Build a useful,
well-labeled visualization and then use it to motivate your description
of the relationship between these two variables in complete sentences.
Does a linear model seem appropriate to describe the association of
these variables? Why or why not? Hint: you will likely want to include a
smooth of some sort in your visualization.

## Question 9 (10 points)

Create a new figure (perhaps building on the one you built in Question
8) so that this new Figure identifies where Cuyahoga County falls when
examining the relationship between `adult_obesity` and
`food_insecurity`. Briefly interpret Cuyahoga County’s position on each
variable relative to the others in the random sample.

# Part C: Spiegelhalter Reaction

## Question 10 (20 points)

Reflecting on Chapter 4 of *The Art of Statistics*, please write an
essay of no more than 100 words which discusses the relationship between
`adult_obesity` and `food_insecurity` we observe in our sample of
counties. Specifically, discuss whether or not we can conclude that lack
of access to adequate food causes obesity.

In your response be sure to also discuss whether the method that we used
to identify these data (our 750 observation random sample) strengthens
or weakens your conclusion(s).

# Include the session information

At the end of your R Markdown file, please include a new code chunk to
provide the **session information**. This time, we’ll use an alternative
approach to get this (as compared to what we did in Lab 02):

``` r
sessioninfo::session_info()
```

    - Session info ---------------------------------------------------------------
     setting  value                       
     version  R version 4.1.0 (2021-05-18)
     os       Windows 10 x64              
     system   x86_64, mingw32             
     ui       RTerm                       
     language (EN)                        
     collate  English_United States.1252  
     ctype    English_United States.1252  
     tz       America/New_York            
     date     2021-08-18                  

    - Packages -------------------------------------------------------------------
     package     * version date       lib source        
     cli           3.0.1   2021-07-17 [1] CRAN (R 4.1.0)
     digest        0.6.27  2020-10-24 [1] CRAN (R 4.1.0)
     evaluate      0.14    2019-05-28 [1] CRAN (R 4.1.0)
     htmltools     0.5.1.1 2021-01-22 [1] CRAN (R 4.1.0)
     knitr         1.33    2021-04-24 [1] CRAN (R 4.1.0)
     magrittr      2.0.1   2020-11-17 [1] CRAN (R 4.1.0)
     rlang         0.4.11  2021-04-30 [1] CRAN (R 4.1.0)
     rmarkdown     2.10    2021-08-06 [1] CRAN (R 4.1.0)
     rstudioapi    0.13    2020-11-12 [1] CRAN (R 4.1.0)
     sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 4.1.0)
     stringi       1.7.3   2021-07-16 [1] CRAN (R 4.1.0)
     stringr       1.4.0   2019-02-10 [1] CRAN (R 4.1.0)
     withr         2.4.2   2021-04-18 [1] CRAN (R 4.1.0)
     xfun          0.24    2021-06-15 [1] CRAN (R 4.1.0)
     yaml          2.2.1   2020-02-01 [1] CRAN (R 4.1.0)

    [1] C:/Users/Thomas/Documents/R/win-library/4.1
    [2] C:/Program Files/R/R-4.1.0/library

Again, providing the session information helps with reproducibility. It
lets us see what packages you have loaded on your machine, and some
other information about your R session that can be helpful in
understanding any problems you run into. The
`sessioninfo::session_info()` command shown above is part of the
template for this Lab, and is a good alternative in many cases to the
approach we took in Lab 02. One or the other of these session
information runs should appear at the end of all of your lab and project
work for this course.

# Submitting the Lab

As mentioned, you should build your entire response as an R Markdown
file using the `YOURNAME-lab03.Rmd` template provided. Then use the Knit
button in RStudio to create the resulting HTML document. Be sure to
remove all of the instructions included in the original template before
submitting your work, and also be sure to review the HTML result to
ensure that it looks clean and clear, that the labels on your plots and
other output are easy to read, and that it doesn’t retain any
unnecessary warning messages or other material that distracts from your
work.

Submit **both** your revised R Markdown file **and** the HTML output
file to the Lab 03 section in the [Assignments folder in
Canvas](https://canvas.case.edu) by the deadline specified in [the
Course Calendar](https://thomaselove.github.io/431/calendar.html). We
will need both the R Markdown and HTML file submitted before we can
grade your work.

Again, we encourage you in the strongest possible terms to **ask
questions**, using any of the approaches described on our [Contact
Us](https://thomaselove.github.io/431/contact.html) page.
