**Automated Timestamping with Google Apps Script: onEdit Checkbox Trigger**

This Script is that checks if a cell in Column D is ticked (assumed as a TRUE checkbox). If it is, it records the current date and time in the corresponding cell in Column F.

**Overview**
This repository contains a Google Apps Script that automates timestamping in a Google Sheet. Specifically, it monitors edits made to Column D (assumed to contain checkboxes) and automatically inserts the current date and time in Column F whenever a checkbox is ticked. If a checkbox is unticked, the corresponding date in Column F is cleared.

**Features**
1. Automatically records the date and time when a checkbox in Column D is ticked.
2. Clears the date and time when the checkbox is unticked.
3. Uses Google Apps Script to streamline automation and eliminate manual date entry.

**Prerequisites**
A Google Sheet with:
  - Checkboxes in Column D (4th column).
    - An existing structure to handle timestamping in Column F (6th column).

**How to Use the Script**
1. Open your Google Sheet.
2. Click on Extensions > Apps Script.
3. Copy and paste the code into the script editor from there.
4. Save the script.
5. Close the Apps Script editor and return to your Google Sheet.
6. Test the script by ticking and unticking checkboxes in Column D.

**Notes**
The script uses the onEdit trigger, meaning it runs automatically whenever a cell is edited.
Ensure your Google Sheet contains checkboxes in Column D to trigger the functionality.
The timestamp uses the user's local time settings from Google Sheets.

**Customization**
Feel free to customize the column numbers, functionality, or add more conditions based on your specific needs.

**License**
This project is open-source and available under the MIT License. Feel free to use, modify, and distribute it as needed.
