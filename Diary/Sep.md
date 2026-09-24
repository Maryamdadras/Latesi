14 september 2026:
Thesis & Project Tasks

Literature Review: Research existing literature and best practices regarding the digitalization of cultural heritage. This will form the theoretical and methodological framework for your thesis.

Read the PND: Read the Piano Nazionale di Digitalizzazione (PND) PDF that the professor shared with you in the chat to understand the national guidelines.

Choose a Dataset: Decide which collection you want to focus on for the metadata enrichment phase. The two options are:

Option A (Ancient Coins): More complex, as evaluating external sources requires specific archaeological competence.

Option B (Modern Coins/Medals): 19th-century artifacts from the Italian Risorgimento museum.

Option B is chosen.

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



------------------------------------------------------------------------------------
15 september 2026:
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

------------------------------------------------------------------------------------

17 September 2026:

The meeting with Silvia:

Crucial Things to Take Note Of:

1. The team is balancing strict national guidelines (PND) with the harsh physical realities of digitization. You need to document these constraints in your thesis as part of your "Risk Management" and "Methodology" sections:
    1. The Human Factor (Fatigue): Digitizing is physically taxing. The professor capped the estimate at 60 shots (30 coins) per hour for a maximum of 4 hours per day to prevent the operators from losing their minds staring into a lightbox. This translates to about 120 coins a day, requiring 40–45 workdays. 
    2. The "Naming" Risk: Typing inventory numbers manually is a massive risk. The protocol is to use the museum-provided Excel sheet to copy and paste the 4-digit ID directly into Capture One as the photos are taken. This ensures the RAW files are "christened" correctly from the start. 
    3. The PND Resolution Conflict: The National Digitalization Plan (PND) requires 5,000 pixels on the long edge, but physically shooting tiny coins with a macro lens maxes out around 3,800 pixels. The team will note this technical reality in the EXIF metadata rather than artificially upscaling the images. 
    4. Asynchronous Post-Processing: The capture PC cannot handle shooting and post-processing simultaneously. Data will be backed up to an external hard drive every session so post-processing (RAW to TIFF/JPEG conversion and cropping) can happen on a different workstation. 
    5. The Color Checker Compromise: A standard color checker won't fit in the macro frame with the coin, and the client wants the final images cropped on a black background anyway. The team will use the color checker for initial/final calibration, but it won't be in every individual cropped shot. 
2. Your Immediate Action ItemsHere is exactly what you should do to establish yourself as the project's digital humanist and process manager:Set up the "Logical Sensors" Tracker: The professor specifically asked you to track productivity during the first few days. Set up an Excel or Google Sheet (to be synced locally via a mobile hotspot, since you won't have admin Wi-Fi access). Create columns for: Date, Session Duration, Operator, Number of Coins Processed, and Notes/Bottlenecks. 
    Draft the Initial Gantt Chart: Use the professor's rough math to draft a baseline project timeline.
    Total Items: ~4,074 coins/medals (270 Risorgimento + 3,804 archaeological). 
    Pace: 120 coins per 4-hour session.   
    Timeline: ~34 sessions.
    Map this out from now until December, assuming 2 to 4 sessions a week depending on museum availability.   
    
    Document the Pre-Flight Checklist: Silvia will write down the physical setup requirements based on the meeting. This includes the lightbox, cables, power strip, extension cord, polarizing filter (for shiny silver/bronze coins), external hard drive, and the museum's pre-supplied Excel inventory.   
    
    Attend the First Shoot: Take the professor up on his offer to join the first session. Your job isn't to take the photos, but to observe the workflow, time the actual process (are they hitting 30 coins an hour?), and document any unforeseen issues.

Key Takeaways & Workflow Constraints:

Inventory & Naming Protocol: The museum must provide the Excel inventory before shooting begins. To avoid losing track of physical items, the 4-digit inventory ID will be copy-pasted directly from the Excel sheet into Capture One during the shoot. 

