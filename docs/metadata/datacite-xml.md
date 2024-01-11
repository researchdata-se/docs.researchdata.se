# DataCite XML

When a DOI is registred via DataCite metadata is provided. This metadata will be harvestable via OAI-PMH.

## Required fields

* Identifier
* Creator
* Title
* Publisher
* PublicationYear
* ResourceType

## Recomended fields

`TODO: recomended fields for researchdata.se` [issue #1](https://github.com/researchdata-se/docs.researchdata.se/issues/1)

Examle metadata for the resource [doi:10.5878/0n2y-dp56](https://doi.org/10.5878/0n2y-dp56)
```xml
<?xml version="1.0" encoding="utf-8"?>
<resource xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xsi:schemaLocation="http://datacite.org/schema/kernel-4 http://schema.datacite.org/meta/kernel-4.4/metadata.xsd" xmlns="http://datacite.org/schema/kernel-4">
  <identifier identifierType="DOI">10.5878/0n2y-dp56</identifier>
  <creators>
    <creator>
      <creatorName nameType="Personal">Skogh, Mårten</creatorName>
      <givenName>Mårten</givenName>
      <familyName>Skogh</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0002-6604-3359</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Chemistry and  Chemical Engineering, Chalmers University of Technology</affiliation>
    </creator>
    <creator>
      <creatorName nameType="Personal">Rahm, Martin</creatorName>
      <givenName>Martin</givenName>
      <familyName>Rahm</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0001-7645-5923</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Chemistry and  Chemical Engineering, Chalmers University of Technology</affiliation>
    </creator>
    <creator>
      <creatorName nameType="Personal">Lolur, Phalgun</creatorName>
      <givenName>Phalgun</givenName>
      <familyName>Lolur</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0002-3409-3415</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Chemistry and Chemical Engineering, Chalmers University of Technology</affiliation>
    </creator>
    <creator>
      <creatorName nameType="Personal">Barucha-Dobrautz, Werner</creatorName>
      <givenName>Werner</givenName>
      <familyName>Barucha-Dobrautz</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0001-6479-1874</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Chemistry and Chemical Engineering, Chalmers University of Technology</affiliation>
    </creator>
  </creators>
  <titles>
    <title xml:lang="en">The Electron Density: A Fidelity Witness for Quantum Computation</title>
    <title xml:lang="sv">The Electron Density: A Fidelity Witness for Quantum Computation</title>
  </titles>
  <publisher xml:lang="en">Chalmers University of Technology</publisher>
  <publicationYear>2024</publicationYear>
  <resourceType resourceTypeGeneral="Dataset" />
  <subjects>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p23053" classificationCode="p23053" xml:lang="en">computational chemistry</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p23053" classificationCode="p23053" xml:lang="sv">beräkningskemi</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p38991" classificationCode="p38991" xml:lang="en">quantum computers</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p38991" classificationCode="p38991" xml:lang="sv">kvantdatorer</subject>
    <subject subjectScheme="NASA Thesaurus" classificationCode="55671" xml:lang="en">electronic structure</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p6787" classificationCode="p6787" xml:lang="en">computers</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p6787" classificationCode="p6787" xml:lang="sv">datorer</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1801" classificationCode="p1801" xml:lang="en">chemistry</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1801" classificationCode="p1801" xml:lang="sv">kemi</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p21978" classificationCode="p21978" xml:lang="en">computational science</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p21978" classificationCode="p21978" xml:lang="sv">tillämpad beräkningsvetenskap</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p352" classificationCode="p352" xml:lang="en">sciences (branches of science)</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p352" classificationCode="p352" xml:lang="sv">vetenskapsgrenar</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p6227" classificationCode="p6227" xml:lang="en">natural sciences</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p6227" classificationCode="p6227" xml:lang="sv">naturvetenskaper</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p7462" classificationCode="p7462" xml:lang="en">computing devices</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p7462" classificationCode="p7462" xml:lang="sv">datorutrustning</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p2442" classificationCode="p2442" xml:lang="en">devices</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p2442" classificationCode="p2442" xml:lang="sv">apparater</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p250" classificationCode="p250" xml:lang="en">systems of a society</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p250" classificationCode="p250" xml:lang="sv">samhälleliga system</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p3358" classificationCode="p3358" xml:lang="en">systems</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p3358" classificationCode="p3358" xml:lang="sv">system</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1340" classificationCode="p1340" xml:lang="en">technical objects (physical objects)</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1340" classificationCode="p1340" xml:lang="sv">tekniska objekt (fysiska)</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p207" classificationCode="p207" xml:lang="en">inanimate objects</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p207" classificationCode="p207" xml:lang="sv">icke-levande objekt</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p4762" classificationCode="p4762" xml:lang="en">objects</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p4762" classificationCode="p4762" xml:lang="sv">entiteter</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1435" classificationCode="p1435" xml:lang="en">physical objects</subject>
    <subject subjectScheme="ALLFO" valueURI="http://www.yso.fi/onto/yso/p1435" classificationCode="p1435" xml:lang="sv">fysiska objekt</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="10407" xml:lang="en">Theoretical Chemistry</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="10407" xml:lang="sv">Teoretisk kemi</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="10399" xml:lang="en">Other Physics Topics</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="10399" xml:lang="sv">Annan fysik</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="103" xml:lang="en">Physical Sciences</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="103" xml:lang="sv">Fysik</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="104" xml:lang="en">Chemical Sciences</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="104" xml:lang="sv">Kemi</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="1" xml:lang="en">Natural Sciences</subject>
    <subject subjectScheme="Standard för svensk indelning av forskningsämnen 2011" classificationCode="1" xml:lang="sv">Naturvetenskap</subject>
  </subjects>
  <contributors>
    <contributor contributorType="Other">
      <contributorName nameType="Personal">Biznárová, Janka</contributorName>
      <givenName>Janka</givenName>
      <familyName>Biznárová</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0002-8887-8816</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Microtechnology and Nanoscience, Chalmers University of Technology</affiliation>
    </contributor>
    <contributor contributorType="Other">
      <contributorName nameType="Personal">Osman, Amr</contributorName>
      <givenName>Amr</givenName>
      <familyName>Osman</familyName>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Microtechnology and Nanoscience, Chalmers University of Technology</affiliation>
    </contributor>
    <contributor contributorType="Other">
      <contributorName nameType="Personal">Warren, Christopher</contributorName>
      <givenName>Christopher</givenName>
      <familyName>Warren</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0001-6195-2708</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Microtechnology and Nanoscience, Chalmers University of Technology</affiliation>
    </contributor>
    <contributor contributorType="Other">
      <contributorName nameType="Personal">Bylander, Jonas</contributorName>
      <givenName>Jonas</givenName>
      <familyName>Bylander</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0003-4521-710X</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Microtechnology and Nanoscience, Chalmers University of Technology</affiliation>
    </contributor>
    <contributor contributorType="Other">
      <contributorName nameType="Personal">Tancredi, Giovanna</contributorName>
      <givenName>Giovanna</givenName>
      <familyName>Tancredi</familyName>
      <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org/">0000-0002-3628-8398</nameIdentifier>
      <affiliation affiliationIdentifier="https://ror.org/040wg7k59" affiliationIdentifierScheme="ROR" schemeURI="https://ror.org/">Department of Microtechnology and Nanoscience, Chalmers University of Technology</affiliation>
    </contributor>
  </contributors>
  <dates>
    <date dateType="Issued">2024-01-11</date>
  </dates>
  <language>eng</language>
  <relatedIdentifiers>
    <relatedIdentifier resourceTypeGeneral="Dataset" relatedIdentifierType="DOI" relationType="IsVersionOf">10.5878/fa5f-xc72</relatedIdentifier>
    <relatedIdentifier resourceTypeGeneral="Text" relatedIdentifierType="DOI" relationType="IsReferencedBy">10.1039/D3SC05269A</relatedIdentifier>
  </relatedIdentifiers>
  <sizes>
    <size>3.42 GiB</size>
  </sizes>
  <version>1</version>
  <rightsList>
    <rights rightsURI="info:eu-repo/semantics/openAccess" />
    <rights rightsURI="https://creativecommons.org/licenses/by/4.0/" xml:lang="en">Creative Commons  Attribution 4.0 International (CC BY 4.0)</rights>
  </rightsList>
  <descriptions>
    <description descriptionType="Abstract" xml:lang="en">Electron densities calculated using physical (superconducting qubits) and simulated quantum computers for the hydrogen molecule (H2), lithium hydride (LiH), di-lithium (Li2), and hydrogen cyanide (HCN). Additionally, the reduced one-particle density matrix (1-RDM) and results of topological analysis for the mentioned molecules. Calculations on physical quantum hardware were performed on Särimner, a quantum processor with three superconducting qubits. Simulations of quantum computers were performed with Qiskit.</description>
    <description descriptionType="Abstract" xml:lang="sv">Elektrontäthet beräknad med hjälp av fysiska (supraledande kvantbitar) och simulerade kvantdatorer för väte molekylen (H2), litiumhydrid (LiH), di-litium (Li2) samt vätecyanid (HCN). Inkluderar även den reducerad enpartikeltäthetsmatrisen (one-particle reduced density matrix, 1-RDM) och resultat av topologisk analys av elektrontätheterna för molekylerna. Beräkningar på fysisk hårdvara utfördes på Särimner, en kvantprocessor med tre supraledande kvantbitar. Simulering av kvantdatorer utfördes med Qiskit, </description>
  </descriptions>
  <fundingReferences>
    <fundingReference>
      <funderName>Swedish Research Council </funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/03zttf063</funderIdentifier>
      <awardNumber>2018-0597</awardNumber>
    </fundingReference>
    <fundingReference>
      <funderName>Swedish Research Council</funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/03zttf063</funderIdentifier>
      <awardNumber>2022-06725</awardNumber>
      <awardTitle>NAISS</awardTitle>
    </fundingReference>
    <fundingReference>
      <funderName>Wallenberg Center for Quantum Technology (WACQT)</funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/004hzzk67</funderIdentifier>
    </fundingReference>
    <fundingReference>
      <funderName>European Commission</funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/00k4n6c32</funderIdentifier>
      <awardNumber>H2020-FETFLAG-2018-03</awardNumber>
      <awardTitle>OpenSuperQ</awardTitle>
    </fundingReference>
    <fundingReference>
      <funderName>European Commission</funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/00k4n6c32</funderIdentifier>
      <awardNumber>HORIZON-CL4-2022-QUANTUM-01-SGA</awardNumber>
      <awardTitle>OpenSuperQPlus100</awardTitle>
    </fundingReference>
    <fundingReference>
      <funderName>European Commission</funderName>
      <funderIdentifier funderIdentifierType="ROR" schemeURI="https://ror.org/">https://ror.org/00k4n6c32</funderIdentifier>
      <awardNumber>101062864</awardNumber>
      <awardTitle>Marie Skłodowska-Curie grant </awardTitle>
    </fundingReference>
  </fundingReferences>
</resource>
```

## References

[DataCite shema documentation](http://schema.datacite.org)