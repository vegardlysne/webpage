---
title: "RStudio::conf2019 notes"
author: "Vegard"
date: "17-18 januar 2019"
output: 
  html_document:
    toc: true
    toc_depth: 2
    toc_float: true
    theme: darkly
---



These are my personal notes from RStudio::conf2019. Links to the slides are pointing to the presenters personal sites, and the video links are pointing to [RStudio.com](https://resources.rstudio.com/rstudio-conf-2019). 

Return to [home](/).

# Keynotes

---

## Shiny in production: Principles, practices, and tools

### **Joe Cheng**, *RStudio*

#### Abstract
> Shiny is a web framework for R, a language not traditionally known for web frameworks, to say the least. As such, Shiny has always faced questions about whether it can or should be used “in production”. In this talk we’ll explore what “production” even means, review some of the historical obstacles and objections to using Shiny for production purposes, and discuss practices and tools that can help your Shiny apps flourish.

#### Resources

- [Slides](https://speakerdeck.com/jcheng5/shiny-in-production)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/shiny-in-production-principles-practices-and-tools-joe-cheng?wvideo=za2lalvz9e"><img src="https://embedwistia-a.akamaihd.net/deliveries/cf40e9636e70dc6a768a99e122137b64.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Use *profvis* to see where your code is slow, do **not** guess!
- Can be accessed through the profile menu

---

## Explicit Direct Instruction in Programming Education

### **Felienne**, *Leiden University*

#### Abstract 
> In education, there is and has always been debate about how to teach. One of these debates centers around the role of the teacher: should their role be minimal, allowing students to find and classify knowledge independently, or should the teacher be in charge of what happens in the classroom, explaining students all they need to know? These forms of teaching have many names, but the most common ones are exploratory learning and direct instruction respectively. While the debate is not settled, more and more evidence is presented by researchers that explicit direct instruction is more effective than exploratory learning in teaching language and mathematics and science. These findings raise the question whether that might be true for programming education too. This is especially of interest since programming education is deeply rooted in the constructionist philosophy, leading many programmers to follow exploratory learning methods, often without being aware of it. This talk outlines this history of programming education and additional beliefs in programming that lead to the prevalence of exploratory forms of teaching. We also explain the didactic principles of direct instruction, explore them in the context of programming, and hypothesize how it might look like for programming.

#### Resources

- [Home page](http://www.felienne.com/)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/opening-keynote-day2?wvideo=5w7gllfav7"><img src="https://embedwistia-a.akamaihd.net/deliveries/89a0fcd1039a6da371dd52afc864e395.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

> "Everyone should learn programming"
>
> --- Every programmer ever

- Spreadsheets (Excel) are a great programming tool, people are programming without knowing they are programming. They are accidentally doing JAVA.
- PhD thesis: Spreadsheets are code
    - Spreadsheets are pure functional and reactive programming
- How to teach?
    - Tell/show vs let others explore themselves

---

## The unreasonable effectiveness of public work

### **David Robinson**, *DataCamp*

#### Abstract 
> In this talk, I'll lay out the reasons that blogging, open source contribution, and other forms of public work are a critical part of a data science career. For beginners, a blog is a great accompaniment to data science coursework and tutorials, since it gives you experience applying practical data science skills to real problems. For data scientists at any stage of their careers, open source development offers practice in collaboration, documentation, and interface design that complement other kinds of software development. And for data scientists more advanced in their careers, writing a book is a great way to crystallize your expertise and ensure others can build on it. All of these practices build skills in communication and collaboration that form an essential component of data science work. Each also lets you build a public portfolio of your skills, get feedback from your peers, and network with the larger data science community.

#### Resources

- [Slides](bit.ly/drob-rstudio-2019)
- Homepage: [Variance Explained](www.varianceexplained.org)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/the-unreasonable-effectiveness-of-public-work?wvideo=fw13ubysfe"><img src="https://embedwistia-a.akamaihd.net/deliveries/90292924b172a1ca5091a5dff8e806db475a8a52.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

##### Notes

- Everything you share is much more valuable than everything still in your computer
- Why spend time on public work?
    - Advance your career
    - Practicing good habits
    - Contribute to the community
- Blog
    - Public portfolio
    - Practice writing, visualization and communication
    - Blogdown, 1 markdown file per post
    - Twitter #datablog
- Contribute to open source
- Give conference talks
    - Share your slides
    
---

# Session 1: Tidyverse 1  

---

## A guide to modern reproducible data science with R

### **Karthik Ram**, *rOpenSci*

#### Abstract 
> Have you ever had a challenging time cloning someone's data analysis repo and easily re-running the analysis without fiddling with missing packages, mismatched versions, external dependencies, unavailable data or a whole host of other issues? Would you like your own work to be reproducible where someone else can access your data, code, workflow, models and provenance and easily re-create your results without consulting you? Then this is the talk for you.

#### Resources

- [Slides](http://github.com/karthik/rstudio2019)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/a-guide-to-modern-reproducible-data-science-with-r?wvideo=ai29cy0lcj"><img src="https://embedwistia-a.akamaihd.net/deliveries/2e2a0413e013d730f505df2e81f9e83c132b0def.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

Make a  research compendium!

- Principle
    - Keep data, methods and outputs separate
- R Package format is great for compendiums
    - Description file is key to manage dependencies etc
    - Take advantage of devtools etc

- Data
    - Small data goes inside the package/compendium
    - Large data - _piggyback_ package
    - Medium data - _arkdb_ package
- Computing environment
    - Isolate 
- Workflows
    - data - analyses - output

---

## Solving R for data science

### **Jeffrey Arnold**, *Insight*

#### Abstract 
> While teaching a course using "R for Data Science", I wrote a complete set of solutions to its exercises and posted them on GitHub. Then other people started finding them. And now I'm here. In this talk, I'll discuss why I did it, and what I learned from the process, both what I learned about the tidyverse itself, and what I learned from teaching it.

#### Resources

- [Solution manual for the R4DS book](https://github.com/jrnold/r4ds-exercise-solutions)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/solving-r-for-data-science?wvideo=phgisauwt0"><img src="https://embedwistia-a.akamaihd.net/deliveries/8b22fe0e7f66b60588e6968b65b0f9f0.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Box plots: A case study in debugging and perseverance

### **Kara Woo**, *Sage Bionetworks*

#### Abstract 
> Come on a journey through pull request #2196. What started as a seemingly simple fix for a bug in ggplot2's box plots developed into an entirely new placement algorithm for ggplot2 geoms. This talk will cover tips and techniques for debugging, testing, and not smashing your computer when dealing with tricky bugs.

#### Resources

- [Slides](https://github.com/karawoo/2019-01-17-rstudioconf)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/box-plots-a-case-study-in-debugging-and-perseverance?wvideo=f2o2awcdyg"><img src="https://embedwistia-a.akamaihd.net/deliveries/3d1be05754efc4f0d1f0d9a35f27b957cb04aa3f.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- What is the bug?
    - Isolate the problem
    - `reprex` - minimal reproducible example
    - `debug()` - look through what happens when a function is called
- How to fix it?
    - Experiment
    - Test many different scenarios
    - Make it generalisable
* When are you done fixing?
    - More testing, don't let the perfect be the enemy of good enough

---

## Working with categorical data in R without losing your mind

### **Amelia McNamara**, *University of St. Thomas*

#### Abstract 
> Categorical data, called “factor” data in R, presents unique challenges in data wrangling. R users often look down at tools like Excel for automatically coercing variables to incorrect datatypes, but factor data in R can produce very similar issues. The stringsAsFactors=HELLNO movement and standard tidyverse defaults have moved us away from the use of factors, but they are sometimes still necessary for analysis. This talk will outline common problems arising from categorical variable transformations in R, and show strategies to avoid them, using both base R and the tidyverse (particularly, dplyr and forcats functions).

#### Resources:

- [Slides](http://www.amelia.mn/WranglingCats.pdf)
- Webpage: [Practical data science for stats](https://peerj.com/collections/50-practicaldatascistats/)!
- Paper: [Wrangling categorical data in R](https://peerj.com/preprints/3163.pdf)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/working-with-categorical-data-in-r-without-losing-your-mind?wvideo=ro2esg1sih"><img src="https://embedwistia-a.akamaihd.net/deliveries/6e6343cb981056d51e78503bd33938bf.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes:

- R handles categorical data as factors
    - A set of values + ordered set of valid levels
- StringsAsFactor defaults to TRUE in base R, but not in tidyverse (read_...)
- We still need factors, but they must be treated with care
    - Base R methods of handling factors is __bad__, and very sensitive to small typos, mismatching of levels/values etc
    - _forcats_ fixes things!
    - run a _summary()_ or similar before and after, defensive coding
    - _assertthat_ and _testthat_ also useful

---

# Session 2: Teaching 1  

---

## R4DS online learning community: Improvements to self-taught data science & the critical need for diversity, equity, and inclusion in data science education

### **Jesse Mostipak**, *Teaching Trust*

#### Abstract 
> The first iteration of the R4DS Online Learning Community was created as an online space for learners and mentors to gather and work through the "R for Data Science" text in a collaborative and supportive environment. The creation of this group was inspired by my own success in transitioning to a career in data science coupled with the resources that I wanted to see in the R programming space. This talk will go through the learnings of creating an online learning space focused on R programming for data science, and how future iterations of similar groups can more proactively center on bringing about diversity, equity, and inclusion to data science spaces.

#### Resources

- [Material](https://github.com/jrnold/r4ds-exercise-solutions)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/r4ds-online-learning-community-improvements-to-self-taught-data-science-and-the-critical-need-for-diversity-equity-and-inclusion-in-data-science-education?wvideo=d4j1ycc1oa"><img src="https://embedwistia-a.akamaihd.net/deliveries/e0d6bf2fffa079155305fe50ada7f540cb07747f.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Teaching data science with puzzles

### **Irene Steves**

#### Abstract 
> Of the many coding puzzles on the web, few focus on the programming skills needed for handling untidy data. During my summer internship at RStudio, I worked with Jenny Bryan to develop a series of data science puzzles known as the "Tidies of March." These puzzles isolate data wrangling tasks into bite-sized pieces to nurture core data science skills such as importing, reshaping, and summarizing data. We also provide access to puzzles and puzzle data directly in R through an accompanying Tidies of March package. I will show how this package models best practices for both data wrangling and project management.

#### Resources

- [Slides](https://github.com/isteves/ds-puzzles)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/teaching-data-science-with-puzzles?wvideo=879kq2ra62"><img src="https://embedwistia-a.akamaihd.net/deliveries/33299cbdc427636c4faae650dd96ff081f1712d6.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Introductory statistics with R: Easing the transition to software for beginner students

### **Kelly Nicole Bodwin**, *California Polytechnic State University*

#### Abstract
> In this talk, we will present our approach to incorporating R and RStudio into a 10-week introductory statistics course for non-majors Cal Poly. Our primary contribution will be to share a series of Shiny Apps, created to ease students with no statistical or coding background into the philosophy of using programming tools to explore data. Our program was recently used in 3 sections of 35 students each this Fall, during which students were surveyed regularly for their reactions to the approach. We will demonstrate our new tools, discuss our successes and failures, share student-generated output, and summarize the results of our Fall survey.

#### Resources

- [Slides](https://web.calpoly.edu/~kbodwin/RStudio_2019.html)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/introductory-statistics-with-r-easing-the-transition-to-software-for-beginner-students?wvideo=ery025plib"><img src="https://embedwistia-a.akamaihd.net/deliveries/90eff02f7c4d5b22ac941763d639e446.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Teaching R using inclusive pedagogy: Practices and lessons learned from over 700 Carpentries workshops

### **Tracy Teal**, *The Carpentries*

#### Abstract
> The Carpentries is an open, global community teaching researchers the skills to turn data into knowledge. Since 2012 we have taught 700+ R workshops & trained 1600+ volunteer instructors. Our workshops use evidence-based teaching, focus on foundational and relevant skills and create an inclusive environment. Teaching the tidyverse allows learners to start working with data quickly, and keeps them motivated to begin and sustain their learning. Our assessment show that these approaches have been successful in attracting diverse learners, building confidence & increasing coding usage. Through our train-the-trainer model and open, collaborative lessons, this approach scales globally to reach more learners and further democratize data.

#### Resources

- [Slides](https://docs.google.com/presentation/d/1yZTOcm0hO3sq8nz24luNoxL2Tk4IWfwoeYSXa09-zB8/edit#slide=id.g4d9835a148_0_218)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/teaching-r-using-inclusive-pedagogy-practices-and-lessons-learned-from-over-700-carpentries-workshops?wvideo=7otea2f3u0"><img src="https://embedwistia-a.akamaihd.net/deliveries/455839407f686a7a03fd54d4e8abfeeb89be18a8.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

# Session 3: Tidyverse 2  

---

## Melt the clock: Tidy time series analysis

### **Earo Wang**, *Monash University*

#### Abstract 
> Time series can be frustrating to work with, particularly when processing raw data into model-ready data. This work presents two new packages that address a gap in existing methodology for time series analysis (raised in rstudio::conf 2018). The tsibble package supports organizing and manipulating modern time series, leveraging tidy data principles along with contextual semantics: index and key. The tsibble data structure seamlessly flows into forecasting routines. The fable package is a tidy renovation of the forecast package. It promotes transparent forecasting practices and concise model representations, to empower analysts tackling a broad domain of forecasting problems. This collection of packages form the tidyverts, which facilitates a fluent and fluid workflow for analyzing time series. 

#### Resources

* [Slides](www.slides.earo.me/rstudioconf19)
* Web page: [Tidyverts](www.tidyverts.com)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/melt-the-clock-tidy-time-series-analysis?wvideo=iz2jrbq0nm"><img src="https://embedwistia-a.akamaihd.net/deliveries/524f53ce8b8608c3919787776cb1878c.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

3 main ideas

* tsibble
    - _**time series tibble**_
    - tidy and transform
    - _index variable_ represents time
    - _key variable_ identify variables that define series, or entities over time, individual id of related observations
    - `has_gaps()`, `scan_gaps()`, `count_gaps()` and `fill_gaps()` explore missing observations
    - `index_by()`
    - `slide()`, `tile()` and `stretch()`, creates rolling functions, structured like purrr functions. 
        - `slide()`, `slide2()`, `pslide()`, and with type-stable suffixes like `slide_dbl()`, `slide_chr()` etc 
    
- mable
    - _**model table**_
    - model the data
    - inspect with `tidy()`, `glance()` and `augment()`

- fable
    - _**forecast table**_
    - tidy forecasting 
    - "fables are never true, but tells you something useful"
    - ggplot implementation: _geom_forecast()_
    
**Key** is the key to extract values across tsibble, mable and fable

---

##  3D mapping, plotting, and printing with rayshader

### **Tyler Morgan-Wall**, *Institute for Defense Analyses*

#### Abstract 
> Is there ever a place for the third dimension in visualizing data? Is the 3D pie chart truly bad, or just misunderstood? In this talk, I will show you how you can create beautiful 3D maps and visualizations with the rayshader package. In addition, I will talk about the value of 3D plotting, how interactions with the R community helped drive the development of rayshader, and how writing/blogging about your projects can vastly improve your code. And, of course—lots of beautiful 3D maps and figures.

#### Resources

- [Homepage](www.tylermw.com)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/3d-mapping-plotting-and-printing-with-rayshader?wvideo=rqe461mc6z"><img src="https://embedwistia-a.akamaihd.net/deliveries/6ae49f2cf01491080771ae662a4ec8c6.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- What is RayShader
    - package to create maps directly from elevation data
    - Only uses base R matrix
    - Can be exported to a 3D printable format!
    - 3D ggplot is coming!
- Should you be scared of 3D plots?
    - 3D is used successfully to illustrate things like landscape, physical objects etc
    - 3D engages people
    
---

## gganimate live cookbook

### **Thomas Lin Pedersen**, *RStudio*

#### Abstract 
> Animation of data visualisation is becoming increasingly popular both as an attention grabber on social media and as a way to tell small data stories. gganimate is a package that extends ggplot2 for making animations and provides a grammar of animation on top of the grammar of graphics. This talk will quickly introduce gganimate, and then dive into a series of different animation and show how they were made and how they could be changed or expanded.

#### Resources

* [Slides](https://www.data-imaginist.com/slides/rstudioconf2019/assets/player/keynotedhtmlplayer)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/gganimate-live-cookbook?wvideo=jqjhhhkzba"><img src="https://embedwistia-a.akamaihd.net/deliveries/881bcddb51a40912174b09b54a65f4bf.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

# Session 3: Modeling  

---

## Solving the model representation problem with broom

### **Alex Hayes**, *University of Wisconsin, Madison*

#### Abstract 
> The R objects used to represent model fits are notoriously inconsistent, making data analysis inconvenient and frustrating. The broom package resolves this issue by defining a consistent way to represent model fits. By summarizing essential information about fits in tidy tibbles, broom makes it easy to programmatically work with model objects. Combining broom with list-columns results in an especially powerful way to work with many model fits at once. This talk will feature several case studies demonstrating how broom resolves common problems in data analysis.

#### Resources

- [Slides](https://github.com/alexpghayes/workshops_presentations/blob/master/2019-01-18-rstudioconf-broom-talk.pdf)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/solving-the-model-representation-problem-with-broom?wvideo=silfkxh9is"><img src="https://embedwistia-a.akamaihd.net/deliveries/832c41240142f36a8084d511730cf28a9c5baea8.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Different models are represented in different ways (list of all objects, structured differently)
- This is hard to work with
- Broom standardises model output
    - `tidy()`summarizes information about fit components
        - modifiable output
    - `glance()` reports goodness of fit values, always a one-row summary
    - `augment()` add information about observations, like predictions etc
- Use cases:
    - By combining `tidy()`and `knitr::kable()`, you can produce nice and quick model output
    - by using `map_df()`, a list of model fits and `glance()`, you can easily compare different model fits
    - Inspecting model information with `nest()`, `tidy()`/`glance()` and `unnest()`, before passing the result to `ggplot()`

---

## parsnip: A tidy model interface

### **Max Kuhn**, *RStudio*

#### Abstract 
> parsnip is a new tidymodels package that generalizes model interfaces across packages. The idea is to have a single function interface for types of specific models (e.g. logistic regression) that lets the user choose the computational engine for training. For example, logistic regression could be fit with several R packages, Spark, Stan, and Tensorflow. parsnip also standardizes the return objects and sets up some new features for some upcoming packages.

#### Resources

- [Slides](https://github.com/rstudio/rstudio-conf/tree/master/2019/Parsnip--Max_Kuhn)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/parsnip-a-tidy-model-interface?wvideo=xs5oz0b7p2"><img src="https://embedwistia-a.akamaihd.net/deliveries/7283540419338367c2732f4a2d4c434c5cdefaed.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Lots of different problems when using different R packages for modeling. Makes it hard to go from model to model to do different things. 
- Parsnip features (white carrot)
    - Creates a unified interface to models
    - Organizes models by tyoe
    - Generalize how to fit models
    - Tidy interface
    - Returns predictable objects

Workflow:

- Parsnip defers computation until specific points, just like ggplot
- Create a model and specify
    - You most often don't need the data for specification of the model
- Set computational engine with `set_engine()`, e.g. "lm", and parsnip knows how to translate your input into the arguments of the model
- Prediction
    - You always get the exact same number of rows back, making it easy to bind predictions to the original data frame
    - When predictions returns more values, `multi_predict()` returns a list column!

---

## Visualizing uncertainty with hypothetical outcomes plots

### **Claus Wilke**, *The University of Texas at Austin*

#### Abstract 
> Uncertainty is a key component of statistical inference. However, uncertainty is not easy to convey effectively in data visualizations. For example, viewers have a tendency to interpret visualizations of the most likely outcome as the only possible one. Viewers may also misjudge the likelihood of different possible outcomes or the extent to which moderately rare outcomes may deviate from the expectation. One way in which we can help the viewer grasp the amount of uncertainty present in a dataset is by showing a variety of different possible modeling outcomes at once. For example, in a linear regression, we could plot a number of different regression lines with slopes and intercepts drawn from the range of likely values, as determined by the variation in the data. Such visualizations are called Hypothetical Outcomes Plots (HOPs). HOPs can be made in static form, showing the various hypothetical outcomes all at once, or preferably in an animated form, where the display cycles between the different hypothetical outcomes. With recent progress in ggplot2-based animation, via gganimate, as well as packages such as tidybayes that make it easy to generate hypothetical outcomes, we can easily produce animated HOPs in a few lines of R code. This presentation will cover the key concepts, packages, and techniques to generate such visualizations.

#### Resources

- [Slides](https://docs.google.com/presentation/d/1zMuBSADaxdFnosOPWJNA10DaxGEheW6gDxqEPYAuado/edit)
- Paper: [Hypothetical Outcome Plots Outperform Error Bars and Violin Plots for Inferences about Reliability of Variable Ordering.](https://www.ncbi.nlm.nih.gov/pubmed/26571487) 

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/visualizing-uncertainty-with-hypothetical-outcomes-plots?wvideo=8m9hzvc38u"><img src="https://embedwistia-a.akamaihd.net/deliveries/8b966c08ac6371481bdfa04f1efe09d859c1dc5b.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- What does the confidence band around a plotted line really mean?
- It's hard to communicate uncertainty. Plots make certain, but they are not
- Bootstrapping with `bootstrapify(n)` as a dplyr verb
- **library(ungeviz)**
    - In ggplot, you can add _data = bootstrapper(n) , aes(group = .draw)_ to the geom you want to bootstrap!
    - `sampler(n)` functions in the same way as `bootstrapper()`

---

# Session 3: Kaleidoscope  

---

## Getting it right: Writing reliable and maintainable R code

### **Amanda Gadrow**, *RStudio*

#### Abstract
> How can you tell that your scripts, applications, and package functions are working as expected? Are you sure that when you make changes in one part of the code, it won't break something in another part? Have you thought deeply about how the consumers of your code (including Future You) will use it, maintain it, fix it, and improve it? Code quality is essential not only for reliable results but also for your script's maintainability and your users' satisfaction. Quality can be measured in part with targeted testing, and fortunately, there are several effective and easy-to-use code testing tools available in R. This talk will discuss some of the most useful testing packages, covering both concepts and examples.

#### Resources

- [Slides](https://github.com/ajmcoqui/testingRCode)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/getting-it-right-writing-reliable-and-maintainable-r-code?wvideo=wzw1i5d1lb"><img src="https://embedwistia-a.akamaihd.net/deliveries/7da91359d76bfa6ccb7071d41f9a6d71.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes
- Code is a mean of analysis, but also an artifact
- You will most likely run your code again later, and want it to produce the same result and not be broken when other things change, like data input
- You can wait until the code fails in the field, but it's better to test it yourself
- Start with testing the major functions, inputs and integration points
    - Manual tests in the console, but coded tests are better in the long run
- Code that is hard to test is also hard to maintain!
- Design code for ease of testing, i.e. small functions that do few things

---

# Session 4: Programming  

---

## pkgman: A fresh approach to package installation

### **Gabor Csardi**, *RStudio*

#### Abstract
> The main goals of pkgman is to make package installation fast and more reliable. This allows new, simpler and safer workflows, such as separate package libraries for projects. In this talk, we will show the features that make pkgman fast, convenient and reliable. Features that make pkgman fast: * Concurrency: pkgman performs all downloads, package builds and installations concurrently by default. * Metadata and package cache: pkgman caches all metadata and all downloaded and locally built packages in its cache. * Lazyness: pkgman only downloads and installs packages if needed. Features that make pkgman convenient: * BioC and GitHub packages are supported seamlessly. * Informative UI. pkgman can lay out the installation/update plan, that the user needs to confirm. It returns data about downloads, builds, installations, etc. Features that make pkgman reliable: * Dependency solver. pkgman makes sure that you end up in consistent, working state of dependencies. * Private library: pkgman's own dependencies do not affect your regular package library, and vice versa. pkgman does not load any packages from your regular library.

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/pkgman-a-fresh-approach-to-package-installation?wvideo=dlcg2854qk"><img src="https://embedwistia-a.akamaihd.net/deliveries/2dacca3a981c3d6cadf44114cefad3c65aa06fff.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## It depends: A dialog about dependencies

### **Jim Hester**, *Rstudio*

#### Abstract
> Software dependencies can often be a double-edged sword. On one hand, they let you take advantage of others' work, giving your software marvelous new features and reducing bugs. On the other hand, they can change, causing your software to break unexpectedly and increasing your maintenance burden. These problems occur everywhere, in R scripts, R packages, Shiny applications and deployed ML pipelines. So when should you take a dependency and when should you avoid them? Well, it depends! This talk will show ways to weigh the pros and cons of a given dependency and provide tools for calculating the weights for your project. It will also provide strategies for dealing with dependency changes, and if needed, removing them. We will demonstrate these techniques with some real-life cases from packages in the tidyverse and r-lib.

#### Resources
- [Slides](https://speakerdeck.com/jimhester/it-depends)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/it-depends-a-dialog-about-dependencies?wvideo=l9bx1pynpo"><img src="https://embedwistia-a.akamaihd.net/deliveries/2f7f0f565bb5350be1af465af8d2cce6.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Our color of magic: The open sourcery of fantastic R packages
### **Miles McBain**, *ACEMS, Queensland University of Technology*

#### Abstract
> What does it mean to say software is, to quote one Twitter user, ‘so f***ing magical!’? In the context of our popular community hobby of rating and sharing R packages, the term ‘magic’ seems reserved for our most powerful expressions of visceral approval. Why is this? And what does it say about how we value software? Can this magical quality be quantified? We will consider these questions in examination of magical specimens, and in the process reveal the surprising depths at which notions of magic are embedded in the R zeitgiest.

#### Resources
- [Slides](https://github.com/MilesMcBain/rstudioconf_talk)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/our-colour-of-magic-the-open-sourcery-of-fantastic-r-packages?wvideo=lbike53t60"><img src="https://embedwistia-a.akamaihd.net/deliveries/85e49bc14d8e86404efe4fd07c42d66aeef30315.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

# Session 4: Publication  

---

## R Markdown: The Bigger Picture

### **Garrett Grolemund**

#### Abstract
> Statistics has made science resemble math, so much so that we've begun to conflate p-values with mathematical proofs. We need to return to evaluating a scientific discovery by its reproducibility, which will require a change in how we report scientific results. This change will be a windfall to commercial data scientists because reproducible means repeatable, automatable, parameterizable, and schedulable.

#### Resources

- [Slides](https://github.com/garrettgman/rmarkdown-the-bigger-picture)
- Significance: [Cargo-cult statistics and scientific crisis](https://www.significancemagazine.com/science/593-cargo-cult-statistics-and-scientific-crisis)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/r-markdown-the-bigger-picture?wvideo=wblobrq76y"><img src="https://embedwistia-a.akamaihd.net/deliveries/423cab432e3c024859f67fdfb390386e1a2b288e.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Replication crisis
    - 75-90% of preclinical results cannot be replicated
    - A high proportion of landmark studies cannot be replicated
    - Yet, they are part of the scientific consensus and accepted as true
    - This becomes a *credibility crisis* for scientists!
- Statistics/science (hypothesis, best guess) is not math (certain, prove)
    - Estimates based on premises, but cannot prove that the premises corresponds with reality, hence there will always be uncertainty
    - The goal should be to provide a map, not a proof
- RMarkdown as a tool for reproducible science
    - Authoring format for data science

---

## pagedown: Creating Beautiful PDFs with R Markdown + CSS

### **Yihui Xie**

#### Abstract
> The traditional way to beautiful PDFs is often through LaTeX or Word, but have you ever thought of printing a web page to PDF? Web technologies (HTML/CSS/JavaScript) are becoming more and more amazing. It is entirely possible to create high-quality PDFs through Google Chrome or Chromium now. Web pages are usually single-page documents, but they can be paginated thanks to the JavaScript library Paged.js, so that you can have elements like headers, footers, and page margins for the printing purpose. In this talk, we introduce a new R package, [pagedown](https://github.com/rstudio/pagedown), to create PDF documents based on R Markdown and Paged.js. Applications of pagedown includes, but not limited to, books, articles, posters, resumes, letters, and business cards. With the power of CSS and JavaScript, you can typeset your documents with amazing elegance (e.g., a single line of CSS, "tr:nth-child(even) { background: #eee; }", will give you a striped table, and "border-radius: 50%;" gives you a circular element) and power (e.g., HTML Widgets).

#### Resources

- [Slides](https://slides.yihui.name/2019-rstudio-conf-pagedown.html)
- [pagedown guide](https://pagedown.rbind.io/)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/pagedown-creating-beautiful-pdfs-with-r-markdown-and-css?wvideo=oxxk6afhtz"><img src="https://embedwistia-a.akamaihd.net/deliveries/77d268f4eb298d5f472a509610ee3fcf.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Experimental packages, you can't throw away LaTeX and Word yet
- Create paged documents
- New package on CRAN, but better to install from GitHub install_github('rstudio/pagedown')
- New RMarkdown - from template - pagedown
- `pagedown::chrome_print()`, print pages, not yet working very well
- Other formats like posters, letters etc is also supported by adding a different output style in the YAML header

---

## Introducing the gt Package

### **Rich Iannone**, *RStudio*

#### Abstract
> With the gt package, anyone can make great-looking display tables. Though the package is still early in development, you can do some really great things with it right now! I'll walk through a few examples that touch upon the more common table-making use cases. These will include features like adding table parts, integrating footnotes, styling/transforming table cells, using tables in R Markdown documents, and even including gt tables in email messages.

#### Resources

- [Slides](http://github.com/rich-iannone/presentations)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/introducing-the-gt-package?wvideo=d38rerkbwb"><img src="https://embedwistia-a.akamaihd.net/deliveries/f54d2b6ffcb5dcf913e67031d060ea98.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Table data (tibble or data.frame) - GT object - display table
- Structural parts of a display table
    - Column labels
    - stubhead label, rownames header
    - Row group labels
    - Summary
    - Title, subtitle
    - Footnotes and source notes
- workflow

| function | explanation |
|----------|-------------|
| `gt()` | turns your table data into a gt object |
| `tab_functions()`| adds parts to a gt table |
| `fmt_functions()`| formats parts of a table, can specify both columns and rows |
| `ìnfo_functions()`| shows information tables for the different formatting options |
| `tab_options()`| general options for a table appearance |

- The **Blastula** package makes it possible to send the output as email

---

## The lazy and easily distracted report writer

### **Mike K Smith**

#### Abstract
> My brain is lazy, shallow and easily distracted. Learn how I use notebooks to keep my present-self organised, my future-self up to speed with what I was thinking months ago, and also how I use parameterised reports to share results for both quantitative and non-quantitative audiences across multiple endpoints. I can update and render outputs for a variety of outputs from a single markdown notebook or report. I’ll show you how I organise my work using the tidyverse, use child documents with parameterisation and also how this is served out to my colleagues via RStudio Connect.

#### Resources

- [Slides](https://github.com/MikeKSmith/RStudioConf2019)
- Blogpost: [Notebook War](https://yihui.name/en/2018/09/notebook-war/)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/the-lazy-and-easily-distracted-report-writer-using-rmarkdown-and-parameterised-reports?wvideo=5rcz8a683r"><img src="https://embedwistia-a.akamaihd.net/deliveries/24e8b382632eaf8d7684940e920f7026ff07ca4e.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Who is your audience?
    - You right now
    - You in the future
    - Colleagues and others
- If you write more comments than code, use rmarkdown, if you write more code than comments, write more comments    
- Copy/paste 3+ times, write a function
- Write reports over multiple outcomes, use parameterized reports
    - set params in YAML
    - use 'params$...' in the text
    
---

# Session 5: Teaching

---

## Learning from eight years of data science mistakes

### **Caitlin Hudon**, *R-Ladies Austin*

#### Abstract
> Over the past eight years of doing data science, I’ve made plenty of mistakes, and I’d love to share them with you -- including what I’ve learned and what I’d do differently with some hindsight. This talk will cover mistakes made during analyses (including communication when delivering results) team and infrastructure mistakes, plus some advice for incoming data scientists.

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/learning-from-eight-years-of-data-science-mistakes?wvideo=yrw896lf17"><img src="https://embedwistia-a.akamaihd.net/deliveries/6cbdf10bfbbf7ccbcb2a7d351274b1c9.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

## Catching the R wave How R and RStudio are revolutionizing statistics education in community colleges (and beyond)

### **Mary Rudis**, *Penn State Harrisburg*

#### Abstract
> There is no doubt that RStudio has had an impact on how introductory statistics is taught in colleges today. When we consider the sheer dominance that giants like Texas Instruments, IBM, and Pearson Publishing have had in academic curriculum development it’s no small wonder that tools like R and Python have been able to gain a foothold. Projects like DataCamp, ModernDive.com, “Introductory Statistics with Randomization and Simulation” courtesy of openintro.org, Wickham’s “R for Data Science” and Peng’s “R Programming for Data Science” are great resources for the student who has already some fundamental math or statistical background and has become comfortable around computing and applications-driven computational exercises. But many of us know that Data Science cannot simply be relegated to the privileged few that stumble into it by virtue of circumstance. My passion, and the purpose of my talk, is to provide educators with a digestible guidebook that would be appropriate for introduction to statistical concepts in high school, college, and under-resourced schools looking for ways to increase diversity in STEM. Organized in small, adaptable activities designed to be the amuse-esprit enticing both the timid and the skeptical to the proverbial banquet table that is RStudio, this exploration into the world of statistics education should be of interest to a wide audience. My hope is to increase data literacy in real world context – with primary emphasis on descriptive statistics and distributions.

#### Resources
- [Slides](https://github.com/mrshrbrmstr/RStudioConf2019)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/catching-the-r-wave-how-r-and-rstudio-are-revolutionizing-statistics-education-in-community-colleges-and-beyond?wvideo=cxuuu82cdy"><img src="https://embedwistia-a.akamaihd.net/deliveries/fb801b037a3ba36aaa5ebae26b261ed5.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

---

# Session 5: Programming  

---

## vctrs: tools for making size and type consistent functions

### **Hadley Wickham**, *RStudio*

#### Abstract
> vctrs is a new package that provides tools (cognitive and computational) to ensure that functions behave consistently with respect to inputs of varying length and type. The end goal of vctrs is to be invisible to the end user of the tidyverse (simply enabling their predictions about function outputs to be more correct), but will help developers write functions that "just work".

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/vctrs-tools-for-making-size-and-type-consistent-functions?wvideo=8oquvw5eqx"><img src="https://embedwistia-a.akamaihd.net/deliveries/c926c141192ea288ad5dc6a649dcf4e2.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>


#### Notes

- It should be easy to predict what type of thing your function returns
- Base R principles of atomic vectors are a good starting point

|           | Logical   | Integer   | Double    | Character |
|-----------|:---------:|:---------:|:---------:|:---------:|
| Logical   | Logical   | Integer   | Double    | Character | 
| Integer   | Integer   | Integer   | Double    | Character | 
| Double    | Double    | Double    | Double    | Character | 
| Character | Character | Character | Character | Character | 

- Not all data types are connected, and should not be coerced together
    - `vec_c()` gives you an error, unless you specifically tell the function that you want i.e. a character by setting the argument `.ptype = character()`
- Type stability principles
    1. The type of output should only depend on the type of arguments
    2. The order of the input should not affect the output type
    3. It uses consistent rules which is applied everywhere
- Length stability
    - Many different sets of recycling rules of vectors of different length

---

## Lazy evaluation

### **Jenny Bryan**, *RStudio* 

#### Abstract
> The "tidy eval" framework is implemented in the rlang package and is rolling out in packages across the tidyverse and beyond. There is a lively conversation these days, as people come to terms with tidy eval and share their struggles and successes with the community. Why is this such a big deal? For starters, never before have so many people engaged with R's lazy evaluation model and been encouraged and/or required to manipulate it. I'll cover some background fundamentals that provide the rationale for tidy eval and that equip you to get the most from other talks.

#### Resources

- [Slides](https://github.com/jennybc/tidy-eval-context/blob/master/tidy-eval-context.pdf)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/lazy-evaluation?wvideo=l0bdufviin"><img src="https://embedwistia-a.akamaihd.net/deliveries/b0d1583f0da7de06b860f98ec5e51062.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Tidy eval is like starting crossfit or going vegan, you tell people about it
- Tidy eval powers a lot of th emetaprogramming going on within tidyverse, making unquoted variable names work
- Function accepting unquoted variable names must deal with non-standard evaluation
    - Meaning functions wrapping these functions, like `dplyr`
- When direct specification is easy, indirect specification is harder
    - Variable name stored in objects
    - Variables as argument names
- Toolkit in `rlang()` 
    - If only one variable is needed, you don't need tidy eval, pass the dots: *arg = ...* and e.g. *group_by(...)*
    - Otherwise, you'll need `enquo()` and `!!`, and maybe `:=` if you want to name things 

---

## Working with names and expressions in your tidy eval code

### **Lionel Henry**

#### Abstract
> In practice there are two main flavors of tidy eval functions: functions that select columns, such as `dplyr::select()`, and functions that operate on columns, such as `dplyr::mutate()`. While sharing a common tidy eval foundation, these functions have distinct properties, good practices, and available tooling. In this talk, you'll learn your way around selecting and doing tidy eval style.

#### Resources

- [Slides](https://speakerdeck.com/lionelhenry/selecting-and-doing-with-tidy-eval)

#### Video
<p><a href="https://resources.rstudio.com/rstudio-conf-2019/working-with-names-and-expressions-in-your-tidy-eval-code?wvideo=ebj7te6m65"><img src="https://embedwistia-a.akamaihd.net/deliveries/b866337a304ea75d56f980cdf8cbe125.jpg?image_play_button_size=2x&amp;image_crop_resized=960x540&amp;image_play_button=1&amp;image_play_button_color=4287c7e0" width="400" height="225" style="width: 400px; height: 225px;"></a></p>

#### Notes

- Why tidy eval
    - Delay the computation of non-existing objects to another context where the object exists
- Pass the dots to vars(...)
- When you create a function, think about what happens with a grouped tibble

---
