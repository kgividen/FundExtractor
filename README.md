FundExtractor
=============

Populate an SQL database with fund information

To run the extractor:

(1) Modify the parameters found in extractor.properties as necessary
(2) Mase sure the DB is set as in db/funds.sql and priceStructure.sql
(3) Run the program with:

       java -jar yahoo.jar

NOTES:

- The program was developed using Intellij IDEA, you can open the project with IDEA using file SiteExtractor2.ipr
- In order to download data for different dates, just change yahoo-start-date and yahoo-end-date.

How the program works:

The program does 2 things. It first downloads the csv data in a local folder. It creates one file per symbol found
in the database. Then it stores that data into the database and then proceeds with the calculation of values.

You can modify extractor.properties so that you can either just download the csv data in a local folder only or you
can store previously downloaded data in DB or do both sequentially. You can manage this with the variables:
yahoo-download-csv and yahoo-update-db