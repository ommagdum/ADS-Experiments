# ADS EXPERIMENT 6  
  
Implement a PL/SQL Procedure(Inside a PL/SQL block)  
****1) ****Find the square of a number using the “IN OUT” Parameter.  
****2) ****Find the Maximum of three numbers use IN,IN & INOUT for the three parameters respectively. Use  
the third parameter to hold the result.  
  
1.  
	  
  
```
CREATE OR REPLACE PROCEDURE SQUARE_NUM(P_NUM IN OUT NUMBER)
IS
BEGIN
    P_NUM := P_NUM*P_NUM;
END;
/

```
  
  
```
DECLARE
    V NUMBER := 7;
BEGIN
    SQUARE_NUM(V);
    DBMS_OUTPUT.PUT_LINE('SQUARE = '||V);
END;

```
  
  
2.   
  
```
CREATE OR REPLACE PROCEDURE max_of_three(
    P_A IN NUMBER,
    P_B IN NUMBER,
    P_C IN OUT NUMBER
)
IS
BEGIN
    IF P_A >= P_B AND P_A >= P_C THEN
        P_C := P_A;
    ELSIF P_B >= P_A AND P_B >= P_C THEN
        P_C := P_B;
    ELSE
        NULL;
    END IF;
END;

```
  
```
DECLARE 
    A NUMBER := 50;
    B NUMBER := 75;
    RESULT NUMBER := 8;
BEGIN
    MAX_OF_THREE(A, B, RESULT);
    DBMS_OUTPUT.PUT_LINE('MAXIMUM OF THREE = ' || RESULT);
END;

```
