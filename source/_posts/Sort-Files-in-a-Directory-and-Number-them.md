---
title: Sort Files in a Directory and Number them
date: 2016-11-10
---

# DAY 10 👾 

### I'm back 💙

#### Exam days are ahead of me & I don't have a hard copy to read from & ebooks for Digital Signal Processing (DSP) suck, atleast those I have. So, today I clicked some pics in my phone & as per the naming convention of my phone they are long strings like `IMG_20164144090.jpg` & so on... Now I want to sort them all & number them so that final result is `1.jpg`. I have 2 languages for automating this task `BASH` & `PYTHON`. I'll go with `PYTHON` as this usecase is more suitable for it.

### Here's the final [Python Script](https://github.com/deadcoder0904/personal-bash-scripts/blob/master/sortAndOrderFiles.py) 

#### Firstly, I'll import all the modules I need, i.e, `os` module & `shutil` module

## `os` module to change directories, get files in the directory & to get current working directory

## `sh` module to copy file from one directory to another directory

# Following is the Code with Explanation above each line

{% vimhl python true %}
# Import `os` & `shutil` module
import os, shutil

# Get Current Working Directory
search_dir = os.getcwd()

# Goto that Directory
os.chdir(search_dir)

# List Files in the Directory, don't list Subdirectories
files = filter(os.path.isfile, os.listdir(search_dir))

# For each file, store it in an `files` list
files = [os.path.join(search_dir, f) for f in files]

# Sort all files according to the `date` 
files.sort(key=lambda x: os.path.getmtime(x))

# Directory name to put your sorted files in
dir = "sorted"

# Create that directory
os.system("sudo mkdir -p " + dir)

# Extension of the file, mine are images
extension=".jpg"

# Starting name
i=1

# For every file copy it in sorted directory
for filename in files:
	destination = "sorted/" + str(i) + extension
	shutil.copy(filename,destination)
	i = i + 1
print "Copied all files to 'sorted' directory"
# End of Program 

{% endvimhl %}

# I wish I would've done this before as it would've helped me in my Previous Semesters. Hope it helps u as well.

### Till the next time 👻