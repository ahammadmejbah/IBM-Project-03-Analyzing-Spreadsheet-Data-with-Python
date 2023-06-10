<div align="center">
      <h1> <img src="https://github.com/ahammadmejbah/IBM-Project-02-Transform-Photos-to-Sketches-and-Paintings-with-OpenCV/blob/main/Additional%20Files/SN_web_lightmode.svg" width="300px"><br/>IBM Project 03 Analyzing Spreadsheet Data with Python</h1>
     </div>


# Description
About Spreadsheets are computer programs that allow users to enter, view, and change information in a gridlike format. One of the most useful programs on a PC is a spreadsheet, which allows users to organize data in tabular form. A spreadsheet's primary purpose is to store numerical data and sometimes a few words of text.

# Features
# Analyzing Spreadsheet Data with Python

Estimated time needed: **40 minutes**

We've all been there: sitting at the computer, a cup of coffee in hand, ready to begin the day by tackling a spreadsheet. But once we open it, all we see are numbers upon numbers staring back at us. It can be a little intimidating tackling these numbers, especially with larger spreadsheets, but not to worry! With a few tricks up its sleeve, Python is here to give us a hand!

Interested in learning more about this? Well, you're at the right place!

In this project, we'll be giving you an introduction to the tools that you can use to load spreadsheet data into Python, manipulate it, and write it back to the original file.

## What You'll Need

You should be familiar with basic concepts of computer programming and the syntaxes of Python programming language. This refers to the concept of list, dictionary, function, class, instance variable, method, etc.

## What You'll Learn

After completing this guided project, you will be able to:

1.  Understand the definition of a dataset.
2.  Understand the concept of Cell and Sheets in spreadsheet.
3.  Load a sheet in an `xlsx` or `xls` file to Python.
4.  Perform basic spreadsheet operations such as subsetting, filtering, calculating column mean, median, max and mean, etc.
5.  Write to a sheet in an `xlsx` or `xls` file from Python.

## Exercise 1: Let's Define Data!

So, let's talk about data. We've been throwing this term around a lot: analyzing *data*, manipulating *data* and writing *data*. What exactly is this "data?

Data is defined as "a collection of numbers, characters, images or other items that provide information of something" (SDM, 3rd CE, Deveaux et al.). In statistical sciences, we store data in files that records *cases* and *variables*:

![image](https://github.com/ahammadmejbah/IBM-Project-03-Analyzing-Spreadsheet-Data-with-Python/assets/56669333/d341ef39-5461-41a0-aa87-1327da880f12)


As shown in the table above, each entry is called a *case*, and each *case*  includes value(s) for *variable*(s). Cases are often deleted due to missing data.


## Exercise 2: Explore a Spreadsheet!

Now that we know the definition of data, we can dive into a spreadsheet!

A spreadsheet is a computer application for organization, analysis, and storage of data in tabular form. `xlsx` and `xls` are the two most popular formats for spreadsheet files. They can be created, opened, and saved using spreadsheet applications such as Microsoft Office Excel and Google Sheets.

![image](https://github.com/ahammadmejbah/IBM-Project-03-Analyzing-Spreadsheet-Data-with-Python/assets/56669333/abf96391-43d7-4554-aff3-7a261f59dabc)



``` python
import requests
import os

if not os.path.isfile("./Airport_Data.xlsx"):
    r = requests.get("https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/analysing-spreadsheet-data-with-python/Airport_Data.xlsx")
    f = open("./Airport_Data.xlsx", mode = "wb+")
    f.write(r.content)
    f.close()

```

To load the spreadsheet into Python, we can use pandas's `read_excel()` function. When calling this function, you'll need to specify:

*   The path to the `xls` or `xlsx` file, and
*   The name of the sheet in which you wish to load into Python.

Both will be passed in format of the string.


``` python
import pandas as pd

df_facilities = pd.read_excel("./Airport_Data.xlsx", sheet_name="Facilities")


```


# Author(s)

[Weiqing Wang](https://www.linkedin.com/in/weiqing-wang-641640133/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkQuickLabsanalysingspreadsheetdatawithpython28639550-2022-01-01)

Weiqing is a Data Scientist intern at IBM Canada Ltd. Weiqing holds an Honours Bachelor of Science from the University of Toronto with two specialist degrees, respectively in computer science and statistical sciences. He is presently working towards a graduate degree in computer science at the University of Toronto.

## Other contributors

Kathy An, Yasmine Hemmati

# Change Log

| Date (YYYY-MM-DD) | Version | Changed By   | Change Description       |
| ----------------- | ------- | ------------ | ------------------------ |
| 2021-08-10        | 1.0     | Weiqing Wang | Initial Version Created. |


© IBM Corporation 2021. All rights reserved.

<!-- </> with 💛 by readMD (https://readmd.itsvg.in) -->
    
