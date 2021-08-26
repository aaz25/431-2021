# 431 Class 02: 2021-08-26

- This is the README for Class 02 of Professor Love's 431 course for Fall 2021. The main website is https://thomaselove.github.io/431/.
- Each class' README serves as a **starting point**. Get here through the link on the [Course Calendar](https://thomaselove.github.io/431/calendar.html).

## Today's Opener: The Quick Survey

As you come in, you will receive a paper survey with 15 questions. Please read these instructions carefully before writing anything down.

1. Introduce yourself to someone near you.
2. Record the survey answers **for that other person**, while they record your responses.
3. Be sure to complete all 15 questions (both sides of the paper).
4. When you are finished, thank your partner and raise your hand. Someone will come around to collect your survey.

There is a [PDF copy of the Quick Survey here](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/431_quick_survey_2021-08-26.pdf), if you'd like to look at the form after your paper copy has been collected.

## Today's Slides

- Class 02 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/431-class02-slides.pdf), as well as in [R Markdown format](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/431-class02-slides.Rmd), so you can see how I built them.

## Tweet of the Day

![](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/images/victor_2021-08-24.PNG)

## Today's Announcements

1. Each 431 class is recorded. The Class 01 recording is available on [Canvas](https://canvas.case.edu/) through Modules, or you can view (and, I believe, download) it on the Zoom link provided in our Shared Google Drive. Recordings of each class should be posted the next morning. If you have problems accessing the recordings, let us know about it on [Piazza](https://thomaselove.github.io/431/).

2. Your first substantial deliverable for the course is [Lab 01](https://github.com/THOMASELOVE/431-2021/blob/main/labs/lab01/lab01.md) which requires you to answer four questions. The deadline, as always, is on the [Course Calendar](https://thomaselove.github.io/431/calendar.html).
    - You'll not be analyzing any data using R in this Lab (unlike all the other Labs) but you'll still want to be able to run R to do it.
    - You'll need to have read the introduction to David Spiegelhalter's *The Art of Statistics* before you do the lab. 

3. I have a roster posted (called 431 Please Check this Roster) on our Shared Drive. Take a look and see if I have the name you want me to use for you, your preferred email, your CWRU ID, your personal pronouns and your program of study. If something's wrong, email me as soon as possible to let me know. If you're not on the list and think you're enrolled in the class, there's a problem.

4. Dr. Love prepared detailed [results from the Welcome to 431 Survey](https://bit.ly/welcome-to-431-results), which you should be able to view if you are logged into Google via CWRU. Please give them a look.

5. In Class 01, fifteen groups reported their guessed ages based on ten photographs. I'll summarize the results by Group here.

Contents of the table:

- **Group (size)** is the name of the group and the number of members, so The R group had 4 members
- **Low-Yes-High** counts estimates that were too low, correct (Yes) and too high, so The R group had 5 too low and 5 too high, none correct.
- **Mean E** is the mean error (sum of the errors divided by 10), so The R group's positive and negative errors exactly balanced out.
- **Range Abs E** is the range (minimum and maximum) of the absolute value of the group's errors, so R group's smallest (in absolute value) error was 1, and its largest was 9 years.
- **Sum Abs E** is the sum of the absolute values of the errors, and this is 36 for The R group
- **Sum E sq** is the sum of the squared errors, and this is 186 for The R group
- **Winners** specifies the photos where this group had the best estimate (t = tie), which didn't happen for The R group. Dimetrodons tied for the best estimate on photo number 5.
- **Corr.** is the Pearson product-moment correlation (often called `r`) of this group's estimates and the actual ages of the ten photographed subjects.
- **R-sq** is the square of the correlation coefficient (or R-squared) which indicates the proportion of variation explained by a linear regression on the estimates when predicting the actual ages.

Group (size) | Low-Yes-High | Mean E | Range Abs E | Sum Abs E | Sum E sq | Winners | Corr. | R-sq
:-----: | :-----: | :----: | :----: | :----: | :----: | :-------: | :-----: | :----:
The R group (4) | 5-0-5 | 0 | (1, 9) | 36 | 186 | - | 0.985 | 0.970
Dimetrodons (3) | 5-0-5 | -0.9 | (1, 12) | 49 | 347 | 05t | 0.979 | 0.959
Alice (4) | 2-1-7 | 2.1 | (0, 12) | 41 | 283 | 02t, 06t, **07**, 08t | 0.976 | 0.953
Terrible Tibbles (6) | 4-0-6 | -0.1 | (1, 11) | 41 | 295 | 01t, 06t | 0.974 | 0.949
Mushrooms (3) | 1-2-7 | 3.7 | (0, 16) | 45 | 431 | 02t, **03**, 04t | 0.974 | 0.948
Luis's Group (5) | 4-0-6 | 0.6 | (1, 14) | 58 | 506 | 10t | 0.962 | 0.925
ThoseJazzHands (3) | 4-1-5 | 2.1 | (0, 12) | 57 | 465 | 04t | 0.960 | 0.921
The Tukeys (4) | 4-1-5 | 1.7 | (0, 14) | 57 | 479 | 04t, 10t | 0.956 | 0.914
3 guys (3) | 4-0-6 | 1.8 | (1, 16) | 50 | 474 | 06t, **09**, 10t | 0.956 | 0.914
Locker Team (5) | 4-0-6 | 0.5 | (1, 16) | 57 | 505 | 08t | 0.951 | 0.905
RAJA (4) | 5-0-5 | -1.3 | (1, 12) | 71 | 581 | - | 0.946 | 0.896
SiJaDrMiSn (5) | 5-0-5 | -2.2 | (2, 16) | 72 | 718 | - | 0.937 | 0.878
STATS STARS (4) | 4-1-5 | -1.3 | (0, 20) | 67 | 737 | 04t | 0.933 | 0.871
Winners (4) | 5-0-5 | 3.1 | (2, 20) | 75 | 791 | - | 0.933 | 0.870
Three Musketeers (3) | 5-0-5 | -3.7 | (1, 23) | 81 | 1267 | 01t, 05t | 0.932 | 0.869

Here's a comparison of the estimates made by The R Group and The Three Musketeers...

![](https://github.com/THOMASELOVE/431-2021/blob/main/classes/class02/images/class02_photo_plot.png)

6. Dr. Love will be away next Tuesday 2021-08-31, so Class 03 will be a pre-recorded Lecture. You will receive instructions on how to watch Class 03 soon, via email and via Piazza. 

7. Next Thursday's Class 04 will be a working session using R to do several things that will be especially helpful in preparing your responses to Lab 01 and also for Lab 02, so it would be helpful to bring a laptop next Thursday with R running on it, if you can.

8. Our [Software Tutorials page](https://github.com/THOMASELOVE/431-2021/blob/main/software/README.md) links to lots of useful resources like the introverse, and we recommend you take some time this weekend to get R installed and start getting up to speed. For example, there is a new R package and set of tools developed by Stephanie Spielman and colleagues called the [introverse](https://spielmanlab.github.io/introverse/articles/introverse_online.html) which is another way to get some help with basic ideas in R and the tidyverse that we'll be discussing through the semester. Here's a [quote from the introverse's page on Github](https://spielmanlab.github.io/introverse/index.html):

> The [introverse package](https://spielmanlab.github.io/introverse/index.html) provides alternate documentation for commonly-used functions and concepts in Base R and in the tidyverse. The provided resources are meant to complement, not replace official documentation and existing R resources. Therefore, the goal of the introverse is to provide beginner-oriented help for most introductory topics within R and the tidyverse, not to provide comprehensive help about using all of R. We hope introverse can help you (and/or your students!) get up-and-running within R and the tidyverse, so that once you get your bearings you can eventually “graduate” from the introverse and take advantage of the official comprehensive documentation/resources.
 
-----------------

## One Last Thing

The 4-minute video from Hans Rosling I wanted to share with you last time is to be found at http://bit.ly/431-rosling. We'll see if I get there today.

