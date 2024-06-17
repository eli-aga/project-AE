---
layout: default
---

## Methodology

The first thing we did was define an area of knowledge we were interested in.
We were interested in zoology, so we chose the class of **cultural institutions or sites**

The aim of our first query, shown below, was to find all the zoology-related sites present in ArCo, under the class Cultural Institution or Site


```js
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
```

This query gave us an extensive table of results, which included libraries, collections, and museums.

Our second query was carried out in order to count the results found, of which there were 71.

```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX cis: <http://dati.beniculturali.it/cis/>

SELECT (count(distinct ?cp) as ?count)
WHERE
{?cp rdfs:label ?label ;
rdf:type cis:CulturalInstituteOrSite .
FILTER(REGEX(?label , "zoo" , "i"))
}
```

Thirdly, we decided we wanted to explore in detail the zoological museums.
We ran this query, which meant we excluded the libraries and collections from the results:

```js
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
```


We then counted these zoological, or zoo-related museums present in ArCo under: Cultural Institutes or Sites and found 20

```js
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
```

Our fifth query aimed at specifying the region of these zoological museums. We wanted to explore zoological museums in the region of Emilia Romagna. 
Running the below sparql query, we found no results.

```js
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>

SELECT DISTINCT ?cp ?label
WHERE
{?cp rdfs:label ?label ;
rdf:type arco:CulturalInstituteOrSite
{?cp arco:regionIdentifier "8" }
UNION
{?cp arco:regionIdentifier "6" }
FILTER(REGEX(?label , "museo di zoologia" , "i"))
}
```

This could be due to a missing link between the zoological museums and their respective regions.

However, we decided to explore the “Museo di zoologia di Bologna” in more detail
![Screenshot 2024-06-17 at 19 39 29](https://github.com/eli-aga/project-AE/assets/171020684/5419dc35-a7f5-4ff8-9f67-d869f6231a2d)


The next step was then to use LLMs to enrich [Link to another-page2.md] the ArCo page about the Zoology Museum of Bologna (https://dati.beniculturali.it/lodview/mibact/luoghi/resource/CulturalInstituteOrSite/101952.html) 





[back](./)
