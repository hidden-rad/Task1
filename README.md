# Task 1 : Generating Causality Reports

## Introduction
Task 1 focuses on generating causality reports based on MIMIC-CXR data. Participants use radiology reports and DICOM images from the MIMIC-CXR dataset to uncover hidden causality relationships, simulating a diagnostic process. The image input (DICOM) is optional, allowing participants to decide whether to include the image data as part of their analysis. Additionally, participants may choose to incorporate their own knowledge bases, ontologies, or other external resources as optional inputs, further enhancing their causality analysis with additional context and domain-specific insights.

![Diagram for Task 1](./images/Task1_bg.png "Task 1 Overview")

## Goal
The goal is to simulate diagnostic reasoning by identifying and documenting causality within radiology reports. By analyzing MIMIC-CXR data, participants will generate a causality exploration report that reflects a radiologist’s thought process. This process can be enriched by optionally including image data or leveraging external resources, such as custom knowledge bases or ontologies, to improve the accuracy and depth of the causality exploration.


## MIMIC Data Folder structure
MIMIC-CXR v2.0.0 contains:

A set of 10 folders (p10 - p19), each with ~6,500 sub-folders. Sub-folders are named according to the patient identifier, and contain free-text reports and DICOM files for all studies for that patient


Free-text reports and images are provided in individual folders. An example of the folder structure for a single patient's images is as follows:

files

    └── p10

        └── p10000032

            ├── s50414267

            │   ├── 02aa804e-bde0afdd-112c0b34-7bc16630-4e384014.dcm

            │   └── 174413ec-4ec4c1f7-34ea26b7-c5f994f8-79ef1962.dcm

            ├── s50414267.txt

            ├── s53189527

            │   ├── 2a2277a9-b0ded155-c0de8eb9-c124d10e-82c5caab.dcm

            │   └── e084de3b-be89b11e-20fe3f9f-9c8d8dfe-4cfd202c.dcm

            ├── s53189527.txt

            ├── s53911762

            │   ├── 68b5c4b1-227d0485-9cc38c3f-7b84ab51-4b472714.dcm

            │   └── fffabebf-74fd3a1f-673b6b41-96ec0ac9-2ab69818.dcm

            ├── s53911762.txt

            ├── s56699142

            │   └── ea030e7a-2e3b1346-bc518786-7a8fd698-f673b44c.dcm

            └── s56699142.txt

Above, we have a single patient, p10000032. Since the first three characters of the folder name are p10, the patient folder is in the p10/ folder. This patient has four radiographic studies: s50414267, s53189527, s53911762, and s56699142. These study identifiers are completely random, and their order has no implications for the chronological order of the actual studies. Each study has two chest x-rays associated with it, except s56699142, which only has one study.


Ref: https://physionet.org/content/mimic-cxr/2.1.0/ 

## Data Format
The data for Task 1 is provided in CSV format, containing relevant information for each case in a structured tabular form. Each row in the CSV file represents a single case, with the following columns:

#### Dir: 
This directory path contains the MIMIC-CXR files. It includes the reports (text files) and images (DICOM files) corresponding to each case. Participants can use this path to access the relevant files for processing.<br>
Example: **./physionet.org/files/mimic-cxr/2.1.0/files/p13/p13369881**

#### Report_name: 
The name of the report file associated with each case. Each report provides a detailed analysis of the patient’s condition, which will serve as the basis for the causality exploration.<br>
Example: **s54086770.txt**

#### DICOM_name: 
The name of the DICOM file, which contains the CXR (Chest X-Ray) image associated with the report. Although the main focus is on the text report, participants may choose to incorporate image analysis if relevant.<br>
Example: **07145c92-7fd06870-9d53917d-067ad184-dbaa11d8.dcm**

#### Causal section:
A unique identifier for each case, linking it to a ground-truth causality report. The ground-truth report is created by radiologists and contains validated causality relationships, which participants can use as a benchmark for validation and evaluation of their own models.<br>
Example: **182f51c3-e5bc-4c19-97c1-3f427bf25af9**

## Output
The output of Task 1 is a causality exploration report. This report should provide a structured analysis of the radiology findings, highlighting potential causative relationships that could lead to a better understanding of the patient's condition. The report should reflect the diagnostic reasoning process by documenting how various symptoms and findings may be interlinked. For example, a finding of "pleural effusion" may be linked causally to "heart failure" if observed in the patient's medical history.

This exploration report should be generated through the participant’s own approach, using a method they design and implement based on the provided data. The report must begin with the fixed heading **"Causal Exploration:"** followed by the causality analysis text that reflects the diagnostic flow and reasoning. This structured format is required for consistency. The output format should clearly delineate identified causal links and any inferred reasoning steps that mimic a radiologist’s analytical process.

## Process
**Data Access**: Locate the MIMIC-CXR data files using the directory path (Dir) and file names (Report_name and DICOM_name). Ensure you have the necessary permissions and tools to read both text and DICOM formats.<br>
**Analyze the Report**: Process the text report to extract relevant medical terms, symptoms, findings, and potential diagnoses.<br>
**Generate Causality Analysis**: Using your own model or method, identify and document causal relationships. For example, you may employ a text analysis model that recognizes patterns indicative of causation, such as certain phrasing or repeated co-occurrences of terms.<br>
**Format the Report**: Structure the causality analysis into a clear format. Create a section titled "Causal Exploration" where you will output the analyzed causality information. This "Causal Exploration" section should capture all identified causative links and reasoning based on the provided data. Submit this "Causal Exploration" section, not the full report.

## Example Structure of Output

![Example for Task 1](./images/Task1_ex.png "Task 1 Example Structure")


