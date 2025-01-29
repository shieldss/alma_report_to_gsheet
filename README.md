# alma_report_to_gsheet

<h2>What the project does</h2>

Use this code to import an Alma Analytics report into a Google Spreadsheet for easy manipulation of data and displaying it on the web.

<h2>Why the project is useful</h2>

<h2>Prerequisites</h2>
<ul>
<li>A Google account to create a Google sheet.</li>
<li>An Alma API key to access analytics reports through their REST API.  For more information, visit https://developers.exlibrisgroup.com/alma/apis/</li>
</ul>

<h2>Getting Started</h2>

In Google Sheets, create a new file.

Go to Extensions > Apps Script

Copy and paste the code from 'alma_report_to_gsheet' to the code window and click 'Save'.

![Alt text](images/code_screenshot.png?raw=true "Example of Code")

Go to 'Project Settings' in the left Side bar. Scroll all the way to the bottom to locate 'Script Properties'

Create a new property named 'API_KEY' and enter your api key in the 'Value' field. Be sure to save it.

![Alt text](images/api_key.png?raw=true "Enter the API Key")

Return to the code window and click 'Run'. You may get an error to begin with once the code runs but this is mainly to get you through the various permissions pages that initially appear when running a newly created script.

Make sure all of your work is saved and return to your Google spreadsheet.

Refresh your Google spreadsheet and you will see a pop window asking for the path to your Report. 

![Alt text](images/pop_up.png?raw=true "Enter the Path")

The URL for an Alma report will look something like this: 
https://api-na.hosted.exlibrisgroup.com/almaws/v1/analytics/reports?path=%2Fshared%2FWashington%20Research%20Library%20Consortium%20(WRLC)%20Network%2FReports%2FAPI%2FAPI%20rpt_clsreq&limit=1000&col_names=false&apikey=

Copy and paste the section after 'path=' and before '&limit=1000&col_names=false&apikey=' to get the required path.

Paste that text into the pop up window and click 'OK'

Wait a few seconds and the spreadsheet should be populated with your report data.

<h3>Scheduling a Report</h3>

Alma Analytics reports can be slow to load so caching them into a Google Spreadsheet is ideal.  You can schedule your script to run at any time to keep your reports up to date.

This can be done in the Apps Script Interface. Go to 'Triggers' in the left sidebar and click 'Add Trigger'.

Under 'Select event source' choose the time interval you wish for the report to refresh. Update the related fields below it and click 'Save'.

![Alt text](images/triggers.png?raw=true "Enter the Path")

Your report will now automatically update on your desired schedule.

