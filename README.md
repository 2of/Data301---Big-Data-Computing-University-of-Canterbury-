# Data301: Big Data Computing, University of Canterbury 2020
##Final Assignment Submission for DATA301 


Use your favourite Notebook editor to run the code, Note that due to the reliance on pulling a lot of data from [The GDELT Project](https://www.gdeltproject.org/), this book should only be considered as reference.


Some notes about using this course as reference.
This submission received a **Perfect** A+ Score in 2020, However:
  * Most of the time allotted was during a national Lockdown, grading was most likely affected
  * You should show scalability, a small part of this assignment creates psuedo-country codes and false data to 'simulate' extra data, proceed with caution
  * This is ordinarily a group assignment
  * This Project failed to correctly run on a google cloud instance
These are all things that should be considered


##**Synopsis**
The Goal: Analyse massive numbers of articles, identify their key public area of concern, the 'unrest-fulness' of the content, and country. Identify the 'calmest' and make reccommendations for which areas of concern, regarding covid 19, should be most shown and in what tone to reduce unrest in the most unrestful countries.
Motivation at the time was the COVID19 protests in the US, contrasting to the reasonably peaceful (and very successful) rule-following here in new zealand, countries where the state of the media are so vastly contrasting.
 

GDELT is a project which aggegates news articles published online worldwide, strips away *fluff* and analyses automatically elements like *tone* *actors* and *locations* involved in these articles, among around a hundred other categories. By analysing what articles, sorted by three letter country codes, are saying about covid and categorising them into the following categories using keyword anaylsis,

'''
  model = {}
  healthcare = {'doctor','hospital','medical','health','nurse','equipment','dying','patients','health'}
  laws = {'legistlation','referendum','legal','laws'}
  politics = {"leader",'majority','opposition'}
  police = {'laws','secutity','protest','unrest',}
  economy = {'fiancial','security','ratepayers','economic'}
  education = {'school','teacher','education','learning'}
  international_relations = {'emmigration','immigration','international','relations'}
  general_public_interest ={'work','family'}
  
'''

the articles were associated with a public interest. Then we simply grouped the most similar articles from a normalized vector with tone weightings :

''' 
  [% of healthcare related articles, % of laws related articles.... ]

'''


And simply by choosing the most similar, the overall reccommendation of 'how can we reduce unrest by changing which categories the media focuses on about covid 19, referencing the protests re: lockdowns at the time (USA)' we are 
