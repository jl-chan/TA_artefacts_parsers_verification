# TA_artefacts_parsers_verification
Streamline tasks by generating Excel templates for parsers CIM validation, saving the team 15-30 minutes for the need to manually making the template every time.

## Outcome of the Python Script
Given a sample file containing the detailed list of newly onboarded devices as shown:
![Sample_Input](https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/screenshots/Generate_Parsers_Verification_Template_Before.png)

Manually, we need to split the entries into different tabs according to the data model each entry is associated with:

1. **Single Data Model Entry:**
   
   For entries using only one data model, such as the Authentication data model:

   - Create a new tab named "DM-Authentication."
   - Copy and paste the entry into this new tab.
   - Then, we could fill in later with the necessary screenshots and validation details for the entry parser's completeness validation status.

2. **Multiple Data Model Entry:**

   For entries using more than one data model, such as both the Authentication and Change data models:

   - Copy and paste the entry into each relevant data model tab.
   
   For example, 
   - As the aboved sample input, the first entry is using only the Authentication data model, create the tab "DM-Authentication" and paste the entry there.
   - As the aboved sample input, the second entry uses both Authentication and Change data models, proceed as follows:
     - Leave some space (approximately 40 rows) in the "DM-Authentication" tab for the content of the first entry.
     - Paste the second entry after the space in the "DM-Authentication" tab.
     - Create a new tab named "DM-Change" and copy and paste the second entry into this tab as well.
     
By following these steps, you will organize the entries according to their respective data models, ensuring each tab is correctly populated for further validation and completeness checks. Outcomes are as shown below:

Three data model are in use and hence three tabs are created. And for each tab contains entries that has associuated with the data model respectively:

The "DM-Authentication" tab
![Sample_Output_DM_Authentication](https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/screenshots/Generate_Parsers_Verification_Template_After1.png)

The "DM-Change" tab
![Sample_Output_DM_Change](https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/screenshots/Generate_Parsers_Verification_Template_After2.png)

The "DM-Database" tab
![Sample_Output_DM_Database](https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/screenshots/Generate_Parsers_Verification_Template_After3.png)

***With the scripts, the boring manual splitting entries job can be done, we could generate the template immediately and continue with just filling in the content with the necessary screenshots and validation details for the entry parser's completeness validation status.***


## Instructions for Running the Python Script

To run the Python script, please follow the steps below:

1. **Install Required Libraries:**
   
   Make sure to install the required libraries by using the provided `requirements.txt` file. Run the following command in your terminal:

   ```sh
   pip install -r requirements.txt
   ```
 
   This command will install all the necessary packages listed in the requirements.txt file.    
    <br /><br />
2. **Sample Input and Output Files:**

   - **Sample Input File:** [`Log Verification_DC_Exit_Sample.xlsx`](
https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/Log%20Verification_DC_Exit_Sample.xlsx)
   - **Sample Output File:** [`Log Verification_DC_Exit_Sample_v20240704_175158.xlsx`](https://github.com/jl-chan/TA_artefacts_parsers_verification/blob/main/assets/Log%20Verification_DC_Exit_Sample_v20240704_175158.xlsx)
  
   The sample output file name will include a timestamp, which allows you to differentiate between different versions of the file generated at different times.    
<br /><br />
3. **Running the Script:**

   Download the sample input file and place it in the same directory as the Python script. Run the script to generate the expected output file, which will contain the timestamp in its filename.

By following these steps, you will be able to run the Python script and obtain the desired output file.
