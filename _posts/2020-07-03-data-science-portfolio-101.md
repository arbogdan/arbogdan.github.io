---
layout: post
author: Alex Bogdan
title: Data Science Portfolio 101
date: "2020-07-03 11:38:00"
thumbnail: /assets/img/posts/ds-portfolio-101-thumbnail.jpg
thumbnail_author: Lukas Blazek
thumbnail_url: "https://www.pexels.com/@goumbik"
category: Guides
summary: Essential components of a compelling data science portfolio
---

Data science is a field that is advancing at a blistering pace. Even in the midst of a public health & economic downturn, large companies are gleefully hiring laid off data scientists to bolster their ranks (as was the case with my previous employer). Companies that have not already embraced data science solutions or integrated data science into their daily workflow are at best severely behind the curve, and at worst, already have one foot in the grave. We are on the eve of profound breakthroughs in AI enhancements and adoption, with driverless cars already on roadways in Beijing, and autonomous freight trucks completing journeys from California to Pennsylvania unassisted. Similarly, with an exponential rise in demand for telemedicine, I expect vigorous advances in algorithms designed to assist and automate select aspects of diagnostic medicine (with some particularly exciting work taking place at Georgia Tech). 

As someone who has sat on interview committees for data scientist positions of various seniorities, it might surprise you to hear that a prospective employer typically cares more about what you can do than what degree you bring to the table or what grades you received. *To be clear*, you *do* need to demonstrate a strong aptitude for statistics (especially probability theory) and computer science to thrive in data science (unless you want to be the DS equivalent of a script kiddie, in which case you'll never land a respectable job in the field). But as long as you have or learn these skills, there is a place for you in the world of data science. And conveniently, it has never been easier to learn these skills online, *completely free*.

The remainder of this post will be broken down into sections to help align you properly for a career in data science. These include:

* Programming Skills
* Portfolio Components
* Projects, Internships, & Resources


### Programming Skills
Proficiency here is an absolute must. At a minimum, you will be expected to be familiar with either Python or R, and SQL. R is a better language for statistical analysis, however the flexibility and generalizability of Python make it the de facto language for data science. Additionally, all major machine learning/AI packages are published in Python in one form or another. R is typically a language used at this point by OG programmers and statisticians; if you're applying for a job that expects proficiency in R, expect that that is the language of choice for that company. Most companies are moving away from R due to the benefits of Python listed above, but some still cling to it due to legacy systems and the ease of creating dashboards (R Shiny makes prototyping dashboards very rapid, but they tend to be quite brittle and don't scale well with significant increases in concurrent users).

SQL is also essential because you will need to communicate with databases and warehouses, and virtually all companies use some form of RDBMS that leverages a flavor of SQL. The exact dialect of SQL you learn isn't so important, as it's pretty easy to pick up one if you know another. That being said, PostgreSQL is probably the most widely used and would be a strong starting point; MySQL is another option. A bonus (but typically not essential) would be to be familiar with some flavor of NoSQL. Unlike SQL, each dialect of NoSQL can be quite different, as an industry standard has yet to emerge; good options include MongoDB & Apache Cassandra. "Familiarity" here would simply constitute being familiar with the concepts behind a NoSQL database and being able to do simple data queries - no need to be an expert; that's what data engineers are for.

