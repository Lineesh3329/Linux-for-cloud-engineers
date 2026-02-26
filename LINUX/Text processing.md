Text Processing
---------------
Text Processing is very important in Linux — especially for logs and troubleshooting.

Text processing commands are used to search, filter, modify, and analyze text data in files. 

These commands are commonly used to read logs, extract specific information, and automate tasks in servers.

They are very useful in cloud and production environments.

## GREP 
  This command used to Search for a particular file or a data.

    grep "word" file.txt        - Search for a word
    grep -i "word" file.txt     - Case insensitive search
    grep -v "word" hello.txt    - Expect "word" show other data
    grep -r "timeout" ~/logs    - Search "timeout" in all folders & files in logs
    grep info *.txt             - if we have same data in 2 files, this cmd search both & shows
    grep info *.txt|tail-f      - shows matching 10 datum from both the files
    grep "^\[Error\]" log1.txt  - Search "Error" in log1 file

## Find
This command used to search files or folders in linux.
    
    find. -name"hello.txt"        - Search for hello.txt
    find. -name"*.txt"            - Find all files with .txt extension
    find. -typed -name"data"      - search directory
    find. -typef -size +10m       - find file>10MB size
    find. -mtime -1               - find files modified in last 1 day
    find. -name "*.txt" -delete   - Delete all .txt file

## wc, sort
  This command used for counting words and sorting file.
    
    wc file.txt                 - Count lines, words, characters
    wc -l file.txt              - Count lines only
    wc -c file .txt             - Count characters
    wc -w file .txt             - Count words
    sort file.txt               - Sort lines
    sort -r file.txt            - Reverse order
    sort -n file.txt            - Sort numbered order in a file
    uniq file.txt               - Remove duplicate lines

#### Difference between Grep & Find:
    grep - search Files/Folders        --> Where is the file ?
    find - serach texts inside a file  --> What is inside the file ?

## AWK
This command used to print specific columns from a file or command output

    awk '{print $1}'data.txt          - Print first column
    awk '{print $1,$3}'data.txt       - Print first & third column
    awk '$2>27{print $1,$3}'data.txt  - Print first & third column if only second column value>27


    &0           - whole line\
    &3>10        - Condition filter
    NR           - Line count
    awk'/text/'  - Search like grep

Text processing commands help in analyzing logs and extracting useful information from files. They are powerful tools for troubleshooting and automation in Linux systems.

    