Physical-to-Digital Correspondence (Risk Management): Because the Risorgimento coins lack physical ID tags (talloncini) and our team lacks the numismatic expertise to identify them by sight, the museum curators must take full responsibility for the physical-to-digital link. During the shoot, a curator must physically hand us each coin and explicitly state its exact inventory number (e.g., "This is inventory 14753"). Only then will the operator place it in the lightbox, shoot it, and paste that ID into Capture One. This protocol protects the team from liability and prevents the irreversible mislabeling of historical artifacts.

The Bottleneck (Operator Fatigue): Shooting continuously in a dark room with a lightbox causes severe eye strain. The workflow is strictly capped at ~60 shots (30 coins) per hour, for a maximum of 4 hours per day (approx. 120 coins/day). Each coin needs two shots, one from the front and one from the back and 30 seconds for each shot which will be a minute for each coin. and of course in first days, will we should count the number of the coins that we will take the photo of them per day, and have a more accurate estimation based on that. 

Timeline & Effort Estimation:
Total Asset Volume: The project comprises a total of 4,074 items, which includes 3,804 archaeological items and 270 Risorgimento medals.

Production Speed: The maximum sustainable shooting speed is estimated at 60 photos per hour. Because each item requires an obverse and reverse shot, the processing rate is 30 items per hour.

Daily Capacity & Fatigue Limits: To mitigate operator fatigue and eye strain from the lightbox, shooting is strictly capped at 4 hours per session, resulting in a maximum daily output of 120 items.

Total Estimated Effort: Dividing the 4,074 items by the daily capacity of 120 items yields a required effort of 34 working days (or capture sessions) to complete the physical digitization.

Calendar Projection: Because the museum schedule may not accommodate a 5-day work week, these 34 sessions will be spread out over several months, projecting a completion date around December before the holidays.

Bidirectional Naming & Tracking Protocol: The museum must provide the Excel inventory before shooting begins. To avoid losing track of physical items, a strict two-way tracking step is required during the shoot. First, the 4-digit inventory ID will be copy-pasted directly from the Excel sheet into Capture One to name the RAW file. Second, immediately after the shot is taken, the operator must record the camera's generated photo sequence number back into that exact row in the Excel sheet. This creates a foolproof, real-time cross-reference between the digital file and the museum's catalog data.

Data Management & "Daily -1" Post-Processing Workflow

    Cloud Syncing for Project Tracking: The master tracking spreadsheet and Gantt chart will be stored on OneDrive as a fixed local copy and synced via a mobile hotspot. This allows the team to track production metrics and project advancement in real-time without relying on the museum's restricted IT network.

    Session Cloning (Hard Drive Backup): Because the Nikon camera generates massive files that will quickly fill the capture PC's local storage, the entire Capture One working folder must be cloned to an external hard drive at the end of every shooting session.

    Parallel Post-Processing: The primary capture PC cannot be used for post-processing while a shooting session is actively taking place. The cloned external hard drive will be transferred to a NAS or a secondary workstation to perform the RAW to TIFF/JPEG conversions and image cropping in parallel.

    The "Daily -1" Quality Control Loop: Post-processing will strictly follow a "Daily -1" schedule, meaning the batch of 120–150 photos taken during a session is processed the very next day. This ensures that any critical capture errors are caught immediately before the physical coins are permanently archived away by the museum, preventing a cascading failure across multiple days of shooting.


The PND Constraint vs. Physical Reality: The PND requires color checkers in every shot. However, macro lenses physically cannot fit a standard color checker in the frame with a tiny coin without losing focus. The solution: calibration shots will be taken separately at the beginning and end of sessions, and technical parameters will be embedded directly into the EXIF metadata.

Equipment & Setup Checklist:

Lightbox, macro tubes, fake battery, and polarizing filter (for shiny silver/bronze coins).

External hard drive, extension cords, and power strips.

Plastic/metal tweezers and an optical center marker (sticker) to ensure coins stay on-axis when flipped from obverse (Dritto) to reverse (Rovescio).

A mobile hotspot (due to lack of admin Wi-Fi access) to sync the Excel sheets, "Logical Sensors" tracker, and Gantt chart via OneDrive.


