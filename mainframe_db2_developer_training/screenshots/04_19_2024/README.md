These screenshots contain the programs and other work that I did while working through the 6th lecture from https://www.udemy.com/course/mainframe-db2-developer-training-by-anil-polsani/.

The COBOL program CBLDB2P2 accepts input from a file that is created from the JCL program JCLPGM01. CBLDB2P2 performs some validation on each record in the file. If the record is valid, it is inserted into the database. Otherwise, the record is wrote to an error file.

CBLDB2P2 uses copybooks COPYBK01 and COPYBK02 and calls the COBOL subprogram CBLSUBP1.

The SQL screenshot shows the SQL used to create the database table.

The JCL program JCLSUBP1 compiles CBLSUBP1. The JCL program CBLDB2J2 is used for CBLDB2P2.