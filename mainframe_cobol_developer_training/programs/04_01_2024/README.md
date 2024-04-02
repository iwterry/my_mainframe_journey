There are three input PS data files:
	- CBLPRAC.FILE1
		- consists of fake data for a person's id number and person's name
		- is sorted in ascending order by a person's id number
	- CBLPRAC.FILE2
		- consists of fake data for a city's id number, city's name, the state the city is in, and the person's id number that lives in that city
		- is sorted in ascending order by a person's id number 
	- CBLPRAC.FILE3
		- consists of same data as CBLPRAC.FILE2, but the data is sorted in ascending order by the city's id number

The three data files were generated using the COBOL program CBLPRAC1 and the JCL file JCLPRAC1. 

NOTE: For the input data files, there is not a situation where a city is lived in by multiple people, but a person can live in multiple cities.

In this ficticious example, the scenario is to use COBOL to create files that combines the information in these files using different approaches in order to create new PS data files.

## Approach 1
With both CBLPRAC.FILE1 and CBLPRAC.FILE2 sharing a common field (a person's id number) and both being sorted in ascending order by a person's id number, matching logic will be used to combine the information of both files to create a new PS data file CBLPRAC.FILE4.

The COBOL program CBLPRAC2 uses this approach, and the JCL program JCLPRAC2 is used to compile and run CBLPRAC2.


## Approach 2
While both CBLPRAC.FILE1 and CBLPRAC.FILE3 share a common field (a person's id number), they are both not sorted using that common field. Therefore, matching logic cannot be used; instead, the approach is to use lookup logic to combine the information of both files to create a new PS data file CBLPRAC.FILE5.

The COBOL program CBLPRAC3 uses this approach, and the JCL program JCLPRAC3 is used to compile and run CBLPRAC3.


## Approach 3
Use lookup logic that combines the information from CBLPRAC.FILE1 and CBLPRAC.FILE3; however, instead of having the information of CBLPRAC.FILE1 be stored in a PS data file, it will be in a copybook. Lookup logic will then be used to combine the data in CBLPRAC.FILE3 and the copybook to create a new PS data file CBLPRAC.FILE6.

The COBOL program CBLPRAC4 uses this approach, and the JCL program JCLPRAC4 is used to compile and run CBLPRAC4.


## What is the goal of all this?
The goal of all this is to practice matching and lookup logic with COBOL based on what I learned in the [first Udemy course](https://www.udemy.com/course/cobol-by-anilpolsani/).


## Where are the files located?
The COBOL files are located in the cobol directory.
The copybooks are located in the copybooks directory, and the copybooks directory is inside the cobol directory.
The JCL files are located in the jcl directory.
The PS data files are located in the data-files-created directory.
All files are stored as text files with the "txt" extension.