# Integrating external CDS services into the EMR with CDS Hooks

**Documentation** 
- https://cds-hooks.org/
- https://cds-hooks.hl7.org/

**Slides**
- https://github.com/uw-fhir/cds-hooks-presentation/blob/master/Remote%20Decision%20Support%20with%20CDS%20Hooks.pptx

**Tutorial**
- (Slides)https://github.com/uw-fhir/cds-hooks-presentation/blob/master/Lets%20Build%20CDS%20Hooks%20Services.pptx
- https://github.com/uw-fhir/cds-services-tutorial

# Data Pipelines with FHIR

This set of tutorials aims to provide a quick introduction the use of FHIR to enable analytics, reporting, and attaching 
FHIR endpoints to data pipelines.  

## FHIR Bulk Data Access (Flat FHIR)

**Documentation**
- https://hl7.org/fhir/uv/bulkdata/
- https://hl7.org/fhir/uv/bulkdata/export/index.html
- http://hl7.org/fhir/async.html

**Slides**
- https://docs.google.com/presentation/d/14ZHmam9hwz6-SsCG1YqUIQnJ56bvSqEatebltgEVR6c/edit#slide=id.g8c17644f87_23_919

**Jupyter Notebook Tutorial**
- https://github.com/uw-fhir/bulk-fhir-tutorial/blob/master/bulk-fhir-tutorial.ipynb

## Creating a FHIR-enabled EMR data pipeline

## Accessing data at the source
For the purpose of this demo, we'll be using OpenMRS - a widely-used open-source EMR - as our source of point-of-care clinical information. 

1. Intro to OpenMRS & Community
2. Intro to the FHIR squad and FHIR module
3. Quick OpenMRS setup + FHIR module + atomfeed module

4. Need to understand what data is there and how it is represented (Job of FHIR)

5. Need to expose this data externally in a standard way (FHIR)

6. Need to retrieve large amounts of data from across patients / providers efficiently (FHIR Bulk Data Access)

7. Cannot overload resources required to support healthcare operations (FHIR Bulk Data Access)


  
---

# Synchronizing data with the target
1. Streaming
2. Bulk

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


## Resource List
1. http://hl7.org/fhir/uv/bulkdata/export/index.html
2. https://www.hl7.org/fhir/async.html
3. https://smilecdr.com/docs/bulk/fhir_bulk_export.html
4. https://docs.google.com/presentation/d/14ZHmam9hwz6-SsCG1YqUIQnJ56bvSqEatebltgEVR6c/edit#slide=id.g8c17644f87_23_919
