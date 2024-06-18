**ENRICHMENT** 

Once we had decided to focus on the _Museo di Zoologia di Bologna_, we made use of LLMs (Chat GPT and Gemini) to enrich the existing information.

We began by asking them simple questions about what should be included in such a website. These are shown below.
![Screenshot 2024-06-18 at 18 16 02](https://github.com/eli-aga/project-AE/assets/171020684/fafd6fd8-b7dd-493b-b64f-48053ba57f19)![Screenshot 2024-06-18 at 18 16 22](https://github.com/eli-aga/project-AE/assets/171020684/89a84436-8e08-4049-89f9-4275573755f2)
![Screenshot 2024-06-18 at 18 16 57](https://github.com/eli-aga/project-AE/assets/171020684/dcd1a7d9-1c1e-4fc9-9e4b-dff7f1c97a09)![Screenshot 2024-06-18 at 18 18 18](https://github.com/eli-aga/project-AE/assets/171020684/f9903881-1fdf-4f32-aad3-d1b813907c1e)
![Screenshot 2024-06-18 at 18 18 32](https://github.com/eli-aga/project-AE/assets/171020684/cebdde43-58b4-437d-8f23-35fe8cc9003d)![Screenshot 2024-06-18 at 18 19 10](https://github.com/eli-aga/project-AE/assets/171020684/5357e722-74e8-4fda-8b3a-ef778c0bcb40)
![Screenshot 2024-06-18 at 18 23 09](https://github.com/eli-aga/project-AE/assets/171020684/feda63bd-8ab7-472b-9ed5-33ef69201d91)![Screenshot 2024-06-18 at 18 23 26](https://github.com/eli-aga/project-AE/assets/171020684/f0ad9d65-3610-4b6f-bccc-8aa0b62eb511)
![Screenshot 2024-06-18 at 18 23 47](https://github.com/eli-aga/project-AE/assets/171020684/c19b2071-cadf-43fc-a08a-bea6bd067437)





[SCREENSHOTS]





This helped us to find out that the page of the Museo di Zoologia di Bologna could be improved: for example, ChatGPT proposed to add information about student resources.

Taking advantage of this, we created new triples based on the information provided by ChatGPT in order to enrich the _Museo di zoologia di Bologna_.


The first new triple we proposed was motivated by the fact that we needed to create a link between the University of Bologna and the Musueum, as the museum is an integral part of the University, but this was not specified in the general tab for the musuem in ArCo.

![Screenshot 2024-06-18 at 13 22 35](https://github.com/eli-aga/project-AE/assets/171020684/5c8ea48e-eb9b-4b94-b1bc-8b3e0ef251a9)

**NEW TRIPLE 1**
https://dati.beniculturali.it/lodview/mibact/luoghi/resource/CulturalInstituteOrSite/101952.html 
**core:isPartOf**
https://dati.beniculturali.it/lodview-arco/resource/University/UniversityOfBologna.html 

ChatGPT suggested we also implement a student-related aspect. It told us that the museum could have "internship and volunteer opportunities for students".
We therefore proposed the following triple:

**NEW TRIPLE 2**
http://unibo.it/resource/arco/universityOfBolognaStudentBody 
**arco-lite:isOrganiserOf**
http://example.org/bolognaZoologyExhibition
![Screenshot 2024-06-18 at 13 25 40](https://github.com/eli-aga/project-AE/assets/171020684/c61ae5fc-af0a-402a-ab6c-18974cb530fc)

We also wanted to specify that the museum was located in Bologna, so we proposed the following triple:

**NEW TRIPLE 3**

![Screenshot 2024-06-18 at 13 27 02](https://github.com/eli-aga/project-AE/assets/171020684/670a1125-4df5-4e05-91c5-a30662c6b03c)

https://example.org/city/bologna   
**core:isLocationOf**
https://dati.beniculturali.it/lodview/mibact/luoghi/resource/CulturalInstituteOrSite/101952.html

Finally, we asked Gemini and ChatGPT for some of the most important collections and artefacts present in the musuem. It emerged that most of the collections present in the _Museo di Zoologia_ are not present in the ArCo database. We therefore proposed two final new triples to enrich the ArCo ontology with additional information


**NEW TRIPLE 4**
https://dati.beniculturali.it/lodview/mibact/luoghi/resource/CulturalInstituteOrSite/101952.html 
**cis:involvesCulturalEntity**
https://w3id.org/arco/resource/ZoologicalHeritage/PesceLuna

![Screenshot 2024-06-18 at 13 29 21](https://github.com/eli-aga/project-AE/assets/171020684/a79775f4-133f-424b-b494-1ebc6ac28d0d)


**NEW TRIPLE 5**
https://dati.beniculturali.it/lodview/mibact/luoghi/resource/CulturalInstituteOrSite/101952.html 
**cis:involvesCulturalEntity**
https://w3id.org/arco/resource/ZoologicalHeritage/RinoceronteIndiano 

![Screenshot 2024-06-18 at 13 29 45](https://github.com/eli-aga/project-AE/assets/171020684/37be422e-2b1c-475e-b6e4-a1407a236788)

Click [here](./another-page2.html) to read about our concluding remarks.


[back](./)
