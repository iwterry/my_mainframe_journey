CBLDB2P1 is a COBOL program that reads rows from the database table S123.CLAIM_T5 and writes all the rows to a new file.

CBLDB2P2 is a COBOL program that reads rows from the database table S123.CLAIM_T5 and updates a table column for each row in the table.

CBLDB2J1 is the JCL for CBLDB2P1.

CBLDB2J2 is the JCL for CBLDB2P2.

CLAIMTAB contains the SQL code to create the S123.CLAIM_T5 database table.

The DCLGEN tool created DCLGEN01, which maps the database columns to COBOL variables for the S123.CLAIM_T5 database table.

The screenshots represent the work I did for the 8th, 9th, and 10th lectures from https://www.udemy.com/course/mainframe-db2-developer-training-by-anil-polsani/.