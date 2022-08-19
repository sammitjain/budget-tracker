# budget-tracker
Google Sheets + Forms Setup to track expenses quickly and effectively without other 3rd party apps/dependencies. Keep track of Income/Expense of different kinds, Credit Card usage, Budget targets all in one spreadsheet. Here's how this works  
- Google Sheets to track and maintain expenses (and income).
- Google Form to quickly record expenses (and income).
- Both of these are web-based environments and therefore work super well as app-like shortcuts on your mobile homescreen.

## Google Sheets ([Link to view sheet](https://docs.google.com/spreadsheets/d/1Xk02BzBike5RoEALE8rTHT_TwGrNbB3R-vG-iaO8-ek/edit?usp=sharing))
This is what the overall Dashboard looks like. More samples (images) in the samples folder.
![image](https://user-images.githubusercontent.com/29622482/185658089-6b46b98d-db95-4ffe-a303-f7c6e11ee3de.png)

## Google Forms ([Link to create your own copy](https://docs.google.com/forms/d/1BUTJ5y90_NdvGrV6U8_6c_3iX_fNs5TJnn1VZxLLst0/copy))
The complete form is also shared as a PDF in the samples folder.

## How to set this up?
* Make sure you're logged into your Google Drive
* Create copies of the sheet and the form. Here's how:
  * Open the google sheet using [this link](https://docs.google.com/spreadsheets/d/1Xk02BzBike5RoEALE8rTHT_TwGrNbB3R-vG-iaO8-ek/edit?usp=sharing).
  * `File -> Make a copy`
  * Note: This option is only accessible when you're logged into your Drive account.
  * The Form [link](https://docs.google.com/forms/d/1BUTJ5y90_NdvGrV6U8_6c_3iX_fNs5TJnn1VZxLLst0/copy) should directly suggest creating a copy once logged in.
* It's time to link your `form` to the `spreadsheet`.
  * Open your copy of the Form, head to the `Responses` tab, click on the green `Create Spreadsheet` button
  * Here, choose your copy of the Google `spreadsheet` in the Drive.
  * We're almost there.
* If you look at your `spreadsheet` closely, it now has a new sheet called `Form Responses`. This is the one we'll link to the back-end.
  * Rename this sheet to something simpler like `res` (I'm avoiding using `responses` because it's already there)
  * Head over to the sheet called `_responses` and in the first cell `A1`, change the formula to `=ARRAYFORMULA(res!A:I)`
  * We basically asked the back-end sheets to switch to the data in `res` (instead of the older `responses`)
* At this point, the dashboard and the rest of the sheets will look empty, so go ahead and fill out your form
  * Open your form and fill out your first expense. (you can also click on the preview button and then fill it there)
  * This should populate the sheet as expected
* Once the sheet+form setup is working, go ahead and customize the options in the google form, names of your credit cards, your spending categories, etc.
  * Note: Do remember that changing the sequence / number of questions in the form will affect everything! If doing this, be careful, and always make sure to check that the filters are using the correct column sequences.
* Happy Tracking!


