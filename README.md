# ufo
Pet project: analysis of UFO observations in USA

## Files
* `ufo.ipynb` Jupyter notebook containing the complete analysis (it may be slightly outdated; __recent development is in separate parts__)
* `1_Data_collection.ipynb`, `2_Data_cleaning.ipynb`, `3_Exploratory_analysis` Jupyter notebooks with the analysis divided in sections (see below)
* `states.csv` data on the states of USA and Canada
* `ufo_raw_date.csv` data on UFO taken from the collections by the observation date
* `ufo_raw_shape.csv` data on UFO taken from the collections by the reported shape
* `ufo_for_analysis.csv` data used in the exploratory analysis section

This project provides the analysis of a dataset of cases of UFO observations, mainly in the USA and Canada. It consists of three fairly independent sections:

## Part 1. Data collection
The data have been taken from the [The National UFO Reportnig Center](http://www.nuforc.org/) wev page. 
This section of the products illustrates the collection of data from a set of HTML tables available online. The list of tables is taken dynamically from a separate table. The data are further compliled in a a Pandas dataframe and saved to csv for later use without downloading.
Moreover, certain data about the states and territories of USA and Canada (such as area and polupation) have been extracted from the corresponding [Wikipedia](https://en.wikipedia.org/wiki/Main_Page) pages in this section of the script.

## Part 2. Data cleaning
The collected data on UFO observations contain the information on the date and time of the UFO observation, place (state and city), duration of the phenomenon, and textual description of it.
The major steps of preliminary data cleaning has included the following steps:
* Verification of identity of two datasets collected independently (these arranged by data of observation and by UFO shape)
* Parsing of the date and time recorded as text in the proper format, filtering of incorrect values and too old (unreliable) cases
* Correction of the mistakes in the names of states
* Correction of the UFO shapes recorded by the observers to aid in further analysis
* Removing of the empty cases and duplicates

## Part 3. Exploratory data analysis
In this part, the following research questions have been covered:
* Which UFO shapes have been the most commonly reported?
* What are the trends in the number of reported cases by year? Are they differrent depending on the UFO shape?
* Are there special days of the week and/or times when the UFO reports are the most frequent?
* How are the cases of UFO observations distributed between the states? What are the possible reasons for the observed difference? Is there any special spatial correlation between the reported cases? (_Notice that this step containes several interactive plots which are not properly rendered by GitHub browser - run the notebook scripts to see them)
* Are there any significant differrences between the cases of UFO observations in the USA, Canada, and in the District of Columbia (a seemingly unusual state)?
Moreover, this part contains overall conclusions on the analysis and possible directions for future investigation.
