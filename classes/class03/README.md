# 431 Class 03: 2021-08-31

- This is the README for Class 03 of Professor Love's 431 course for Fall 2021. The main website is https://thomaselove.github.io/431/. Get here through the link on the [Course Calendar](https://thomaselove.github.io/431/calendar.html).

## This is a pre-recorded class. We will not meet in-person on 2021-08-31. Our next class meeting is Thursday 2021-09-02 at 1 PM in E321, for Class 04.

For Class 03, Dr. Love has recorded himself using R and RStudio to:

- create a Project in RStudio
- create an R Markdown document to obtain and describe results
- ingest a data set from the wild into an R data frame
- manage that data frame so that it becomes a tidy tibble
- use that tibble to learn about the data by iterating through
  - visualizing the data
  - transforming the data
  - modeling the data (with a few simple summaries)
- interspersing code and text in an R Markdown document
- "knitting" that R Markdown document into an attractive HTML result

## The Materials

- The 97-minute video recording is available **now**, via either the Modules section or the Echo 360 section of [Canvas](https://canvas.case.edu/), or directly through Zoom at the link provided on our Shared Google Drive.
    - If you view the recording directly through Zoom (where you should also be able to download the recording) you should be able to click into the transcript to look at specific pieces of the work.
- The [431-first-r-template.Rmd](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class03/431-first-r-template.Rmd) file I'll start with (this is also available as part of [our 431-data page](https://github.com/THOMASELOVE/431-data)).
    - Be sure to click Raw to download the plain text version if that's what you want.
- The [quick_survey_2021.csv](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class03/data/quick_survey_2021.csv) file containing the data we'll use (this is also available as part of [our 431-data page](https://github.com/THOMASELOVE/431-data))
    - Again, be sure to click Raw to download the file if you're not pulling it from the 431-data page.
- The [431-class03-results.Rmd](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class03/431-class03-results.Rmd) file that shows the final version of the R Markdown file created during the recorded session.
- The HTML version of the document (after knitting the R Markdown) can be viewed at http://rpubs.com/TELOVE/class03-results-431.

## Analytic Questions Addressed in Class 03

We address these five "analytic" questions in the file, using the data from the Quick Survey we conducted in Class 02. Here's [the PDF file of that survey](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/431_quick_survey_2021-08-26.pdf) if you'd like to see it.

- A. What is the distribution of pulse rates among students in 431 since 2014?
- B. Does the distribution of student heights change materially over time?
- C. Do taller people appear to have paid less for their most recent haircut?
- D. Does the relationship between height and haircut price look the same within each sex?
- E. For the 2021 students specifically, do students have a more substantial tobacco history if they prefer to speak English or a language other than English?

## R Tools Demonstrated in Class 03

In addition to demonstrating general approaches for creating R projects and R Markdown files, and loading R packages, Dr. Love's Class 03 recording demonstrates the following key ideas:

1. Ingesting data with `read_csv` from a csv (comma-separated version text) file.
2. Six key verbs from the `tidyverse`: `count`, `filter`, `select`, `mutate`, `group_by` and `summarize`
3. Using two pipes: `%>%` for work within the tidyverse and `%$%` to extract variables from a tibble.
4. Summarizing data with `summary`, `tabyl` and with `mosaic::favstats`
5. Using `across` and `where` to do more efficient programming across columns
6. Dealing with missing data via the creation of complete-case analyses with `filter(complete.cases(.))`
7. Converting categorical variables to factors with `as_factor`, and recoding the levels of those factors with `fct_recode`
8. Building plots using `ggplot` and the `ggplot2` package
    - Setting the x and y variables with `aes()`
    - Using `geom_histogram()` to obtain histograms of quantities
    - Using `geom_boxplot()` and `geom_violin()` for comparisons of quantities across categories (groups)
    - Using `geom_point()` and `geom_smooth()` to build scatterplots of the association between quantities and fit linear models and loess smooths to data
    - Building multiple plots with `facet_grid()` and `facet_wrap()` and by using `aes(group = ., color = .)` to divide plots by a category
    - Using `labs()` to set axis labels, main and sub-titles
    - Using `guides(col = "none")` to delete legends from a plot where color is used to separate groups
9. Using `lm` to fit and `summary(lm())` to summarize a straight-line ordinary least squares linear regression model
10. Using `sessionInfo()` to describe information about your installation of R at the end of your session.

All of this material is also demonstrated in early Chapters of the [Course Notes](https://thomaselove.github.io/431-notes/), and we will review (and augment) these ideas in class over the next few weeks.

# Things to do before Thursday's Class 04

1. Watch the video provided for Class 03, and (if you like) work your way through the R Markdown files provided.
2. Complete the required reading (the [Syllabus](https://thomaselove.github.io/431-2021-syllabus/) and at least the introduction to David Spiegelhalter's *The Art of Statistics*) as specified in the [Course Calendar](https://thomaselove.github.io/431/calendar.html). Chapter 1 of Spiegelhalter is also something worth reading now.
3. Get all necessary software installed on your computer, following the instructions on our [Software Installation](https://thomaselove.github.io/431/software_install.html) page. Be sure to install the necessary [R Packages](https://thomaselove.github.io/431/r_packages.html), and [data sets](https://thomaselove.github.io/431/data_index.html). And check out our [Software Tutorials](https://github.com/THOMASELOVE/431-2021/blob/main/software/README.md) page for some additional suggestions on how to get up to speed with R.
4. It will be helpful to come to class on Thursday with a laptop on which you are running R and RStudio. Take a look at the [Class 04 README](https://github.com/THOMASELOVE/431-2021/tree/main/classes/class04) which will include key files you'll want to download to use during the session.
5. Get started on [Lab 01](https://github.com/THOMASELOVE/431-2021/tree/main/labs) which is your first substantial assignment for the course and which is due Monday 2021-09-06 at 9 PM, as indicated by the [Calendar](https://thomaselove.github.io/431/calendar.html). 
    - If you've completed [Lab 01](https://github.com/THOMASELOVE/431-2021/tree/main/labs), then take a look at [Lab 02](https://github.com/THOMASELOVE/431-2021/tree/main/labs), which is due two weeks later, on 2021-09-20.
6. Try out [Piazza](https://piazza.com/case/fall2021/pqhs431) if you have any questions about software installation or anything else, or visit [TA office hours](https://thomaselove.github.io/431/contact.html) (which are held every day except Tuesday - Zoom links are in our Shared Google Drive.)

