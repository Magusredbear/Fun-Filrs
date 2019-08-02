CREATE VIEW view_name AS
	SELECT column_name(s)
	FROM table_name
	WHERE condition
	
CREATE INDEX index_name
	ON table_name (column_name)	
SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index

==============================================================
			Login 
--------------------------------------------------------------

CREATE TABLE T_LOGIN 
   (Email VARCHAR(50)NOT NULL PRIMARY KEY, 
	Password VARCHAR(30)NOT NULL, 
	PIN NUMBER(4,0)NOT NULL, 
	Question_One VARCHAR(200)NOT NULL, 
	Question_Two VARCHAR(200)NOT NULL, 
	Question_Three VARCHAR(200)NOT NULL);


INSERT INTO
	INSERT INTO T_LOGIN
		(Email,Password,PIN NUMBER,Question_One,Question_Two,Question_Three)
	VALUES = ('','','','','','')	
	
SELECT  
	SELECT * FROM T_LOGIN
	WHERE EMAIL = ""
	

NOTES:
QUESTION ONE = What is your maternal grandmothers maiden name?
QUESTION TWO = Where were you when you first heard about 9/11?
QUESTION THREE = In what city or town was your first job?
	
==============================================================
			ALLERGIES
--------------------------------------------------------------

CREATE TABLE T_ALLERGIES 
   (Email VARCHAR(50)NOT NULL PRIMARY KEY,
    ALLERGIES VARCHAR(50)NOT NULL, 
	NOTES VARCHAR(250)NOT NULL);
	
INSERT INTO T_ALLERGIES 
	(Email,ALLERGIES,NOTES);
	VALUES = ('','','')
	
SELECT * FROM  T_ALLERGIES
	WHERE EMAIL = "" 
	
==============================================================
			DEMOGRAPHIC
--------------------------------------------------------------

CREATE TABLE T_DEMOGRAPHIC 
   (Email VARCHAR(50)NOT NULL PRIMARY KEY,
    LAST_NAME VARCHAR(20)NOT NULL, 
	FIRST_NAME VARCHAR(20)NOT NULL, 
	ADDRESS VARCHAR(55)NOT NULL, 
	CITY VARCHAR(25)NOT NULL, 
	STATE VARCHAR(2)NOT NULL, 
	ZIP NUMBER(5,0)NOT NULL);
	
DEMOGRAPHIC	
	INSERT INTO T_DEMOGRAPHIC 
		(Email,LAST_NAME,FIRST_NAME,ADDRESS,CITY,STATE ,ZIP);
	VALUES = ('','','','','','')	
	
SELECT * FROM T_DEMOGRAPHIC
	WHERE EMAIL = "" 
	
==============================================================
			DMLOGSBed
--------------------------------------------------------------	

CREATE TABLE T_DMLOGSBed 
   (Email VARCHAR(50)NOT NULL PRIMARY KEY,
    BEFORE_BED_DATE_TIME TIMESTAMP (6)NOT NULL, 
	BEFORE_BED_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	BEFORE_BED_BG NUMBER(3,0)NOT NULL); 

INSERT INTO T_DMLOGSBed
		(Email,BEFORE_BED_DATE_TIME ,BEFORE_BED_INSULIN_DOSE,BEFORE_BED_BG);
	VALUES = ('','','','')
	
SELECT * FROM  T_DMLOGSBed
	WHERE EMAIL = ""

==============================================================
			DMLOGSBreakfast
--------------------------------------------------------------	

CREATE TABLE T_DMLOGSBreakfast 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    BEFORE_BREAKFAST_DATE_TIME TIMESTAMP (6)NOT NULL, 
	BEFORE_BREAKFAST_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	BEFORE_BREAKFAST_BG NUMBER(3,0)NOT NULL, 
	AFTER_BREAKFAST_DATE_TIME TIMESTAMP (6)NOT NULL, 
	AFTER_BREAKFAST_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	AFTER_BREAKFAST_BG NUMBER(3,0)NOT NULL);
	
INSERT INTO T_DMLOGSBreakfast
    (EMAIL,BEFORE_BREAKFAST_DATE_TIME,BEFORE_BREAKFAST_INSULIN_DOSE,
     BEFORE_BREAKFAST_BG NUMBER,AFTER_BREAKFAST_DATE_TIME , 
	 AFTER_BREAKFAST_INSULIN_DOSE,AFTER_BREAKFAST_BG );
	VALUES = ('','','','','','','')
	
SELECT * FROM	T_DMLOGSBreakfast
	WHERE EMAIL = ""
	
==============================================================
			DMLOGSDinner
--------------------------------------------------------------

CREATE TABLE T_DMLOGSDinner
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    BEFORE_DINNER_DATE_TIME TIMESTAMP (6)NOT NULL, 
	BEFORE_DINNER_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	BEFORE_DINNER_BG NUMBER(3,0)NOT NULL, 
	AFTER_DINNER_DATE_TIME TIMESTAMP(6)NOT NULL, 
	AFTER_DINNER_INSULIN_DOSE NUMBER(2,3)NOT NULL);
	
INSERT INTO T_DMLOGSDinner
   (EMAIL ,BEFORE_DINNER_DATE_TIME,BEFORE_DINNER_INSULIN_DOSE, 
	BEFORE_DINNER_BG NUMBER,AFTER_DINNER_DATE_TIME,AFTER_DINNER_INSULIN_DOSE );
	VALUES = ('','','','','','','')
	
SELECT * FROM T_DMLOGSDinner
	WHERE EMAIL = ""
	
==============================================================
			DMLOGSLunch
