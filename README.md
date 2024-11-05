## Task 1 
## Generating Causality Reports

# Introduction
Task 1 focuses on generating causality reports based on MIMIC-CXR data. The objective is to utilize radiology reports and images from the MIMIC-CXR dataset to uncover hidden causality relationships within the diagnostic process. Participants are tasked with using data to develop their own methods or models that can interpret the report content, aiming to generate a causality exploration report that mirrors the thought process of a radiologist.

![Diagram for Task 1](./images/Task1_bg.png "Task 1 Overview")

# Goal
The primary goal of Task 1 is to simulate diagnostic reasoning by identifying and documenting causality in radiology reports. By analyzing the MIMIC-CXR data, the generated causality report will help provide insights into the connections between findings, symptoms, and potential diagnoses. This task challenges participants to go beyond simple data analysis and delve into the reasoning process, offering a deeper understanding of radiological findings and their causal relationships.

# Input
Dir: This directory path contains the MIMIC-CXR files. It includes the reports (text files) and images (DICOM files) corresponding to each case. Participants can use this path to access the relevant files for processing.
Report_name: The name of the report file associated with each case. Each report provides a detailed analysis of the patient’s condition, which will serve as the basis for the causality exploration.
DICOM_name: The name of the DICOM file, which contains the CXR (Chest X-Ray) image associated with the report. Although the main focus is on the text report, participants may choose to incorporate image analysis if relevant.
Case_ID: A unique identifier for each case, linking it to a ground-truth causality report. The ground-truth report is created by radiologists and contains validated causality relationships, which participants can use as a benchmark for validation and evaluation of their own models.

# Output
The output of Task 1 is a causality exploration report. This report should provide a structured analysis of the radiology findings, highlighting potential causative relationships that could lead to a better understanding of the patient's condition. The report should reflect the diagnostic reasoning process by documenting how various symptoms and findings may be interlinked. For example, a finding of "pleural effusion" may be linked causally to "heart failure" if observed in the patient's medical history.

This exploration report should be generated through the participant’s own approach, using a method they design and implement based on the provided data. The output format should clearly delineate identified causal links and any inferred reasoning steps that mimic a radiologist’s analytical process.

# Process
Data Access: Locate the MIMIC-CXR data files using the directory path (Dir) and file names (Report_name and DICOM_name). Ensure you have the necessary permissions and tools to read both text and DICOM formats.
Analyze the Report: Process the text report to extract relevant medical terms, symptoms, findings, and potential diagnoses.
Generate Causality Analysis: Using your own model or method, identify and document causal relationships. For example, you may employ a text analysis model that recognizes patterns indicative of causation, such as certain phrasing or repeated co-occurrences of terms.
Format the Report: Present the causality report in a structured format that allows easy interpretation of causative links. Consider organizing the report by sections, such as "Symptoms and Findings," "Potential Causes," and "Diagnostic Insights."

# Example Structure of Output

