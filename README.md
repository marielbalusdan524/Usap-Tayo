USAP TAYO — GOOGLE SHEETS SETUP

FILES
- index.html: your questionnaire website
- Code.gs: receives the answers and saves them to your Google Sheet

1) CREATE YOUR SPREADSHEET
- Sign in to Google Sheets and create a blank spreadsheet.
- Name it "Usap Tayo Responses".
- Keep the spreadsheet private.

2) ADD THE DATABASE SCRIPT
- In the spreadsheet, choose Extensions > Apps Script.
- Replace the sample code in Code.gs with the contents of the supplied Code.gs.
- Save.

3) DEPLOY AS A WEB APP
- Click Deploy > New deployment > gear icon > Web app.
- Execute as: Me.
- Who has access: Anyone.
- Deploy and complete Google's authorization prompts.
- Copy the Web app URL ending in /exec.

4) CONNECT THE WEBSITE
- Open index.html in Notepad or another text editor.
- Find GOOGLE_SCRIPT_URL near the top of the script.
- Replace PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE with your /exec URL.
- Save the file.

5) PUBLISH index.html
- Upload index.html to a static website host that gives you a public HTTPS link.
- Share that public website link with the respondent.
- The Apps Script Web App URL is for connecting the form; it is not the website link.

VIEW ANSWERS
- Open your private Google Sheet. Each submission is saved as a new row.
- Test with a sample response and check the sheet before sharing the website.

IMPORTANT PRIVACY NOTES
- The form sends answers to your Google Sheet. Tell the respondent before they submit.
- Keep the spreadsheet private. Anyone with the web app endpoint may be able to submit data.
- The original login is checked in browser JavaScript, so it is only a simple screen, not secure authentication. The username/password can be discovered by inspecting the page.
- Do not put highly private or sensitive information in the form.
- The website uses a no-cors request, so the page cannot verify the server's response. Confirm that the test submission appears in your spreadsheet.
