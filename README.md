# Task 1 README: 
# Generating Causality Reports

Overview
This task aims to generate a report that identifies hidden causality from MIMIC-CXR reports and the reading process. The output will provide insights into the diagnostic reasoning, incorporating the original MIMIC-CXR report data.

Data Description
Dir: The directory path containing the 'MIMIC report' and 'CXR image (DICOM file)' for each case.
Report_name: The filename of the 'MIMIC report' corresponding to each case.
DICOM_name: The filename of the CXR image in DICOM format for each case.
Case_ID: A unique identifier for each case, matching the corresponding 'Ground truth' report's name that contains medical professionals' causality insights. 

Input
MIMIC-CXR report data.

Output
A causality exploration report that highlights the inferred diagnostic reasoning based on the provided MIMIC-CXR report.
Steps for Data Use
Access the 'MIMIC report' and corresponding DICOM file using the paths in the 'Dir' column.
Process the report using your unique method (model) to generate a causality analysis based on the provided data.
Refer to 'Case_ID' for corresponding ground truth data to validate or compare results.

Task Objective
The goal is to leverage AI methods to interpret MIMIC-CXR reports and produce a causality report that aligns with the diagnostic flow used by medical professionals.
