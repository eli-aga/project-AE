---
layout: default
---
[HOME](https://eli-aga.github.io/project-AE/) || [METHODOLOGY](./another-page.html) || [ENRICHMENT](./another-page3.html) || [DISCUSSION](./another-page2.html)



## Enrichment

Once we had decided to focus on the _Museo di Zoologia di Bologna_, we made use of LLMs (Chat GPT and Gemini) to enrich the existing information.

We began by asking them simple questions about what should be included in such a website. These are shown below. Here, we used the **zero-shot prompting technique**

![Screenshot 2024-06-18 at 19 02 36](https://github.com/eli-aga/project-AE/assets/171020684/598dbd15-07f2-4df8-b4f5-4342d20dec27)

![Screenshot 2024-06-18 at 19 02 59](https://github.com/eli-aga/project-AE/assets/171020684/5a718aac-e6b2-42d3-a696-ce4f9e8b0b20)

![Screenshot 2024-06-18 at 19 03 14](https://github.com/eli-aga/project-AE/assets/171020684/8cec874a-0770-4b71-83c8-8b55e388ab4c)

![Screenshot 2024-06-18 at 19 03 25](https://github.com/eli-aga/project-AE/assets/171020684/4536056f-5ab7-4394-a795-ca6cc0d7da76)


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

Finally, we asked Gemini and ChatGPT for some of the most important collections and artefacts present in the musuem. This was carried out using the **zero-shot prompting technique** It emerged that most of the collections present in the _Museo di Zoologia_ are not present in the ArCo database. We therefore proposed two final new triples to enrich the ArCo ontology with additional information


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




Here is an overview of the **prompting techniques** we used: 

1) **Zero-Shot prompting**: _Involves asking the model to perform a task without providing examples. This approach relies on the model's pre-trained knowledge to generate a response_
![Screenshot 2024-07-01 at 15 05 09](https://github.com/eli-aga/project-AE/assets/171020684/356a3522-52a3-4af5-8c88-915642dbb932)

2) **Few-Shot prompting**: _It refers to when a model adapts pre-trained language models quickly and effectively for new tasks or domains with only a few examples (shots) of data._

![Screenshot 2024-07-01 at 15 06 07](https://github.com/eli-aga/project-AE/assets/171020684/a60a106b-316d-4b3e-95fb-4416989bfec1)

3) **Generated Knowledge prompting**: _Involves generating a knowledge background that can help the model perform a task more effectively_
   
![Screenshot 2024-07-01 at 15 05 38](https://github.com/eli-aga/project-AE/assets/171020684/7f7fff5f-d546-4fec-aa06-6de7d9f633a1)


4) **Chain-of-thought prompting**: _It involves a series of examples that guide the tool to think through problems step-by-step._
5) 
![Screenshot 2024-07-01 at 15 06 56](https://github.com/eli-aga/project-AE/assets/171020684/5c55dbc6-1102-4bc1-ad05-7335e4557566)



Click [here](./another-page2.html) to read about our concluding remarks.


[back](./)
