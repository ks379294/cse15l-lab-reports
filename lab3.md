# Part 1
1. A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
2. An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
3. The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
4. The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)

# Part 2
1. Consider the commands `less`, `find`, and `grep`. Choose one of them: For this exercise, I'm choosing the find command.
2. Online, find 4 interesting command-line options or alternate ways to use the command you chose: `-type`, `-mtime`, `-name`, `-iname`

## Command 1
The command used here is `find` and `-type`
Give 2 examples of using it on files and directories from `./technical`:
Example 1: Using `-type` for a socket in the directory, code block that shows the command and its output:

```
(base) administrator@Administrators-MacBook-Pro docsearch % find technical -type s
(base) administrator@Administrators-MacBook-Pro docsearch %
```

Write a sentence or two about what it’s doing and why it’s useful: This is telling me that tere are no socket files in `./technical` directory. That is why there is no printed output, because no socket files have been found. This is useful because it can tell me immediately there are no socket files without me having to do a manual search.

Example 2: Using `-type` to get directories in the directory, code block that shows the command and its output:
```
(base) administrator@Administrators-MacBook-Pro docsearch % find technical -type d
technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
```
Write a sentence or two about what it’s doing and why it’s useful: This output is all the directories in the `./technical` directory. This is useful, because if I wanted to find a certain subdirectory in the this directory, I could just look at this list instead of looking through thousands of files.

## Command 2
The command used here is `find` and `-mtime`
Example 1: Using `-mtime` to get items modified in the last six days, code block that shows the command and its output:

```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical/911report/ -mtime -6
../technical/911report/
../technical/911report//chapter-13.4.txt
../technical/911report//chapter-13.5.txt
../technical/911report//chapter-13.1.txt
../technical/911report//chapter-13.2.txt
../technical/911report//chapter-13.3.txt
../technical/911report//chapter-3.txt
../technical/911report//chapter-2.txt
../technical/911report//chapter-1.txt
../technical/911report//chapter-5.txt
../technical/911report//chapter-6.txt
../technical/911report//chapter-7.txt
../technical/911report//chapter-9.txt
../technical/911report//chapter-8.txt
../technical/911report//preface.txt
../technical/911report//chapter-12.txt
../technical/911report//chapter-10.txt
../technical/911report//chapter-11.txt
```
Write a sentence or two about what it’s doing and why it’s useful:

Example 2: Example 1: Using `-mtime` to get items modified 5 or more days ago, code block that shows the command and its output:
 
```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical/911report/ -mtime +5
../technical/911report/
../technical/911report//chapter-13.4.txt
../technical/911report//chapter-13.5.txt
../technical/911report//chapter-13.1.txt
../technical/911report//chapter-13.2.txt
../technical/911report//chapter-13.3.txt
../technical/911report//chapter-3.txt
../technical/911report//chapter-2.txt
../technical/911report//chapter-1.txt
../technical/911report//chapter-5.txt
../technical/911report//chapter-6.txt
../technical/911report//chapter-7.txt
../technical/911report//chapter-9.txt
../technical/911report//chapter-8.txt
../technical/911report//preface.txt
../technical/911report//chapter-12.txt
../technical/911report//chapter-10.txt
../technical/911report//chapter-11.txt
(base) administrator@Administrators-MacBook-Pro technical % 
```
Write a sentence or two about what it’s doing and why it’s useful:

## Command 3

Example 1: Using `-name` to find a file by name, code block that shows the command and its output:
```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical -name "commission_report.txt" 
../technical/government/About_LSC/commission_report.txt
```
Write a sentence or two about what it’s doing and why it’s useful:


Example 2: Using `-name` to find a different by name, code block that shows the command and its output:
```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical/ -name "chapter-1.txt"           
../technical//911report/chapter-1.txt
```
Write a sentence or two about what it’s doing and why it’s useful:

## Command 4

Example 1:
```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical/government -iname "*report*txt" 2>/dev/null 
../technical/government/About_LSC/Progress_report.txt
../technical/government/About_LSC/Strategic_report.txt
../technical/government/About_LSC/Special_report_to_congress.txt
../technical/government/About_LSC/commission_report.txt
../technical/government/About_LSC/reporting_system.txt
../technical/government/About_LSC/State_Planning_Report.txt
../technical/government/About_LSC/State_Planning_Special_Report.txt
../technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
```

Example 2:

```
(base) administrator@Administrators-MacBook-Pro technical % find ../technical -iname "tech*txt" 2>/dev/null 
../technical/government/Env_Prot_Agen/tech_sectiong.txt
../technical/government/Env_Prot_Agen/tech_adden.txt
```



