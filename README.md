# ADS-command-line
An interactive command line tool designed for [Astrophysics Data System](http://www.adsabs.harvard.edu) for macOS.
![img](http://adsabs.github.io/img/bbb_assets/ads_logo_full_light_background.svg)
## Installation
```
python ads.py
pyInstaller -F ads.py
cp dist/ads /bin/
```
when the installation is done, launch it with
`
ads
`
or use
`
ads NAMEOFTHEAUTHOR(S) (YYYY)
`
for a quick search.

## System requirement
Python2 (and packages including re, urlib2, multiprocessing and pyperclip), [iTerm2](http://www.iterm2.com) (Best operating environment to enable terminal-based url request)

## Search modes
The software allows three modes of searching.
1. Citation based (default)
![img](https://github.com/LiYunyang/ADS-command-line/blob/master/example/cmod.png)
   type the citation, e.g., Li, et al., (2017); Li & Bregman 2017, etc.
   arXiv ID based search is also supported in this mode.
2. Author-year based
    ![img](https://github.com/LiYunyang/ADS-command-line/blob/master/example/amod.png)
   type `a(uthor)` to enter this search mode. 
   Use the conventional `^` before the first author, the form of the author goes as Last; Last, First; or Last, F. The search is case insensitive.
   
   The year is **required**, which can be a single year like `2017` or two years concatenated by '-' for a search within the range.
3. Journal based
![img](https://github.com/LiYunyang/ADS-command-line/blob/master/example/jmode.png)
   type `j(ournal)` to enter this search mode.
   Type the abbreviations of the journal, year, volume and pages as indicated. Either of the term can be omitted.

add `!` anywhere in the name will force an exact name-matching.
## Search output
The results of the search is list in a citation-descending order. 

The link to the article, if available, is given in the gray url with the name of the journal (or arXiv) marked ahead.

Click the url linked to access to the PDF version of the article.

## Ciation
type `num` to get the bibTeX citation, which is by default copied to the clipboard.

## Statistics
Command `stat` plots the statistics of the author. With the blue bars showing the number of publications per year (green the Nature/Science/ARA&A paper and yellow the Physical Review papers) and the orange curve showing the average citations per paper per year. Here is an example of P. Abbott
![img](https://github.com/LiYunyang/ADS-command-line/blob/master/example/statistics.png)

## WordCloud
Command `wc` analyzes the word frequency of the titles of the search results (only in the author mode and python package [wordcloud](http://amueller.github.io/word_cloud/index.html) is required). Here is an example for Dr. Kip Thorne:
![img](https://github.com/LiYunyang/ADS-command-line/blob/master/example/wc.png)
