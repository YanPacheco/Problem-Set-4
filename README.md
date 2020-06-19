# Problem-Set-4
# (1)

Source of Data: http://2016.padjo.org/tutorials/sqlite-data-starterpacks/#toc-florida-death-row-roster

Column header | Description
--------------|------------
Inmate Name | Name
DC# | Case Number
Race/Gender | WM or BM for white male/black male
Date Received | Date inmate entered system
Crime | Crime commited
Date of Offense | Crime Date
Date of Sentence  | Date sented
Date of Birth | Date of Birth
County  | Florida county 

# 2
# Data could be normalized by Inmate county and also by Race/Gender. These would both be TEXT data types.

# 3
Create TABLE inmates_slim (
  Inmate Name TEXT NOT NULL,
  RACE_GENDER TEXT NOT NULL,
  County TEXT NOT NULL);
# 4

INSERT INTO inmates_slim(Inmate Name, Race_Gender, County)
SELECT 'Inmate Name', 'Race/Gender', County FROM inmates;
