<!-- Required extensions: footnotes -->
# Summary of recommendations

The benefits of facilitating data sharing in health have been demonstrated during the COVID-19 crisis. The proposal of the European Commission for a ‘European health data space’ (EHDS) [^1] shows the huge interest in improving access to health data across Europe for secondary use.

While data analytics methods are increasingly offering new ways to help optimise operations and drive decision-making, regulatory and public pressure on privacy issues make the creation of the EHDS a complex process [^2].

Besides legal aspects, technological issues underlying the sharing and integration of health data are also being discussed within the medical informatics community. Despite many initiatives and projects for decades, data interoperability is still an unsolved task. Multiple health data interoperability standards such as openEHR [^3], HL7 FHIR [^4], ISO 13606 [^5], OHDSI OMOP [^6], etc. still co-exist, supporting sharing of data from electronic health records (EHRs) on the one hand, and research data on the other hand, but many implementations for them are not necessarily compatible. In fact, many hospital information systems and dedicated research databases do not yet comply with any of the mentioned standards although efforts are being made in that direction.

In the last years, there has also been a growing interest and effort from the different SDOs in aligning their models. Past European projects like NoE SemanticHealthNet [^7] worked on the idea that there is a need to propose methods for ontology-based interoperability. In the U.S., the CTSA ontology group has issued a White Paper on interoperability desiderata [^8].

OHDSI, a multi-stakeholder, interdisciplinary collaborative health data sharing initiative [^9], has established an international network of researchers and observational health databases with a central coordinating center housed at Columbia University. The recent experience of the OHDSI initiative has demonstrated how fast a new data model is being successfully adopted by a large community of users thanks to being open source and providing an increasing tools ecosystem.

Reflecting on the past and current data interoperability landscape we can think of a future scenario in which new data models, interoperability approaches and tools will emerge. This challenges the
community to build a common pan-European infrastructure that facilitates semantic data interoperability independently of specific standards, specifications or implementations.

The authors share the opinion of many renowned experts in the field that semantic resources and technologies, particularly health terminologies, ontologies and information models play a central role
here. The practice of Applied Ontology, i.e. the provision of formal descriptions of entities of the domain, will help create bridges across all existing representations based on data semantics and not only on informal structures or envelopes. This is also mentioned in a recent work in the context of the building of the Swiss Personalized Health Network (SPHN) [^10], in which the authors state that current trends in data interoperability have moved from a data model technocentric approach to sustainable semantics, formal descriptive languages, and processes [^11].

Based on our experiences and current state of the art research and implementations in data sharing, we provide a list of recommendations that can serve as a basis for future projects and inform
policy makers, industry and key stakeholders for future developments and research directions.

1. Data should be described by rich metadata (data about the collected data) and the latter should be shared as soon as possible since it does not contain patient data and does not require
ethical approval.
Metadata is a powerful resource for identifying, describing and processing data. It is crucial for semantic harmonization and data integration. Data providers should provide metadata
such as name and description of the data elements, their data types and list of permissible values. Based on this metadata, automatic methods can be implemented for their semantic
enrichment such as annotating them with identifiers from CVs and ontologies.

2. Metadata should follow the FAIR principles and be based on semantic metadata standards.

Using Fair Data Points (FDPs) for representing and sharing metadata has been proposed by the authors of the FAIR recommendations. It is a promising solution to follow a common approach
to publish semantically-rich and machine-processable metadata according to FAIR.
Representing metadata using FDPs will benefit from Semantic Web technologies, facilitating the automatic and meaningful combination and integration of data from multiple and possibly
heterogeneous data sets. It is important to highlight that FDPs address interoperability of the metadata but not of the data.

3. Metadata and data should be described using ontologies or terminologies as far as possible.

Data and metadata should be mapped to CVs and ontologies (e.g. SNOMED CT, LOINC, etc.). Automatic methods based on text mining can be implemented to support the mapping
process, e.g. via terminology server implementations.

4. The construction of ontologies and terminologies should be better coordinated.