Documents:
Official Project Authorization & Hardware AllocationDocument: Verbale di affidamento di beni mobili inventariati (Protocol 09_26)
Location: Museo civico Archeologico, via dell'Archiginnasio 2, 40124 Bologna.
Official Duration: September 18, 2026 – November 30, 2026. (Note: This tight deadline aligns with our projected 34 shooting sessions, meaning the physical digitization must be strictly completed before December).   

Assigned Institutional Equipment:
The following university-owned equipment has been officially assigned to Marco Serra and the sub-assigned team (Silvia, Paolo, Tommaso, Michela) for the digitization of the Risorgimento and Archaeological coin collections:   
Camera: NIKON D850 (44 Megapixel) with 24x120mm lens (Inventory: 01897 A.N5).   C
apture Station: Lenovo ThinkCentre M75s Gen2 Desktop PC (Inventory: 02272 A.N5).   Monitor: PHILIPS 23.8" 16:9 VGA + HDMI (Inventory: 02058 A.N5).   
Color Checkers: IMAGE ENGINEERING TE262-UTT-A4-1 and TE236 EXTENDED 1 (Inventories: 02398 A.N5 & 02399 A.N5).   

Project Manager Notes: This document proves that the team is working with a high-end 44 Megapixel sensor (Nikon D850). However, notice the lens is a standard 24-120mm, which explains why the team in the meeting was discussing bringing their own macro tubes or lenses to shoot the tiny coins properly!

Official Tender Specifications (Capitolato) - Numismatic CollectionsGeneral Constraints & DeliveryProject Framework: The digitization is part of the "SIMBOLO" project, funded by the PR-FESR 2021-2027. All activities must comply with the National Digitalization Plan (PND).   
Deadline: All interventions across the asset groups must be completed by November 30, 2026.   
Physical Location: The capture setup must be located at the Museo Civico Archeologico (Via dell'Archiginnasio 2) in an exclusive space (minimum 2 sq. meters) with controlled lighting.   
Asset Handling: All identification, inventory recognition, and physical handling of the numismatic assets will be performed exclusively by museum personnel.   
Group III: Archaeological Coins (Tabarroni Collection)Volume & Dimensions: 3,804 items (including 250 pieces of paper money). Coin diameters range from 5 mm to 100 mm.   Capture Standards: Minimum optical resolution of 600 PPI at the object's real dimension. The camera sensor must be perfectly parallel to the asset. Each shot must include a colorimetric and metric reference in the margins, and a dedicated ICC profile must be created per session. Minimum views required are Obverse and Reverse (Diritto/Rovescio).   File Deliverables: Uncompressed TIFF 6.0 (Master) and high-quality JPEG for web/IIIF (Derivative). Both formats must share the exact same filename. The derivative JPEG must be cropped to remove the colorimetric/metric references.   Naming Convention: InstituteCode + CollectionCode + ObjectCode + ViewIdentifier (D for Diritto, R for Rovescio) + Extension (e.g., MCABo_Num_95812D.tif).   Metadata: A MAG (Metadati Amministrativi Gestionali) XML file containing digitization info and MD5 checksums must be generated for each image.   
Group IV: Risorgimento Coins & Medals (XIX-XX Century)Volume & Dimensions: Approx. 270 items ranging from 20 mm to 60 mm in diameter.   
Capture Standards: Identical to Group III (600 PPI, parallel sensor, obverse/reverse views, colorimetric/metric references), but with an added requirement: the shot must explicitly include an indication of the object's identifying inventory number.   File Deliverables & Metadata: Identical to Group III (TIFF Masters, cropped JPEGs, matching filenames, and MAG XML metadata).   


questions:
as for the pictures of back and front of each coin we will use the sollution of adding D for the front (where the worth of the coin isn't mentioned) and R for the back (where the worth of the coin is mentioned) to the coin ID in the file name, what approach should we have for the Medals?

Should I just focus on the Risorgimento coins for now or the medals?