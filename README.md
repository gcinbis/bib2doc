# bib2doc
A tool to automatically generate bibliography in various formats (HTML, TEX, etc) from text-based records

## Installation
Simply clone the git repository to use the most recent code, or, use `pip install bib2doc`.

## List of utilities
* bib2doc  Auto-create bibliography web or tex page based on a jinja template. (An example output can be found <a href="http://user.ceng.metu.edu.tr/~gcinbis/publications.html">here</a>.)

## Database file format

Bibliography data should be stored as a YAML file that consists of a set of entries, one entry per paper 
(See [examples/data.yaml](examples/data.yaml)).

The set of all possible fields (define only the ones that are relevant and known):

| FIELD        | DEFINITION |
| ------------ | --------- |
| type         | journal,  conference,  national,  report,  presentation,  book_chapter,  under_review,  working_paper|
| img          | Link to teaser image. |
| pdf          | Link to the pdf file|
| slides       | Link to slides|
| code         | Link to code|
| data         | Link to data|
| journal      | Name of the journal. Only for "journal" publications, everything else should use "booktitle".|
| booktitle    | Vanue name for conference, under-review (including journals), etc publications.|
| award        | HTML snippet for award info|
| author       | Author list, in the form of "G. Hinton, Y. LeCun"|
| author2      | Author list, in the form of "Geoffrey Hinton, Yann LeCun"|
| bibauthor    | Author list to be used for bibtex generation|
| selected     | Add selected=1 for selected publications |
| month        | Numeric month|
| month4sort   | Numeric month, just to define ordering priority among papers published in the same year.|
| year         | Publication year|
| doi          | DOI number |
| issn         | ISSN number |
| pages        | Page range (start_page-end_page).|
| volume       | Volume. |
| jindex       | null,  "SCI",  "SCI-E"|
| note         | Some additional note (like LNCS reference)|
| ...          | Any other field can be added if useful.|

 
