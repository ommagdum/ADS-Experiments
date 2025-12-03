# ADS EXPERIMENT 10  
  
**Implement a trigger** trg_assign_grade that automatically assigns a grade before inserting a  
new student record according to the following criteria:  
 Marks ≥ 75 → Grade **'A'**  
 Marks ≥ 50 and < 75 → Grade **'B'**  
 Marks < 50 → Grade **'C'**  
  
  
CREATE TABLE Student (  
    SID     NUMBER,  
    Sname   VARCHAR2(50),  
    Marks   NUMBER,  
    Grade   CHAR(1)  
);  
  
CREATE OR REPLACE TRIGGER trg_assign_grade  
BEFORE INSERT ON Student  
FOR EACH ROW  
BEGIN  
    IF :NEW.Marks >= 75 THEN  
        :NEW.Grade := 'A';  
    ELSIF :NEW.Marks >= 50 THEN  
        :NEW.Grade := 'B';  
    ELSE  
        :NEW.Grade := 'C';  
    END IF;  
END;  
/  
  
INSERT INTO Student (SID, Sname, Marks) VALUES (1, 'Amit', 82);  
INSERT INTO Student (SID, Sname, Marks) VALUES (2, 'Riya', 63);  
INSERT INTO Student (SID, Sname, Marks) VALUES (3, 'Karan', 45);  
  
SELECT * FROM Student;  
