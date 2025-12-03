# ADS Experiment 4  
  
Implement & Demonstrate Object Oriented Database.  
1) Create a Rectangle Object with operations Area & Perimeter.  
  
TYPE -> TYPE BODY -> OBJECT TABLE -> Insert Objects -> Query  
  
```
CREATE OR REPLACE TYPE Rectangle AS OBJECT (
    length NUMBER,
    width NUMBER,
    
    MEMBER FUNCTION Area RETURN NUMBER,
    MEMBER FUNCTION Perimeter RETURN NUMBER
);
/

```
  
CREATE OR REPLACE TYPE BODY Rectangle AS   
      
    MEMBER FUNCTION Area RETURN NUMBER IS  
    BEGIN  
        RETURN length * width;  
    END;  
  
    MEMBER FUNCTION Perimeter RETURN NUMBER IS  
    BEGIN  
        RETURN 2 * (length + width);  
    END;  
END;  
/  
  
  
```
CREATE TABLE Rectangle_Table OF Rectangle;

```
  
```
INSERT INTO RECTANGLE_TABLE VALUES(RECTANGLE(10,5));
INSERT INTO RECTANGLE_TABLE VALUES(RECTANGLE(20,2));

```
  
```
SELECT
    r.length,
    r.width,
    r.Area() AS Area,
    r.Perimeter() AS Perimeter
FROM RECTANGLE_TABLE r;

```
