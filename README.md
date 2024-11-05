# Task 1 : Generating Causality Reports

## Introduction
Task 1 focuses on generating causality reports based on MIMIC-CXR data. The objective is to utilize radiology reports and images from the MIMIC-CXR dataset to uncover hidden causality relationships within the diagnostic process. Participants are tasked with using data to develop their own methods or models that can interpret the report content, aiming to generate a causality exploration report that mirrors the thought process of a radiologist.

![Diagram for Task 1](./images/Task1_bg.png "Task 1 Overview")

## Goal
The primary goal of Task 1 is to simulate diagnostic reasoning by identifying and documenting causality in radiology reports. By analyzing the MIMIC-CXR data, the generated causality report will help provide insights into the connections between findings, symptoms, and potential diagnoses. This task challenges participants to go beyond simple data analysis and delve into the reasoning process, offering a deeper understanding of radiological findings and their causal relationships.

## Input
#### Dir: 
This directory path contains the MIMIC-CXR files. It includes the reports (text files) and images (DICOM files) corresponding to each case. Participants can use this path to access the relevant files for processing.<br>
Example: **./physionet.org/files/mimic-cxr/2.1.0/files/p10/p10000975**

#### Report_name: 
The name of the report file associated with each case. Each report provides a detailed analysis of the patient’s condition, which will serve as the basis for the causality exploration.<br>
Example: **s56016012.txt**

#### DICOM_name: 
The name of the DICOM file, which contains the CXR (Chest X-Ray) image associated with the report. Although the main focus is on the text report, participants may choose to incorporate image analysis if relevant.<br>
Example: **989619d4-840b984d-3188207f-1599e894-f3fdc15c.dcm**

#### Case_ID:
A unique identifier for each case, linking it to a ground-truth causality report. The ground-truth report is created by radiologists and contains validated causality relationships, which participants can use as a benchmark for validation and evaluation of their own models.<br>
Example: **bcd4a40c-ac9c-4ba4-913c-2ae6834f3b7d**

## Output
The output of Task 1 is a causality exploration report. This report should provide a structured analysis of the radiology findings, highlighting potential causative relationships that could lead to a better understanding of the patient's condition. The report should reflect the diagnostic reasoning process by documenting how various symptoms and findings may be interlinked. For example, a finding of "pleural effusion" may be linked causally to "heart failure" if observed in the patient's medical history.

This exploration report should be generated through the participant’s own approach, using a method they design and implement based on the provided data. The output format should clearly delineate identified causal links and any inferred reasoning steps that mimic a radiologist’s analytical process.

## Process
**Data Access**: Locate the MIMIC-CXR data files using the directory path (Dir) and file names (Report_name and DICOM_name). Ensure you have the necessary permissions and tools to read both text and DICOM formats.<br>
**Analyze the Report**: Process the text report to extract relevant medical terms, symptoms, findings, and potential diagnoses.<br>
**Generate Causality Analysis**: Using your own model or method, identify and document causal relationships. For example, you may employ a text analysis model that recognizes patterns indicative of causation, such as certain phrasing or repeated co-occurrences of terms.<br>
**Format the Report**: Structure the causality analysis into a clear format. Create a section titled "Causal Exploration" where you will output the analyzed causality information. This "Causal Exploration" section should capture all identified causative links and reasoning based on the provided data. Submit this "Causal Exploration" section, not the full report.

## Example Structure of Output

![Example for Task 1](./images/Task1_ex.png "Task 1 Overview")
