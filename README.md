# tlg-dataset

Dataset of News Articles for the Timeline Generation Problem. See [(Holt et. al 2016)](http://alta2016.alta.asn.au/U16/U16-1020.pdf).

## Data

###  Primary Dataset: `crowd.csv`
The primary dataset is comprised of the set of crowd-annotated articles for our entities. We define gold-standard timelines to be comprised of the articles which are labeled 'valid' and 'very important'. Columns:

- **entity**: The name of the entity.
- **URL**: Article URL.
- **valid**: Crowd-annotated label. An article is 'valid' if it is concerned with a single event in the history of the entity.
- **valid_conf**: Confidence of above annotation.
- **importance**: Crowd-annotated label. One of 'not', 'somewhat' or 'very' important.
- **importance_conf**: Confidence of above annotation.

### Secondary Dataset: `supplement.csv`

The secondary dataset is comprised of a number of entity-linked articles retrieved by querying Google News. Columns:

- **entity**: The name of the entity.
- **index**: The index of the article in the relevant Google News query.
- **URL**: Article URL.
- **published**: Publish date.
