# PL-SQL-Procedure-ETL-Aggregate-Transformations
a PL/SQL Procedure that works on two tables, a source and a target. 

The Source Table Contains Four Columns: Table name, Column name, type of aggregation, and the frequency of the aggregation.

<img width="308" alt="333" src="https://user-images.githubusercontent.com/108706173/221380638-dbb99846-9896-460d-b14e-5a07c96c97ba.png">

The main task of the ETL Process is to preform the selected aggregate transformation on that column and load the result of it with the rest of the the column info and the date of the job according to the frequency.

The Calculation of the date is kind of Tricky !

- If it is the first run of the procedure and the frequency is Monthly then the date would be sysdate + 1 day
- If it is the first run of the procedure and the frequency is Daily then the date would be sysdate + 1 month
- If it is NOT the first run of the procedure and the frequency is Monthly then the date would be last date in the target table + 1 month
- If it is the first run of the procedure and the frequency is Monthly then the date would be last date in the target table + 1 day


Here is an Example after Excueting the Procedure 4 Times!

<img width="396" alt="4444" src="https://user-images.githubusercontent.com/108706173/221380639-5f637684-d987-49ff-9f4a-191c8b91aca3.png">


