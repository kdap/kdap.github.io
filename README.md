## Knowledge Data Analysis and Processing Platform

This library contains a collection of utilities for efficiently processing Knol-ML database dumps. There are two important features that this module intends to address: providing standard algorithms and efficient parsing of Knol-ML dump.


### Bsic Example

KDAP is easy to use and can work on any of the knowledge data. Based on the standarization of Knol-ML platform, inter-portal analysis and knowledge building analysis can be performed efficiently. KDAP also represents the revision based data in compressed form, because of which a large data dump can be stored easily in RAM, achieving the parallel processing.

```markdown
# import the KDAP method

`from kdap.converter.wikiConverter import wikiConverter`
`from kdap.converter.qaConverter import qaConverter`
`from kdap.analysis import knolAnalysis`

# Download and convert the datadump of apple.stackexchange
`qaConverter.download_qna('Stack Overflow',download=True,post=True)`

# count words in each thread
`knolAnalysis.countAllWords(dir_path='path_of_directory')`



For more details see [GitHub Page](https://github.com/descentis/kdap).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kdap/kdap.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
