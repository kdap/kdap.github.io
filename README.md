## Knowledge Data Analysis and Processing Platform

This library contains a collection of utilities for efficiently processing Knol-ML database dumps. There are two important features that this module intends to address: providing standard algorithms and efficient parsing of Knol-ML dump.


* Installation: pip install kdap
* Repositiory: Due to anonymization purpose, this repository has been hidden
* License: 3-Clause BSD

### Basic Example

KDAP is easy to use and can work on any of the knowledge data. Based on the standarization of Knol-ML platform, inter-portal analysis and knowledge building analysis can be performed efficiently. KDAP also represents the revision based data in compressed form, because of which a large data dump can be stored easily in RAM, achieving the parallel processing.

```markdown
# import the KDAP method

from kdap.converter.wikiConverter import wikiConverter
from kdap.converter.qaConverter import qaConverter
from kdap.analysis import knolAnalysis

# Download and convert the datadump of apple.stackexchange
qaConverter.convert('Stack Overflow',download=True,posthistory=True, post=True)

# Download Wikipedia article
wikiConverter.getArticle(file_name='', [output_dir=''])

# Convert Wikipedia article into Knol-ML
wikiConverter.compressAll(dir_name, output_dir='')

# Iterate over revisions
revisionList = knolAnalysis.getAllRevisions(file_name)
for rev in revisionList:
  revisions = knolAnalysis.wikiRetrieval(file_name,rev)
  for revision in revisions:
    # Write your analysis code here

# Count number of revisions
revCount = knolAnalysis.countRevInFiles([dir_path=''])

# Count users
userCount = knolAnalysis.countUsersInFiles([dir_path=''])

# Age of knowledge data
knolAge = knolAnalysis.getAgeOfKnowledge([dir_path=''])

# Retrieve knowledge data by date
knolByDate = knolAnalysis.knowledgeByDate(file_name, first_date[, last_date])

# count words in each thread
knolAnalysis.countAllWords([dir_path='path_of_directory'])

# count images in each file
knolAnalysis.getNumberOfImages([dir_path='path_of_directory'])

# Compute user contribution
knolAnalysis.getLocalGiniCoefficient([dir_path='path_of_directory'])

# Get edit statistics
knolAnalysis.getRevisionTypes([dir_path='path_of_directory'])

```

### ANALYSIS AND RETRIEVAL OF KNOWLEDGE DATASET 
As a part of KDAP, we are also maintaining the Analysis and Retrieval of Knowledge dataset, containing the knowledge dataset of  different collaborative portals including Wikipedia (all Featured articlesandGoodarticles), StackExchange network, and Wikia in Knol-ML format. Because of the anonimity purpose, we are not providing the link of dataset.

| Portal Name | Category | Description |
|-------|--------|---------|
| Wikipedia | All revision history | The dataset contains the the full revision history of all the Featured Articles and Good Articles in compressed Knol-ML format |
| Stack Exchange | All posts and Poshitory | All the questions, answers, votes and user's details of all the Stack Exchange websites in Knol-ML format |
| Wikia | All revision history | Full revision history of Wikia pages in Knol-ML format |
