# ADS EXPERIMENT 7  
  
  
Demonstrate the concept of sequences. Create sequence to generate EmloyeeID’s for the table  
Employee(EmloyeeID,Ename,Salary,City). Demonstrate Insert, Select , Delete Operations.  
  
```
CREATE TABLE EMPLOYEE(
    EMP_ID NUMBER PRIMARY KEY,
    NAME VARCHAR(50),
    SALARY NUMBER
);

```
  
```
CREATE SEQUENCE emp_id_seq
START WITH 1
INCREMENT BY 1
NOCACHE;

```
  
```
INSERT INTO EMPLOYEE VALUES(EMP_ID_SEQ.nextval, 'OM MAGDUM', 50000);

```
  
```
SELECT * FROM EMPLOYEE

```
  
```
DELETE FROM EMPLOYEE WHERE EMP_ID = 2;

```
