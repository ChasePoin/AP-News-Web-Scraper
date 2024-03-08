# AP News Web Scraper
This is a demonstration of SOLID principles using the web scraper that this is branched off of.
The scraper was reorganied into two modules and put into classes with superclasses and subclasses. These superclasses provide a model for the subclasses to be based off of.
### Information:
-This version of the project was meant to showcase two SOLID principles: the single-responsibility principle and the Liskov substitution principle. There is more information on how the two modules fulfill these principles inside of the module files themselves, near the top.
-Module 1 contains the getters and the writers that the scrapers use. Each getter and each writer has a set purpose; the implementation of these getters and writers is meant to be flexible and allow for easy implementation of new getters/writers.
-Module 2 contains the AP News scraper and inherits from a superclass that is meant to provide a framework if new scrapers are ever added. The getters and writers being implemented as individal, single-responsibility classes allow for the scraper() to be easily changed to add more or less functionality based on what is needed, just by adding different objects of the writers/getters classes.
-Data contains two different folders: raw and processed. Raw is the original version of the data format, with there being a title and the article body. Processed is the new version, with only the article body being present.


To use this version of the scraper:
-Follow the steps in the other branch of this repo. This will assure you have succesfully set up a way to run the program.
-Now, download the zip of the branch by clicking the green <> code button.
-Navigate your current working directory to the folder you just downloaded.
-Run run.py, and enter the name of the file containing your urls. There is one present already in the folder, you can either use that one or create a new one, just make sure it is in the same folder as run.py and that your current working directory is navigated to the new folder, as the file paths are relative to the CWD.
-Check the data folders for the raw and processed files.
