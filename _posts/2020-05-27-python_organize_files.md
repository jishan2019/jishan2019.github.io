---
title: "How to organizing files using Python"
date: 2020-05-27
tags: [Python, os, organize, office]
header:
  image: "/images/.jpg"
excerpt: "Python, os, organize, office"
mathjax: "true"
---


In this article, we will talk about how to **create** and **write** new files in Python, and how to **organize** the existing files on the hard drive. The tasks will include:\
1. Print out the files and folders in a specific dirctory
2. Traverse, search, and get the information of the files
3. Create temparary files and folders
4. Create multiple files and folders

## 1. Symbol "/" and "\n"

#### In windows, '\n' is used for separation, while "/" is used in Mac and Linux.


```python
import os
print(os.getcwd())
print(os.path.join('02 working on','01 office'))
```

    C:\Users\...\01 office


## 2. Print out all files and folders under the current working directory


```python
print(os.listdir())

for item in os.listdir():
    print(item)
```

    ['.ipynb_checkpoints', '01.py', '01OS.ipynb', 'Markdown in Jupyter Notebook-Copy1.ipynb', 'newfolder']
    .ipynb_checkpoints
    01.py
    01OS.ipynb
    Markdown in Jupyter Notebook-Copy1.ipynb
    newfolder


#### If we want to print the absolute or relatice path with 'os.listdir()' in Window, we have to write the code as following:


```python
print(os.listdir('C:\\Users\\...\\01Projects\\'))
```

    ['.idea', '01Interesting_projects', '02Course_projects', '03github', '04Textbook_projects', 'SMS_spam']


#### The following codes show how to check if it is a file or a folder:

* Method 1


```python
files = os.listdir()
for file in files:
    print(file,os.path.isdir(file))
```

    .ipynb_checkpoints True
    01.py False
    01OS.ipynb False
    Markdown in Jupyter Notebook-Copy1.ipynb False
    newfolder True


* Method 2


```python
for file in os.scandir():
    print(file.name,file.path,file.is_dir())
```

    .ipynb_checkpoints .\.ipynb_checkpoints True
    01.py .\01.py False
    01OS.ipynb .\01OS.ipynb False
    Markdown in Jupyter Notebook-Copy1.ipynb .\Markdown in Jupyter Notebook-Copy1.ipynb False
    newfolder .\newfolder True


## 3. Traverse, search, and get the information of the files


```python

```
