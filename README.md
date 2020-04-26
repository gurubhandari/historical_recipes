# historical_recipes
repository about a project on *historical_recipes*
add some items


# CWE-code-extraction
The extraction of vulnerable code, function names and function blocks from CWE Test Suites using 'srcML' could be useful to generate a dataset. Different test suites of open source programs  from NIST's  CWE Test Suites and Software Assurance Reference Dataset (SARD) are considered here for the possibility of dataset construction in different code level;
- class level (if a class has at least a vulnerable line in it) 
- function level (if a function has at least a vulnerable line in it)
- statement level (vulnerable lines)
- file level (at least a line in it)

Initially, we are focusing to extract function names as vulnerable or not. The vulnerable function names are the list of function names(//src:function/src:name) which have at least one vulnerable line in its function block.

## Requirements
- [srcML](https://www.srcml.org/)
- Python 3 or above

### Run
```
$ python3 Code/extractVulFunctions.py Data/manifest-107.csv
```
Note: As far as most of the researchers' dataset based on NIST SARD concerned, they have only considered specific files, for eg- in case of VLC_test suite(a java project), they have considered only '.java' files but there are other supportive files like '.xml', '.py' , '.sh' in the project that are vulnerable eg- (https://samate.nist.gov/SARD/view_testcase.php?tID=231386). It would be better to consider these supportive files as well. 
