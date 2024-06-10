# checkurl

To run this tool, you need to have:
1. A recent Java Virtual Machine (11 or higher)
2. A recent version of Maven (3 or higher)
3. A SerpApi key (please include it in the key.properties file)

The results obtained in the paper can be reproduced as follows. Go to the project directory (where the pom.xml file appears) and do the following:

```mvn package
  cd target
  chmod 751 ./runEntireFlow.sh
  ./runEntireFlow.sh DBLP-EMSE-2003.xml #Or any other DBLP XML file

Once the processing is finished, the extracted URLs, their accessibility and the category under which they have been classified will appear in the pdf_database.db (SQLite) database. The different steps of the process are documented in text files within the same execution directory.

We recommend backing up the database before processing another DBLP XML file, as the database does not contain references to the journal/conference volume/edition.
