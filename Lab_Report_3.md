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
The -c option enables us to find the number of lines that match the query.\


Example 1:
```
# Example 1 of grep -c
grep -c "Amsterdam" written_2.txt
```


**`grep -n`**\
The -n option also displays the line number at which the given query was matched along with the whole line.\


**`grep -i`**\
The -i option searches for the given string without keeping the specific case of the alphabets. It basically searches for the string case insensitively.\


**`grep "^query"`**\
The ^query option helps us to match the lines that start with the specified query.\
