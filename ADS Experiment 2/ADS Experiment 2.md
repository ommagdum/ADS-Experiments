# ADS Experiment 2  
  
1. Print sum of N numbers   
```
DECLARE
N NUMBER := 10;
TOTAL NUMBER := 0;
BEGIN
    FOR I IN 1..N LOOP
    TOTAL := TOTAL + I;
END LOOP;
DBMS_OUTPUT.PUT_LINE(TOTAL);
END;

```
  
2. Find the Factorial of a given number.  
  
DECLARE  
N NUMBER := 4;  
FACTORIAL NUMBER := 1;  
BEGIN  
    FOR I IN 1..N LOOP  
    FACTORIAL := FACTORIAL * I;  
END LOOP;  
DBMS_OUTPUT.PUT_LINE(FACTORIAL);  
END;  
  
  
3. Check whether input number is prime or not  
  
```
DECLARE
    NUM NUMBER := 7;
    IS_PRIME BOOLEAN := TRUE;
BEGIN
    IF NUM <= 1 THEN
        IS_PRIME := FALSE;
    ELSE
        FOR I IN 2..TRUNC(SQRT(NUM)) LOOP
            IF MOD(NUM, I) = 0 THEN
                IS_PRIME := FALSE;
                EXIT;
            END IF;
        END LOOP;
    END IF;

    IF IS_PRIME THEN
        DBMS_OUTPUT.PUT_LINE(NUM || ' IS PRIME');
    ELSE
        DBMS_OUTPUT.PUT_LINE(NUM || ' IS NOT A PRIME');
    END IF;
END;




```
