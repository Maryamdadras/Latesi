14 september 2026:
Thesis & Project Tasks

Literature Review: Research existing literature and best practices regarding the digitalization of cultural heritage. This will form the theoretical and methodological framework for your thesis.

Read the PND: Read the Piano Nazionale di Digitalizzazione (PND) PDF that the professor shared with you in the chat to understand the national guidelines.

Choose a Dataset: Decide which collection you want to focus on for the metadata enrichment phase. The two options are:

Option A (Ancient Coins): More complex, as evaluating external sources requires specific archaeological competence.

Option B (Modern Coins/Medals): 19th-century artifacts from the Italian Risorgimento museum.

Acknowledge the Technical Workflow: Prepare to structure your project around four core phases:

Digitalization (image acquisition).

Post-processing (normalizing image geometry to fix macro-lens distortion).

Reconciling catalog data.

Descriptive enrichment (linking internal data with external Open Source databases).


Summary of the Professor's Statements

Focusing on establishing a workflow for the digitization and descriptive enrichment of a numismatic collection. He advises prioritizing a methodological approach over a content-driven one, noting that evaluating the strict historical validity of archaeological coins falls outside his technical expertise. By focusing on methodology, I can build a flexible pipeline that demonstrates how to effectively connect internal catalog data with various external open-source databases.

Regarding technical execution, the Professor clarifies that while I will not manage the physical camera setup, I must document the digitization phase as a project case study. He highlights a specific challenge: photographing high-resolution micro-objects like coins with macro lenses introduces geometric distortion. Consequently, my proposed workflow must incorporate a post-processing phase utilizing software libraries to normalize the image geometry before reconciling the technical metadata with the descriptive catalog data.

He instructs me to begin a literature review on digitization best practices, sharing the mandatory Italian Piano Nazionale di Digitalizzazione (PND) in the chat as my primary normative reference. Additionally, referencing external project materials can help me document the operational constraints as I structure the planning model for the shooting activities.


PND Summary:

Overview and Objectives
The document represents Annex 1 of Italy's National Digitalization Plan of Cultural Heritage (2022-2023) and provides technical and theoretical guidelines for cultural institutions undertaking digitization projects. The primary motivations for digitizing cultural assets include preserving physical originals, enhancing public access and valorization, facilitating scientific study and diagnosis, and recovering legacy digitization campaigns. Before digitization begins, assets must be carefully selected, inventoried, and assigned a unique physical identifier to link the physical object with its digital counterpart. To execute these tasks, the guidelines recommend assembling a multidisciplinary team that includes roles such as a Project Manager, Conservator, Restorer, Technical Operator, Cataloger, and IT specialists.   

Methodology and Technical Standards
The guidelines outline specific technical approaches and file formats based on the type of asset being digitized:

    2D and 3D Digitization: 2D scanning can be performed using various professional scanners (flatbed, planetary, virtual drum) or digital cameras, while 3D digitization relies on laser scanning and photogrammetry.   
    File Formats: For long-term preservation, master files must be uncompressed and lossless. Recommended master image formats are RAW (preferably DNG) and uncompressed TIFF (16 to 48-bit), whereas JPEGs are recommended for web access copies. Video masters should be captured in AVI 2160p 4K, and audio masters should use linear PCM in WAV or BWF formats.   
    Metadata: Projects must use the METS (Metadata Encoding and Transmission Standard) schema to organize digital objects. Metadata is categorized into descriptive, administrative (including technical and copyright data), structural, and preservation subsets. Technical metadata formats like Exif, IPTC, and XMP are used to record capture parameters.   
    File Nomenclature: Files must follow a strict naming convention to ensure unique identification: InstituteCode+ObjectCode+ProgressiveNumber.Extension.
    
Project Management, Quality Control, and StorageThe guidelines detail how to structure the administrative and logistical aspects of a digitization project.
    Cost Management: Project budgets must explicitly account for human resources, specialized equipment (purchased, rented, or outsourced), asset packaging, transport, insurance, and long-term storage infrastructure.   
    Quality Assurance: The document provides a framework for drafting technical tender specifications and mandates rigorous quality testing. This includes testing an initial technical prototype and conducting periodic checks during different progress stages (SAL) to evaluate image readability, completeness, resolution accuracy, and metadata linking.   
    Storage and Delivery: Final deliverables (master files, derivatives, and metadata) must be stored in duplicate on secure media. Approved storage solutions include Cloud infrastructures, designated digital libraries, Hard Disk Drives (HDDs), and NAS systems configured with RAID 1.  

DIGITALIZATION WORKFLOW BASED ON PND:

Preparation and Setup
    Assess the conservation status of the items and perform necessary physical cleaning or preliminary restoration.   
    Assign a unique physical identifier to each object to logically link the physical item to its catalog description.   
    Calibrate the optical equipment and create an input ICC color profile using specific targets like the ColorChecker.   

