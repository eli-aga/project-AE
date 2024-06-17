---
layout: default
---

## Methodology

The first thing we did was define an area of knowledge we were interested in.
We were interested in zoology, so we chose the class of **cultural institutions or sites**

The aim of our first query, shown below, was to find all the zoology-related sites present in ArCo, under the class Cultural Institution or Site




PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX cis: <http://dati.beniculturali.it/cis/>

SELECT DISTINCT ?cp ?label ?depiction
WHERE
{?cp rdfs:label ?label ;
rdf:type cis:CulturalInstituteOrSite .
FILTER(REGEX(?label , "zoo" , "i"))
OPTIONAL {?cp foaf:depiction ?depiction}
} 
ORDER BY (?label)
LIMIT 250

This query gave us an extensive table of results, which included libraries, collections, and museums.

Our second query was carried out in order to count the results found, of which there were 71.

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX cis: <http://dati.beniculturali.it/cis/>

SELECT (count(distinct ?cp) as ?count)
WHERE
{?cp rdfs:label ?label ;
rdf:type cis:CulturalInstituteOrSite .
FILTER(REGEX(?label , "zoo" , "i"))
}

Thirdly, we decided we wanted to explore in detail the zoological museums.
We ran this query, which meant we excluded the libraries and collections from the results:

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX cis: <http://dati.beniculturali.it/cis/>

SELECT DISTINCT ?cp ?label ?depiction
WHERE
{?cp rdfs:label ?label ;
rdf:type cis:CulturalInstituteOrSite .
FILTER(REGEX(?label , "museo" , "i"))
FILTER(REGEX(?label , "zoo" , "i"))
OPTIONAL {?cp foaf:depiction ?depiction}
} 
ORDER BY (?label)
LIMIT 250


We then counted these zoological, or zoo-related museums present in ArCo under: Cultural Institutes or Sites and found 20

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX cis: <http://dati.beniculturali.it/cis/>

SELECT (count(distinct ?cp) as ?count)
WHERE
{?cp rdfs:label ?label ;
rdf:type cis:CulturalInstituteOrSite .
FILTER(REGEX(?label , "museo" , "i"))
FILTER(REGEX(?label , "zoo" , "i"))
}




[back](./)