An overarching ontological framework, e.g. a foundational ontology, can facilitate their integration. 
Since data and metadata will be encoded using multiple CVs and ontologies, correspondences between their terms and concepts must be established. Contributing to the coordinated
building of CVs and ontologies by following certain criteria or principles like ontologies from the OBO Foundry, and ideally within an overarching ontological framework, will facilitate their
integration. Thus, increased investment in ontology research and development should aim at best practices and engineering standards.

5. Data should be described in a flexible way to facilitate data conversion into multiple representations and follow FAIR principles.

RDF allows the representation of data using a flexible data model and facilitates accomplishing FAIR data principles. In addition, RDF can be used together with other formalisms when
needed for other types of information and purposes

6. Bridging methods for transforming data into other standardized or not representations should be based on ontologies.

Since there is no universal agreed standard or representation for clinical data, specific converters need to be implemented. They should be guided by the clinical content, encoded
using ontologies developed under an overarching ontological framework.


In addition to the above recommendations, none of them will succeed without appropriate opensource tools. The existence of reference implementations like in the case of the FDPs can facilitate the
adoption of the corresponding technology.

[^1]:European Health Data Space. European Commission site.
https://health.ec.europa.eu/ehealth-digital-health-and-care/european-health-data-space_en
(last accessed Sept. 22)
[^2]:Horgan D, Hajduch M, Vrana M, Soderberg J, Hughes N, Omar MI, Lal JA, Kozaric M, Cascini F,
Thaler V, Solà-Morales O, Romão M, Destrebecq F, Sky Gross E. European Health Data
Space—An Opportunity Now to Grasp the Future of Data-Driven Healthcare. Healthcare.
2022; 10(9):1629. https://doi.org/10.3390/healthcare10091629
[^3]: Kalra, D., Beale, T., & Heard, S. (2005). The openEHR foundation. Studies in health technology
and informatics, 115, 153-17
[^4]: HL7 FHIR. https://hl7.org/fhir/ (last accessed Sept. 22)
[^5]: ISO 13606 Standard, Part 1: Reference model.
https://www.iso.org/obp/ui/#iso:std:iso:13606:-1:ed-2:v1:en (last accessed Sept. 22)
[^6]: Hripcsak, G., Duke, J. D., Shah, N. H., Reich, C. G., Huser, V., Schuemie, M. J., ... & Ryan, P. B.
(2015). Observational Health Data Sciences and Informatics (OHDSI): opportunities for
observational researchers. In MEDINFO 2015: eHealth-enabled Health (pp. 574-578). IOS
Press.
[^7]: SemanticHealthNet project. https://cordis.europa.eu/project/id/288408/es (last accessed
Sept. 22)
[^8]: CTSA Whitepaper on ontology desiderata. ArXiV 4495999
[^9]: Hripcsak, G., Duke, J. D., Shah, N. H., Reich, C. G., Huser, V., Schuemie, M. J., Suchard, M. A.,
Park, R. W., Wong, I. C., Rijnbeek, P. R., van der Lei, J., Pratt, N., Norén, G. N., Li, Y. C., Stang,
P. E., Madigan, D., & Ryan, P. B. (2015). Observational Health Data Sciences and Informatics
(OHDSI): Opportunities for Observational Researchers. Studies in health technology and
informatics, 216, 574–578
[^10]: Swiss Personalized Health Network (SPHN). https://sphn.ch. (last accessed Sept. 22)
[^11]: Gaudet-Blavignac C, Raisaro JL, Touré V,Österle S, Crameri K, Lovis C. A National, Semantic-
Driven, Three-Pillar Strategy to Enable Health Data Secondary Usage Interoperability for
Research Within the Swiss Personalized Health Network: Methodological Study. JMIR Med
Inform 2021;9(6):e27591 doi: 10.2196/27591

Authors: Catalina Martínez-Costa (UM); Francisco Abad-Navarro (UM); Stefan Schulz (MUG); Katryna Cisek (TU Dublin); Julia Amann (ETH); Günter
Neumann (DFKI); Saadullah Amin (DFKI)
