CBLDB2P3 is a COBOL program that reads rows from the database table S124.CLAIM_T5 and then calls the COBOL subprogram CBLDB2P4 to validate each row. Based on the return value from CBLDB2P4, CBLDB2P3 updates the table column CLAIM_STATUS.

CBLDB2P4 is a COBOL program that searches for a row from the database table S124.POLICY_T5 by filtering based on the value CBLDB2P3 provides. CBLD2P4 uses the data from the row and the data given to it by CBLDB2P3 to decide what value to return to CBLDB2P3.

CBLDB2J4 contains the JCL code for CBLDB2P3.

CBLDB2J3 contains the JCL code for CBLDB2P4.

CLAM2TAB contains the SQL code to create the S124.CLAIM_T5 dabase table.

POLCYTAB contains the SQL code to create the S124.POLICY_T5 database table.

The DCLGEN tool created DCLGEN02, which maps the database columns to COBOL variables for the S124.CLAIM_T5 database table.

The DCLGEN tool created DCLGEN03, which maps the database columns to COBOL variables for the S124.POLICY_T5 database table.

Note that I could have used null indicator variables in the COBOL programs, but since I knew that no column would have null values, I chose not to use null indicator variables for these programs.

The screenshots represent the work I did for the 11th lecture from https://www.udemy.com/course/mainframe-db2-developer-training-by-anil-polsani/.