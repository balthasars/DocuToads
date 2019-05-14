# DocuToads

DocuToads is an open source minimum edit distance algorithm written in Python 2.7 that can handle cut-paste edit operations, created by Henrik Hermansson, who reserves some rights. This code may be modified and used by anyone, granted that this source is cited.

## Instructions

1. The texts
   1. DocuToads accepts texts in .txt, utf8 format. Make sure all your texts are in this format.
   1. If you want to perform an article-by-article comparison of the two texts, you need to mark the break-points between articles.
     1. DocuToads finds the break-points using a regular expression which is looking for the word DTBREAKPOINT. Insert this word between each article (not before the first nor after the last). 
1. Install Python 2.7 and the following necessary Python packages:
   1. time
   1. math
   1. string
   1. re
   1. os
   1. sys
   1. traceback
   1. pp
   1. numpy
   1. subprocess
   1. pylab
   1. collections
   1. csv
   1. matplotlib
1. A list of cases
   1. By a "case" is meant one pair of texts to be compared
   1. You will need a python list of cases where each entry (case) is a list containing (in string format) in the correct order:
     1. Path to `text 1`
     1. Path to `text 2`
     1. Short name for `text 1`
     1. Short name for `text 2`
     1. Short name for case
     1. A list of article names in the first text, for example: ["Article 1", "Article 2", "Article 3"]. Make sure the list matches the actual number of articles separated by DTBREAKPOINT markers. Enter empty list if you don't want to perform article-by-article comparison of the two texts.
     1. A list of article names in the second text. Make sure the list matches the actual number of articles separated by DTBREAKPOINT markers. Enter empty list if you don't want to perform article-by-article comparison of the two texts. 
   1. Name this lists "caselist" and enter into `DocuToads_main.py`.
1. Set the parameters
   1. Open `DocuToads_main.py` and enter the following parameters:
     1. `outpath` – The path of the desired output folder, no need to worry about sub-folders
     1. `plottype` – Determines which kind of graph to create - "block", "bar" and "line" are available. If no plot wanted set to "none".
     1. `backtrace` - Determines whether to save a table of the exact edit operations found, i.e. the backtrace. Set to "yes" or "no".
     1. `by_article` - Determines whether to split results article-by-article, based on the first text. Set to "article" or "noarticle".
     1. `cutoff` - Determines how many words in sequence there must be for the algorithm to detect a transposition, default value is 5.
     1. `ncpus` – Determines how many CPU:s DocuToads will use to process several cases simultaneously. Default is 1.
1. Run `DocuToads_main.py`
