# Notebook Documentation
# Nikhil Vasudeva
This is documentation to explain what was done for the following notebooks since it may be confusing to the reader:

- **Netflix_Movies_And_Shows_Cleaning.ipynb**
- **Netflix_Movies_And_Shows_StringRepresentation.ipynb**  


The first notebook was made to clean the data for Dataset 1. Around 4 to 5 columns contained 31 or less missing values, so the rows
with missing entries in those columns were removed. Only 1 column, 'director', contained a large amount of missing values. I could
not simply remove rows with missing values in this column because it would greatly reduce the size of the dataset which could
cause a loss in valuable information. After discussing with my team, we realized that a missing director value, meaning the director 
was unknown, could actually give insight into how popular the movie/show was. Thus, any missing value in that column was replaced 
with 'unknown'. In the future, when we are analayzing out data, we will try to see if an unknown director has correlation to popularity.
The 'rating' column also has missing values after cleaning, but I did not touch this because with previous experimentation, when
merged with the other dataset, the missing values are negated. 

The 'cast' and 'listed_in' columns also had to be handled as they are lists. In the future, it may be difficult to work with list 
data, so I had to figure out how to represent these columns in a numerical way. Recommended by Anthony, I created two new columns that
represent the mean frequency of the cast members in each row in comparison to the whole dataset. This is done for the 'listed_in' 
column as well. 

The second notebook is a very small addition to the first. Majority of the code is a copy of the first notebook, but at the end, I 
add some code. In the future, this will be done all in one notebook to avoid confusion, but since it is still in experimentation, I 
keep it in a separate notebook. Dr. Mallavarapu suggested we use features like the following to represent string based features:

Length: The number of characters in the string
Word Count: The number of words in the string (split by spaces or punctuation).
Character/Word Frequencies: The count or proportion of specific characters or words. 
Presence of Specific Substrings: Boolean flags indicating whether certain words or patterns are present.

The main concern we have is the description column, which is literally a paragraph description of the movie/entry. This notebook
adds code to count the total number of words in the descriptions for the whole dataset while getting rid of common English words
like "is, a, etc." For the 7293 rows, there are 17152 unique words. This is a lot of words! To actually find meaning in the
description column, I used vectorization to represent how many words each description has in this "bag of words." We also find
out what the top 50 words are in this bag. If the descriptions contains 2,3, or 4 or more words in top 50 bank, we denote it with
a true or false value. This adds 3 more columns to our wrangled dataset. 
