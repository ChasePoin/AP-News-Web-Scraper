# AP News Web Scraper
This is a demonstration of SOLID principles using the web scraper that this is branched off of.
The scraper was reorganied into two modules and put into classes with superclasses and subclasses. These superclasses provide a model for the subclasses to be based off of.
### Information:
-This version of the project was meant to showcase the single responsibility principle. There is more information on how the two modules fulfill this principle inside of the module files themselves, near the top.

-Module 1 contains the new way of grabbing the URLs from the user inputted file. This and the scraper were redesigned to take a single URL at once instead of the entire file in order to fit a more modular approach.

-Module 2 contains the AP News scraper and inherits from a superclass that is meant to provide a framework if new scrapers are ever added. It also contains the getters and the writers. Each getter and each writer has a set purpose; the implementation of these getters and writers is meant to be flexible and allow for easy implementation of new getters/writers. The getters and writers being implemented as individal, single-responsibility classes allow for the scraper() to be easily changed to add more or less functionality based on what is needed, just by adding different objects of the writers/getters classes.

-The new modular format as well as the class structure makes the code much more simple and streamlined, allowing for easy implementation of new features and very, very easy testing.

-Data contains two different folders: raw and processed. Raw is the original version of the data format, with there being a title and the article body. Processed is the new version, with only the article body being present.

-The actual logic of this version of the project is very similar to how it was before; the biggest difference is how scrape() functions for the APscraper class. Before, it would take the file containing the URLs and loop through them; this was moved to run.py. Scrape() now is only responsible for a single URL at a time; it now relies on a different module for the URLs being properly taken from the file. 


### To use this version of the scraper:
-Follow the steps for initialization in the other branch of this repo. This will assure you have succesfully set up a way to run the program. This program uses the exact same environment.

-Now, download the zip of the branch by clicking the green <> code button.

-Navigate your current working directory to the folder you just downloaded/ where you put the files.

-Create a .txt file containing the AP News URLs you want to scrape the information from. Make sure this .txt file is in the same folder as run.py.

-The way to run the program has changed. It now uses an argparser. Repeating this because it is super important: to run the program, make sure your CWD is in the folder downloaded from this; all of the folder accesses are relative, so you need to be in the folder downloladed. Then type in the CMD/terminal "python run.py x" with x being the name of the file containing your URLs to be scraped.

-Check the data folders for the raw and processed files; the raw folder will contain the old format, with the title and article body. The processed folder will contain the files with just the article body.
