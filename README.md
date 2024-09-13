Python Code for ECB SDMX File Modification

Purpose:
This script is designed as a business continuity solution for National Central Banks (NCBs) when there is an issue disseminating data to the ECB via SDMX for a particular reference period. 
In such cases, the NCB can send a temporary file where positions are retained, and flows are set to zero.

Functionality:
Handling Different Data Types:
For data types equal to "1" (typically representing positions), the script retains the obs_value and updates the OBS_STATUS.
For data types not equal to "1" (e.g., flows), the script changes the obs_value to "0.00" and updates the OBS_STATUS.
Updating the Reference Period:
The script updates the TIME_PERIOD in the XML file to reflect the current reference period (e.g., 2024-04).

Usage:
This script can be run when an NCB needs to send a temporary file to the ECB with the same positions but zero flows.
It modifies the provided XML file to meet ECB requirements in such scenarios, ensuring smooth data transmission despite technical issues.

Files:
Input: An XML file containing Investment Funds (IF) data.
Output: A modified XML file with updated obs_value for data types not equal to "1" and adjusted TIME_PERIOD.
