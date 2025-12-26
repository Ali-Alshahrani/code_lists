# Clinical Code Lists for CPRD-Based Research
This repository will contain structured clinical code lists used in CPRD and linked datasets for research in cardiovascular disease in patients with cancer_ An electronic health records study.
The code lists are structured for transparency, reusability, and reproducibility of research using routine healthcare data. They may be reused or adapted under the terms of the license below.

---

## Repository Structure
The repository is organised into three main sections:

### [`primarycare_codes/`](./primarycare_codes)

- Contains clinical codes from **CPRD Aurum** and **GOLD**, mapped to Read codes and SNOMED CT.
- Includes:
  - `af_codes.txt`: Atrial fibrillation
  - `hf_codes.txt`: Heart failure
  - `diabetes_codes.txt`: Diabetes mellitus
  - ...etc.

### [`secondarycare_codes/`](./secondarycare_codes)

- Contains **ICD-10** codes for diagnoses and **OPCS-4** codes for procedures.
- Used for linked **hospital episode statistics (HES)** and **National Cancer Registration Registration and Analysis Service (NCRAS)**.
- ICD-9 codes were reviewed but not relied upon in the study, as most study events occurred after the transition to ICD-10.
- Although both data sources (HES and NCRAS) use ICD-10 classification system, they differ in purpose and granularity: HES APC captures diagnoses related to hospital admissions and comorbidities, whereas NCRAS focuses on primary cancer site classification and is supplemented by morphology and behaviour information (ICD-O). To ensure harmonisation and reproducibility, code lists are curated to allow matching at both three- and four-character ICD-10 levels (i.e., low and high-level) where appropriate.

### [`helpful_resources/`](./helpful_resources)

- Includes guides, training materials, and resources on:
  - How to create, update, and validate clinical code lists
  - Mapping between Readcode, SNOMEDCT, ICD-10, and OPCS-4
  - Best practices in clinical codelist curation and FAIR data principles

---

## Code List Format

Each `.txt` file is **tab-delimited** and may contain the following columns depending on the source:

### For primary care (CPRD):

| Column               | Description                                      |
|----------------------|--------------------------------------------------|
| `medcodeid`          | CPRD MedCode ID                                 |
| `originalreadcode`   | Original Read code                               |
| `cleansedreadcode`   | Harmonised Read code                             |
| `snomedctconceptid`  | SNOMED CT concept ID (if mapped)                |
| `description`        | Clinical term description                        |

### For hospital (ICD / OPCS):

| Column         | Description                    |
|----------------|--------------------------------|
| `icd10code`    | ICD-10 diagnosis code          |
| `opcs4code`    | OPCS-4 procedure code          |
| `description`  | Clinical term description      |

---

## Curation and Methods

Most code lists in this repository were developed from scratch as part of the current CPRD-based research study. Code list development involved:

- Structured keyword searches in CPRD's medical dictionary browser and code list tools
- Iterative clinical review and refinement
- Mapping to SNOMED CT (for Aurum) and ICD-10 codes where applicable

###  Code Lists Adapted or Updated from Previous Sources

Some code lists were updated from previous projects led by researchers within our group or adapted from published external sources:

- **Atrial fibrillation** and **stroke** code lists were updated from earlier projects by colleagues (Alyaa Ajabnoor and others) in the same research unit
- **Dementia** and **severe mental illness** code lists were initially developed by Catherine Morgan, and updated for this study
- **Alcohol misuse** and **smoking** code lists were adapted from:
> Buzasi, E.; Carreira, H.; Funston, G.; Mansfield, K.E.; Forbes, H.; Strongman, H.; Bhaskaran, K. (2023).  
> *Codelists for: "Risk of fractures in half a million survivors of 20 cancers: a population-based matched cohort study using linked UK electronic health records"*.  
> London School of Hygiene & Tropical Medicine. https://doi.org/10.17037/DATA.00003415

All code lists were reviewed and revised for consistency within the context of this specific study.

---

## License

This repository is licensed under the **Creative Commons Attribution 4.0 International (CC-BY-4.0)**.

- You may **share**, **reuse**, and **adapt** these lists
- You must provide **appropriate credit** and link to this repository

See full license: [LICENSE](./LICENSE)

---


##  How to Cite This Repository

If you use these code lists in your research, please cite:

> Alshahrani AA, Kontopantelis E, Morgan C, Martin GP, Ravindrarajah R, Evison M, Mamas MA.  
> Clinical Code Lists for CPRD-Based Research on Cardiovascular Disease in Patients with Cancer. GitHub Repository.
> https://github.com/Ali-Alshahrani/code_lists. Licensed under CC-BY-4.0.

---

## Contact

**Ali Alshahrani**  
PhD Researcher, The University of Manchester  
[ali.alshahrani@manchester.ac.uk](mailto:ali.alshahrani@manchester.ac.uk)

---

## Related Resources

- CPRD documentation: https://www.cprd.com/primary-care 
- HES APC documentation : https://www.cprd.com/sites/default/files/2024-11/HES_APC_Documentation_v2.9.pdf 

