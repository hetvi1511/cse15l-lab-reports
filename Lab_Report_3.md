# Researching Commands
Commands like `less`, `find` and `grep` help in accessing the files more efficiently. They all have their seperate functions respectively. The command
that I have chosen is `grep`. `grep` is a command line tool to search for regular expressions and it will print the matching expressions to the output.
Few command options that can be used along with `grep` that can help in searching for patterns and displaying files containing those patterns easier, are
as follows:
- `grep -c "query" filename`
- `grep -n "query" filename`
- `grep -i "query" filename`
- `grep "^query" filename`



**`grep -c`**\
The -c option enables us to find the number of lines that match the query.


Example 1:\
*Command-line statement*
```
# Example 1 of grep -c
grep -c "Amsterdam" travel_guides/berlitz2/Amsterdam-WhereToGo.txt
```
*Output*\
![Amsterdam](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-c%20amsterdam.png)

Example 2:\
*Command-line statement*
```
# Example 2 of grep -c
grep -c "this" */*/*/*
```
*Output*\
![this](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-c%20this.png)


**`grep -n`**\
The -n option also displays the line number at which the given query was matched along with the whole line.


Example 1:\
*Command-line statement*
```
# Example 1 of grep -n
grep -n "this" non-fiction/OUP/Castro/chC.txt
```
*Output*\
![this](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-n%20this.png)

Example 2:\
*Command-line statement*
```
# Example 2 of grep -n
grep -n "hetvi" *
```
*Output*\
![hetvi](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-n%20hetvi.png)
When no match is found it returns 0 for all files in the specified path.



**`grep -i`**\
The -i option searches for the given string without keeping the specific case of the alphabets. It basically searches for the string case insensitively.\
Example 1:\
*Command-line statement*
```
# Example 1 of grep -i
grep -i "ThIs" travel_guides/berlitz2/Cuba-WhatToDo.txt
```
*Output*\
![this](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-i%20this.png)

Example 2:\
*Command-line statement*
```
# Example 2 of grep -i
grep -i "PUERTO" travel_guides/berlitz2/Vallarta-History.txt
```
*Output*\
![puerto](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/-i%20puerto.png)

**`grep "^query"`**\
The ^query option helps us to match the lines that start with the specified query.\
Example 1:\
*Command-line statement*
```
# Example 1 of grep "^query"
grep "^The" travel_guides/berlitz2/Vallarta-History.txt
```
*Output*\
![the](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/%5E%20the.png)

Example 2:\
*Command-line statement*
```
# Example 2 of grep "^query"
grep "^Gandhi" non-fiction/OUP/Rybczynski/ch3.txt
```
*Output*\
![gandhi](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/%5E%20gandhi.png)
When no line starts with the speicfied query, it displays nothing.


I did all my research on grep command-lne options from [GeeksForGeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