Acquisition (Scanning/Shooting)
    Capture the entire object, including blank pages, borders, and bindings, ensuring the sensor remains perfectly parallel to the subject.   
    Include a colorimetric and metric reference scale in the capture area, or produce a dedicated initial shot containing these references.   
    Save the initial digital capture strictly as an uncompressed RAW file, with DNG being the preferred format.   

Post-Production and Metadata
    Process images on calibrated monitors to generate a secondary uncompressed 16-bit or 48-bit TIFF master.   
    Apply minor necessary adjustments, such as white balance, brightness, and contrast, exclusively to the TIFF file to keep the RAW file unaltered.   
    Track all post-production modifications using open sidecar files, such as XMP.   
    Rename all files using the mandatory syntax: InstituteCode+ObjectCode+ProgressiveNumber.Extension.   
    Generate METS-compliant XML metadata to encode the structural, descriptive, technical, and administrative properties of the digital object.   

Quality Control and Storage
    Conduct a preliminary prototype test, followed by periodic quality checks at different project advancement stages to verify resolution, color accuracy, and file consistency.   
    Save all master files, derivatives, and metadata in duplicate across secure infrastructures such as a NAS, Cloud storage, or offline Hard Disks.  




17 september 2026:
Your Action Plan
To successfully model your thesis and internship project, you should actively document and prepare for the five workflow phases the professor outlined:

Phase 1: Data Normalization. It will be needed to take raw data (like Excel inventory lists provided by the museum) and convert them into a structured relational database that links physical objects to their source material.

Phase 2: Acquisition & Post-Processing. It will be needed to document how the physical scan is performed (e.g., scanning a full sheet) and how custom applications are used to crop individual objects, extract geometric coordinates, and save the files as Master (TIFF) and Derivative (JPEG) formats.

Phase 3: Internal Metadata Generation. It will be needed to learn to associate the cropped digital objects with administrative/technical metadata (EXIF camera data, MAG standards) and descriptive metadata (the museum's inventory text).

Phase 4: External Enrichment. This is where your methodological research comes in. You need to identify authoritative external databases (like Wikidata or VIAF) to enrich the local records with broader historical context.

Phase 5: Validation. Plan to present the final, enriched dataset back to the domain experts (e.g., the archaeologists or historians) to confirm that the structured data actually serves their research needs.

Your Action Plan
Incorporate "Logical Sensors" for Time Tracking: The professor highlights a major industry problem: the inability to estimate the time and cost of digitization projects due to a lack of historical data. Your workflow model must include timestamps (logical sensors) that record exactly when an object enters and exits a specific phase (e.g., administrative metadata entry).

Define a Requirement Analysis Phase: When linking external data sources (like Wikidata) to your digital objects, you cannot just link everything arbitrarily. Your methodology must include a formal requirement analysis step where you consult the domain experts (e.g., archaeologists, historians) to define exactly which external data is valuable to them.

Establish a Validation and Error-Tracking Loop: Your workflow must include Quality Assurance (QA). If errors are detected during validation, they must be tracked and categorized. If a specific error occurs repeatedly (e.g., 90% of the time), your methodology should dictate a return to the initial process design to fix the root cause.

Map the "Digital Humanist" Interventions: Your final thesis should serve as a step-by-step framework for anyone digitizing a collection for the first time. Clearly outline the workflow's start and end points, the individual steps, the specific criticalities/risks, and exactly where the Digital Humanist is required to intervene to guide the process.

Research Business Process Management (BPM): Start looking into process engineering literature applied to cultural heritage to back up your methodology. The professor mentions looking into the work of King's Digital Lab (specifically Elena/Arianna Ciula) and organizing your bibliography in Zotero.

OBJECTIVES:
1) PROCESS MODEL: list of distinct atomic steps that starts from the physical object to the final dataset delivery.
2) BASIC STEP DESCRIPTION: inventory collection and normalization, digital repro production, digital object post-production, technical metadata production, decriptive metadata production, external sources collection, dataset production, dataset validation.
3) METODOLOGICAL GUIDELINES: core requirements analysis, metadata collection guidelines, validation guidelines, performance and QA assessments. 


To do list:

Basic Step Descriptions
Once your skeleton list is approved, you will write a brief description for each phase the professor outlined:

Inventory & Normalization: Explain how you turn messy museum data into a relational database.

Digital Repro & Post-Production: Detail the camera setup, capturing the physical asset, fixing geometric distortion, cropping, and generating the Master TIFF and Derivative JPEGs.

Metadata Production: Define the technical metadata (EXIF, MAG) and how the descriptive metadata (inventory details) gets linked to the digital object using coordinates.

External Sources & Dataset Production: Describe the process of linking the object to Wikidata or VIAF.

 
Methodological Guidelines
This is where the "King's Digital Lab" engineering mindset comes into play. You aren't just describing what you did, but the rules for how anyone else should do it:

Requirement Analysis: Write the guidelines for how a digital humanist should sit down with domain experts (archaeologists/historians) to figure out which external data is actually worth linking.

Validation & QA: Outline your error-tracking loops. How do you measure the time a step takes? If you spot a repeated error in the metadata, what is the protocol for fixing the root cause?

