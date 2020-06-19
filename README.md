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
# Data could be normalized by Inmate county and also by Race/Gender. These would both be TEXT data types. It would be worth normalizing the data in this manner because you can then see which county has the most inmates and additionally look at which Race/Gender has the most offenses. You can also choose to parse over the date information and run an analysis on which county had the most incidents of crimes per year.

# 3
Create TABLE inmates_slim (
  Inmate Name TEXT NOT NULL,
  RACE_GENDER TEXT NOT NULL,
  County TEXT NOT NULL);
# 4

INSERT INTO inmates_slim(Inmate Name, Race_Gender, County)
SELECT 'Inmate Name', 'Race/Gender', County FROM inmates;
