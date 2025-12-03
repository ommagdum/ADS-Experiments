# ADS Experiment 3  
  
Implement the following PL/SQL Programs using switch case statements.  
1) Find the area of the Circle. 2) Find the area of Triangle. 3) Find the area of Rectangle.  
  
```
DECLARE
    CHOICE NUMBER := &CHOICE;
    RADIUS NUMBER;
    BASE NUMBER;
    HEIGHT NUMBER;
    LENGTH NUMBER;
    WIDTH NUMBER;
    AREA NUMBER;
BEGIN
    CASE CHOICE
        WHEN 1 THEN
            RADIUS := &RADIUS;
            AREA := 3.14 * RADIUS * RADIUS;
            DBMS_OUTPUT.PUT_LINE('Area Of Circle: ' || AREA);

        WHEN 2 THEN
            BASE := &BASE;
            HEIGHT := &HEIGHT;
            AREA := 0.5 * BASE * HEIGHT;
            DBMS_OUTPUT.PUT_LINE('Area Of TRIANGLE: ' || AREA);

        WHEN 3 THEN
            LENGTH := &LENGTH;
            WIDTH := &WIDTH;
            AREA := LENGTH * WIDTH;
            DBMS_OUTPUT.PUT_LINE('Area Of RECTANGLE: ' || AREA);
        
        ELSE
            DBMS_OUTPUT.PUT_LINE('INVALID INPUT');
    END CASE;
END;
/
        


```
