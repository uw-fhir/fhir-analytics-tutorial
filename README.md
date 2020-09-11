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
- https://github.com/uw-fhir/fhir-analytics-tutorial/blob/master/bulk-fhir-tutorial.ipynb

## Creating a FHIR-enabled EMR data pipeline

### Step One: Access data at the source

** Install OpenMRS**
For the purpose of this demo, we'll be using OpenMRS - a widely-used open-source EMR - as our source of point-of-care clinical information. You can give the EMR a whirl here: https://openmrs.org/demo/

Next, you'll need to install an instance of OpenMRS. The easiest approach is to download the *standalone* edition of the recent *2.10.0* release of the *OpenMRS Reference Application*, which you can download on this page: https://openmrs.org/download/

Once you download and unzip the file, follow the instructions in the `Readme` to get OpenMRS up and running locally. 

If you're more developer-minded and want to jump right into learning the ropes of OpenMRS development, you can install your instance following the instructions in the excellent OpenMRS Developer Manual, which you can find here: http://devmanual.openmrs.org/en/Technology/getSetUp.html. 


**Add the FHIR2 Module**

We're going to be using the new FHIR module that's currently under development. In order to get this module up and running, you need to remove the old FHIR module from your OpenMRS installation. Go into the unzipped folder, go into the `appdata/modules` directory, and delete `fhir-1.20.0.omod`. 

Then, download the following file and add it to the same directory: https://www.dropbox.com/s/v79lxvsm8oqg3kh/fhir2-1.0.0-SNAPSHOT.omod?dl=1

---

### Step Two - Synchronizing data with the target
   
(TODO: Elaborate)
Then, follow the instructions here to set up the rest of the dependencies:

https://github.com/GoogleCloudPlatform/openmrs-fhir-analytics

Extraction of Patient Data
1. Streaming
    - Live updates to a live feed of resources that need to be uploaded
    - Patient Creation
    - Patient Update
2. Batch
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

## Other Notes
1. Need to understand what data is there and how it is represented (Job of FHIR)

2. Need to expose this data externally in a standard way (FHIR)

3. Need to retrieve large amounts of data from across patients / providers efficiently (FHIR Bulk Data Access)

4. Cannot overload resources required to support healthcare operations (FHIR Bulk Data Access)
