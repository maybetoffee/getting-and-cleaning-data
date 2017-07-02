##Preliminaries
###Firstly we should install the packages
<br>packages <- c("data.table", "reshape2")</br>
<br>sapply(packages, require, character.only = TRUE, quietly = TRUE)</br>
###and see the working directory
path<-getwd()
path
##get the data
url <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
f <- "Dataset.zip"
if (!file.exists(path)) {
  dir.create(path)
    }  
download.file(url, file.path(path, f))
