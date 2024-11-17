# GSHeet-Automatic-Date-Update
This Script is that checks if a cell in Column D is ticked (assumed as a TRUE checkbox). If it is, it records the current date and time in the corresponding cell in Column F.

**Overview**
This repository contains a Google Apps Script that automates timestamping in a Google Sheet. Specifically, it monitors edits made to Column D (assumed to contain checkboxes) and automatically inserts the current date and time in Column F whenever a checkbox is ticked. If a checkbox is unticked, the corresponding date in Column F is cleared.

Features
Automatically records the date and time when a checkbox in Column D is ticked.
Clears the date and time when the checkbox is unticked.
Uses Google Apps Script to streamline automation and eliminate manual date entry.
Prerequisites
A Google Sheet with:
Checkboxes in Column D (4th column).
An existing structure to handle timestamping in Column F (6th column).
How to Use the Script
Open your Google Sheet.
Click on Extensions > Apps Script.
Copy and paste the code into the script editor:
javascript
Copy code
function onEdit(e) {
  // Get the edited range and sheet
  var sheet = e.source.getActiveSheet();
  var range = e.range;

  // Only proceed if edits are made in column D (Column 4)
  if (range.getColumn() == 4) {
    var row = range.getRow();
    var value = range.getValue();

    // Check if the cell is ticked (TRUE indicates ticked)
    if (value === true) {
      // Record the current date and time in Column F (Column 6)
      sheet.getRange(row, 6).setValue(new Date());
    } else {
      // Optionally clear the corresponding cell in column F if unticked
      sheet.getRange(row, 6).clearContent();
    }
  }
}
Save the script.
Close the Apps Script editor and return to your Google Sheet.
Test the script by ticking and unticking checkboxes in Column D.
Notes
The script uses the onEdit trigger, meaning it runs automatically whenever a cell is edited.
Ensure your Google Sheet contains checkboxes in Column D to trigger the functionality.
The timestamp uses the user's local time settings from Google Sheets.
Customization
Feel free to customize the column numbers, functionality, or add more conditions based on your specific needs.

License
This project is open-source and available under the MIT License. Feel free to use, modify, and distribute it as needed.