Another important language to be familiar with that no one ever tells you about is Bash/Zsh. Being familiar with whatever powers your terminal (if you're using a Windows machine, give PowerShell a try) is essential for confidently and quickly navigating your machine and automating low-level manual processes. A common example of when Bash would be helpful is when you have a +100 files in location X and want to move them to location Y and also change their names to include a timestamp indicating when they were originally created; this is common when piping daily model output to a static text/csv file. The best way to improve this skill is just to practice doing simple things such as moving/copying/deleting/renaming dummy files.

The last major programmatic tool you'll need familiarity with is Git. Version control (VCS) is an essential concept in the worlds of programming and data science, and you will be expected to know how to interact with GitHub, GitLab, or BitBucket (they are all quite similar, it's really just a matter of preference for yourself and/or your employer; I use GitHub personally). You should get into the habit of starting all new projects using one of the websites listed above (as well as creating a virtual environment for each project), and this is actually where your portfolio should be hosted. This demonstrates that you are familiar with version control, and serves as an organized one-stop shop for all of your projects/work. You can even create a personal website using GitHub, which I highly recommend (and you're viewing right now :D), as this conveys flexibility with ancillary programming languages/frameworks and indicates your ability to adapt to skills adjacent to data science.

Continuous integration and continuous deployment (CI/CD) go hand-in-hand with proper version control. You should be lightly familiar with these topics (TravisCI and CircleCI are viable options) to compliment your understanding VCS.

In addition to all of these things you *should* learn, there are a number of things you *should not*. Specifically, the following languages are either not used in data science, or are so niche that you'd be hard-pressed to find a job worth taking that actually uses them in their day-to-day.
- SAS (pretty much exclusive to finance & healthcare)
- Stata
- SPSS
- Java (I'm sure there are people who would try to make a case here, but Python reigns supreme)
- C/C++ (used in bleeding-edge data science, but this sort of work would expect you to have a PhD in CS/Math/Stats and be superrr math-oriented)

None of the above languages are worth your time if your goal is to become a data scientist. You could learn Scala, but that's more of a data engineering language. You could also learn Julia, however adoption of this language has been fairly slow and I honestly don't think it's going to catch on versus something like Python.

Lastly, you should also be familiar with basic file/data types common to data science, such as .csv, .json, .yaml/yml, and .txt.

### Portfolio Components
Ultimately, the theme/topic of your portfolio can be whatever you want, and should ideally be something you're interested in or passionate about. For example, I write financial trading algorithms for work and as a side project. I have either written or am writing code to do everything listed below to aid me in this project. These are the main pillars of any data science project.

##### ETL (Extract, Transform, Load) Pipeline
An ETL pipeline demonstrates the following:
- You can identify external data sources (e.g an API) or databases and communicate efficiently with them
- You can ingest unstructured/messy data and conduct all of the tasks necessary to convert it into something usable for statistical analysis
- These tasks include:
    - Reshaping the data into a desirable/workable format
    - Checking that the data contain the number of rows/columns/dimensions that were expected and modifying it if necessary
    - Checking/changing data types to conform to requirements
    - Identifying extreme/unusual/missing values and conducting appropriate actions to address these
    - Upon successful cleaning, loading your shiny new data into a database where it will live until you conduct your analyses
    - Implementing logging output and error handling to accompany all of this

It's important to note that, in a perfect world, you would not need to create an ETL pipeline as a data scientist; this is a task that is squarely in the domain of a data engineer. However, most employers (save the biggest names) continue to have an amorphous vision of what a data scientist is and should be. Because of this, you will often find yourself doing tasks related to data science, with this unequivocally being top among them.

##### Exploratory Data Analysis (EDA)
EDA demonstrates the following:
- You can generate summary statistics for your data and *know what summary statistics are appropriate based on your data type*
- You can generate appropriate bivariate statistics based on data types
- You can generate simple graphics to visualize relationships (in Python, matplotlib/plotly is the de facto viz library; in R, ggplot2)

##### Feature Engineering & Dimensional Reduction
These demonstrate the following:
- You can think critically about the data you have and apply domain expertise to synthesize new features
- You can take a data set of, say 200 variables, and distill it down to 10-20 of the most influential features using something like PCA, LASSO, Ridge Regression, etc.
- You don't just blindly throw everything at your model

##### Model Selection & Validation
These demonstrate the following:
- You know what models are appropriate for a given analysis (e.g. Logistic regression for binary classification, XGBoost Regressor for a continuous outcome)
- You know how to conduct a train, test, validation split of your data (ideally also using K-fold cross validation (CV))
- You know how to conduct hyperparameter tuning to optimize your models (if you can learn Bayesian optimization, huge bonus points; Facebook has a great framework for this called [AX](https://ax.dev/))
- You know how to compare the performance of models and make an informed & practical decision about which is optimal. "Practical" meaning that if Model A has an accuracy of 89% and trains in 1 hour, and Model B has an accuracy of 91% and trains in 1 day, you have to be able to decide which is better by balancing business requirements & statistics.
- You know how to interpret all of the metrics being used to quantify the performance of your models. To be clear, some models (e.g. neural networks) are not easily explainable. What I'm referring to here is being able to explain accuracy, recall, precision, informedness, markedness, etc.

##### Dashboard
This demonstrates the following:
- You are able to create a visual that is usable by technical (or non-technical) end users
- You can link the output of statistical models/analyses into a visually pleasing/usable interface to aid in disseminating your findings

### Projects, Internships, & Resources
As mentioned above, the projects should be something you're passionate about. This will both sustain your enthusiasm (these projects can easily take months) and will make it much easier for you to describe your work to a prospective employer during an interview. Unless you're planning to apply to a very niche job (e.g. a high frequency algorithmic trading firm), your employer will probably not care too much about what the specific topic of the project is, but rather that it demonstrates what I have outlined above.

In terms of internships, I can't really offer much insight here. I had a lot of academic/work experiences related to data science that supplanted the need for an internship. I would suggest googling some of the big names in the tech world (e.g. Apple, Google, Facebook, Uber, Twitter, Reddit, Amazon, Netflix, etc.) and seeing what they have to offer. If you have a particular industry in mind that you're interested in, that would also be a good place to look.

For resources, you'll often find that the best resources available are the documentation pages for the packages themselves. Most have a "Getting Started" page as well as rich examples to help you learn. I would point you toward the following:
- [Kaggle](https://www.kaggle.com/): This site is 100% essential if you're new to data science. You'll find project inspiration, competitions, tutorials, information on new algorithms, and tons of example code that people have written and freely share aimed at beginners like yourself. 
- [Pandas](https://pandas.pydata.org/): De facto library for data manipulation and basic analysis in Python. Essential to master if you want to be a data scientist
- [Matplotlib](https://matplotlib.org/): De facto visualization library for Python
- [Dashboarding Intro](https://towardsdatascience.com/build-a-web-data-dashboard-in-just-minutes-with-python-d722076aee2b?gi=53d1694ce44): Medium article with a light intro to creating a dashboard in Python
- [Sci-kit Learn](https://scikit-learn.org/stable/index.html): De facto Python library for machine learning
- [Tensorflow](https://www.tensorflow.org/): Google's library for Deep Learning (e.g. neural networks)
- [PyTorch](https://pytorch.org/): Facebook's library for Deep Learning (I prefer this one over Tensorflow)
- [OpenAI](https://spinningup.openai.com/en/latest/): Excellent resource for Reinforcement Learning (this is cutting-edge data science; the stuff that powers driverless car AI and things like that. This will require a deeper appreciation for statistics)

### Concluding Remarks
The content above should serve as a solid starting point for anyone looking to build a career in data science. I'm sure there are things I've missed, and please feel free to add comments if you believe there is something essential that should be included. Also understand that, depending on what subset of data science you're interested in breaking into, some of the items above may not apply to you, or may be quite different than what I've described above. For example, if your desire is to work in computer vision, EDA is going to look *very* different for you. What I've provided is a recipe for a well-rounded generalist, who, upon mastering the skills above, can begin to branch out and become an S-Tier specialist. Happy coding!