# Data Pipelines with FHIR

This tutorial provides a quick intro to the


in the context of a contrived population/public Health data analysis scenario analyzing flu vaccinations. 

## Resources

1. http://hl7.org/fhir/uv/bulkdata/export/index.html
2. https://www.hl7.org/fhir/async.html
3. https://smilecdr.com/docs/bulk/fhir_bulk_export.html
4. https://docs.google.com/presentation/d/14ZHmam9hwz6-SsCG1YqUIQnJ56bvSqEatebltgEVR6c/edit#slide=id.g8c17644f87_23_919
5. https://github.com/dcinformatics/cds-hooks-presentation/blob/master/Remote%20Decision%20Support%20with%20CDS%20Hooks.pptx

## Outline

### CDS Hooks Tutorial
- Breeze through slides at https://github.com/uw-fhir/cds-hooks-presentation
- Look through CDS Hooks website
- Run through CDS Hooks Tutorial
- Highlight excercises

### Introduction to Pipelines
(look for slides)
- Intro to transactional vs. async
- Highlight OLAP vs. w/e, transactional vs. asynchronous 
- Highlight different reqs for each 

- Modified Bulk FHIR Slides

- Bulk FHIR tutorial
  
---

Once we get things out, what do we do then?

(Show diagram)

focus on pipeline to sync data with analytics platform

--> demo OpenMRS analytics project

Set Up: a FHIR-enabled open-source EMR
1. Intro to OpenMRS & Community
2. Intro to the FHIR squad and FHIR module
3. Quick OpenMRS setup + FHIR module + atomfeed module
   
Extraction of Patient Data
1. Streaming
    - Live updastes --> live feed of resources that need to be uploaded
    - Patient Creation
    - Patient Update
2. Bulk
    - FHIR Search API
    - Apache Beam API
    - non-standard hack
    - tie-in to bulk fhir export
  
Current application:
Shared Health Record based on the Internation Patient Profile for the Haitian Health System