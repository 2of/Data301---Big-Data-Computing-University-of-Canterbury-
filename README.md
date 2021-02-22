# Data301: Big Data Computing, University of Canterbury 2020
## Final Assignment Submission for DATA301 


Use your favourite Notebook editor to run the code, Note that due to the reliance on pulling a lot of data from [The GDELT Project](https://www.gdeltproject.org/), this book should only be considered as reference.


Some notes about using this course as reference.
This submission received a **Perfect** A+ Score in 2020, However:
  * Most of the time allotted was during a national Lockdown, grading was most likely affected
  * You should show scalability, a small part of this assignment creates psuedo-country codes and false data to 'simulate' extra data, proceed with caution
  * This is ordinarily a group assignment
  * This Project failed to correctly run on a google cloud instance


**These are all things that should be considered, do not use this as anything but a reference for how previous students have approached the problems.


## **Synopsis**
The Goal: Analyse massive numbers of articles, identify their key public area of concern, the 'unrest-fulness' of the content, and country. Identify the 'calmest' and make reccommendations for which areas of concern, regarding covid 19, should be most shown and in what tone to reduce unrest in the most unrestful countries.
Motivation at the time was the COVID19 protests in the US, contrasting to the reasonably peaceful (and very successful) rule-following here in new zealand, countries where the state of the media are so vastly contrasting.
 

GDELT is a project which aggegates news articles published online worldwide, strips away *fluff* and analyses automatically elements like *tone* *actors* and *locations* involved in these articles, among around a hundred other categories. By analysing what articles, sorted by three letter country codes, are saying about covid and categorising them into the following categories using keyword anaylsis,


```python
  model = {}
  healthcare = {'doctor','hospital','medical','health','nurse','equipment','dying','patients','health'}
  laws = {'legistlation','referendum','legal','laws'}
  politics = {"leader",'majority','opposition'}
  police = {'laws','secutity','protest','unrest',}
  economy = {'fiancial','security','ratepayers','economic'}
  education = {'school','teacher','education','learning'}
  international_relations = {'emmigration','immigration','international','relations'}
  general_public_interest ={'work','family'}
  #code ommitted
  
```


the articles were associated with a public interest. Then we simply grouped the most similar articles from a normalized vector with tone weightings :

```python
  [% of healthcare related articles, % of laws related articles.... ]

```


With the vectorization done, we can compare different countries, look at clustering using *cosine similarity* and make a reccommendation.


## Usage


Import to google collab and run. You may need to set some time aside to pull data from GDELT. However, simply choosing which cells to run is sufficient.

Download / Analysis time for gdelt in a google collab instance was upwards of 4 hours for several hundred thousand articles.