--------------------------------------------------------------

CREATE TABLE T_DMLOGSLunch 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    BEFORE_LUNCH_DATE_TIME TIMESTAMP(6)NOT NULL, 
	BEFORE_LUNCH_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	BEFORE_LUNCH_BG NUMBER(3,0)NOT NULL, 
	AFTER_LUNCH_DATE_TIME TIMESTAMP (6)NOT NULL, 
	AFTER_LUNCH_INSULIN_DOSE NUMBER(2,3)NOT NULL, 
	AFTER_LUNCH_BG NUMBER(3,0)NOT NULL);

INSERT INTO T_DMLOGSLunch 
   (EMAIL ,BEFORE_LUNCH_DATE_TIME,BEFORE_LUNCH_INSULIN_DOSE , 
	BEFORE_LUNCH_BG,AFTER_LUNCH_DATE_TIME,AFTER_LUNCH_INSULIN_DOSE,AFTER_LUNCH_BG);
	VALUES = ('','','','','','','')
	
SELECT * FROM T_DMLOGSLunch
	WHERE EMAIL = ""
	
==============================================================
			DOCTOR
--------------------------------------------------------------

CREATE TABLE T_DOCTOR 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    LAST_NAME VARCHAR(20)NOT NULL, 
	FIRST_NAME VARCHAR(20)NOT NULL, 
	ADDRESS VARCHAR(55)NOT NULL, 
	ADDRESS2 VARCHAR(55), 
	CITY VARCHAR(25)NOT NULL, 
	STATE VARCHAR(2)NOT NULL, 
	ZIP NUMBER(5,0)NOT NULL, 
	PHONE NUMBER(10,0)NOT NULL, 
	PHONE2 NUMBER(10,0));

INSERT INTO T_DOCTOR
   (EMAIL,LAST_NAME,FIRST_NAME,ADDRESS,ADDRESS2,CITY,STATE,ZIP , 
	PHONE NUMBER,PHONE2);
	VALUES = ('','','','','','','','','','')

SELECT * FROM 	T_DOCTOR 
	WHERE EMAIL = ""  
	
==============================================================
			MAJOR_ILLNESSES_SURGERIES
--------------------------------------------------------------

CREATE TABLE T_MAJOR_ILLNESSES_SURGERIES 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    DOS DATE NOT NULL, 
	ILLNESSES_SURGERIES VARCHAR(50)NOT NULL, 
	MAJOR_MINOR_CHRONIC VARCHAR(15)NOT NULL);
	
INSERT INTO T_MAJOR_ILLNESSES_SURGERIES 
   (EMAIL,DOS,ILLNESSES_SURGERIES,MAJOR_MINOR_CHRONIC );
	VALUES = ('','','','')
	
SELECT * FROM  T_MAJOR_ILLNESSES_SURGERIES 
	WHERE EMAIL = "" 
	
==============================================================
			PRESCRIPTION
--------------------------------------------------------------

CREATE TABLE T_PRESCRIPTION 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,	
    NAME VARCHAR(20)NOT NULL, 
	DOSES VARCHAR(20)NOT NULL, 
	REFILLS_LEFT NUMBER(10,0)NOT NULL, 
	EXP DATE NOT NULL);
	
INSERT INTO T_PRESCRIPTION 
   (EMAIL,NAME,DOSES,REFILLS_LEFT,EXP);
	VALUES = ('','','','','')
	
SELECT * FROM  T_PRESCRIPTION  
	WHERE EMAIL = ""
	
==============================================================
			TEST_SCREENINGS
-------------------------------------------------------------- 

CREATE TABLE T_TEST_SCREENINGS 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    DOTS DATE NOT NULL, 
	TEST_SCREENINGS VARCHAR(50)NOT NULL);
	
INSERT INTO T_TEST_SCREENINGS
   (EMAIL,DOTS,TEST_SCREENINGS);
	VALUES = ('','','')

SELECT * FROM T_TEST_SCREENINGS 
	WHERE EMAIL = "" 
	
==============================================================
			Diseases
--------------------------------------------------------------

CREATE TABLE T_Diseases 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,	
    NAME VARCHAR(20)NOT NULL, 
	Date Diagnosis VARCHAR(20)NOT NULL, 
	AcutChor VARCHAR(15)NOT NULL,);

INSERT INTO T_Diseases 
   (EMAIL,NAME,Date Diagnosis,AcutChor);
	VALUES = ('','','','')

SELECT * FROM T_Diseases
	WHERE EMAIL = "" 
	
==============================================================
			History
--------------------------------------------------------------

CREATE TABLE T_History 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,	
    Illness_NAME VARCHAR(20)NOT NULL, 
	Family_Member VARCHAR(20)NOT NULL);
	
INSERT INTO T_History
   (EMAIL,Illness_NAME,Family_Member);   
	VALUES = ('','','')

SELECT * FROM  T_History
	WHERE EMAIL = ""
==============================================================
			ILLNESSES_SURGERIES
--------------------------------------------------------------

CREATE TABLE T_ILLNESSES_SURGERIES 
   (EMAIL VARCHAR(50)NOT NULL PRIMARY KEY,
    DOS DATE NOT NULL, 
	ILLNESSES_SURGERIES VARCHAR(50)NOT NULL);
	
INSERT INTO T_ILLNESSES_SURGERIES 
   (EMAIL,DOS,ILLNESSES_SURGERIES);
   VALUES = ('','','') 
   
SELECT * FROM  T_ILLNESSES_SURGERIES
	WHERE EMAIL = "" 
	
==============================================================
			
--------------------------------------------------------------
