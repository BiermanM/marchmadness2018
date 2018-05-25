# March Madness 2018
Prediction of March Madness 2018 Men's Tournament

The detailed project report can be viewed [here](http://bierman.io/report.pdf).

## Installation Instructions
1.  Install [Apache Spark](https://spark.apache.org/) and [Apache Hadoop](http://hadoop.apache.org/)
2.  Download and install [R v3.4.3](https://cran.rstudio.com)
3.  Download and install [RStudio v1.1.383](https://www.rstudio.com)
4.  In case you have never used the libraries I used in my project, open the R console in RStudio and type the following lines:
    * `install.packages("caret")`
    * `install.packages("SparkR")`
    * `install.packages("dplyr")`
    * `install.packages("magrittr")`
    * `install.packages("tidyr")`
    * `install.packages("ggplot2")`
5.  Open `FullTeamData.rmd` in RStudio
6.  Go to line 11 (it will contain: `currentYear <- 2016`)
7.  Set `currentYear` to the value of `2010` (it should look like: `currentYear <- 2010`)
8.  Knit the file, this will create a `FullTeamData.html` file in the current directory that shows the results and a `FullTeamData2010.csv` file in the Data folder
9.  Repeat steps 8 and 9 for values `2011`, `2012`, `2013`, `2014`, `2015`, `2016`, `2017`, and `2018`
10. Open `Testing.rmd` in RStudio
11. Knit the file (this will take about 20 minutes to complete), this will create a `Testing.html` file that shows the results
12. Open `Submission.rmd` in RStudio
13. Knit the file, this will create a `Submission.html` file that shows the results and `submission_v1.csv`, `submission_v1_forBracket.csv`, `submission_v2.csv`, and `submission_v2_forBracket.csv` in the current directory
14. `submission_v1.csv` and `submission_v2.csv` were the files submitted to the Kaggle competition, `submission_v1_forBracket.csv` and `submission_v2_forBracket.csv` were used to create brackets for the NCAA March Madness Bracket Challenge
15. To view the results of the three R scripts (`FullTeamData.rmd`, `Testing.rmd`, and `Submission.rmd`), open the respective html files that were created in any browser

## * Note *
`FullTeamData.rmd` creates 9 datasets (`FullTeamData2010.csv`, ..., `FullTeamData2018.csv`) that combines all of the data from the 52 datasets given by Kaggle into one dataset for each year. `Testing.rmd` tests six different Logistic Regression models on every year's data, which comes from the datasets created in `FullTeamData.rmd`. `Submission.Rmd` uses the two best Logistic Regression models on the 2018 data to create output files used in the two competitions (Kaggle and NCAA Bracket Challenge).
