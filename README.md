# budget-tracker
Google Sheets + Forms Setup to track expenses quickly and effectively without other 3rd party apps/dependencies. Keep track of Income/Expense of different kinds, Credit Card usage, Budget targets all in one spreadsheet. Here's how this works  
- Google Sheets to track and maintain expenses (and income).
- Google Form to quickly record expenses (and income).
- Both of these are web-based environments and therefore work super well as app-like shortcuts on your mobile homescreen.

<img src="https://user-images.githubusercontent.com/29622482/185693437-cad54fc0-ceae-42c6-bfa4-c69f5e3e8df8.jpeg" alt="mobile_UX" width=195><img src="https://user-images.githubusercontent.com/29622482/185695489-b4b2ec49-4173-4e82-8520-7459e2d84221.png" alt="dashboard" width=550>


## Google Sheets ([Link to view spreadsheet](https://docs.google.com/spreadsheets/d/1Xk02BzBike5RoEALE8rTHT_TwGrNbB3R-vG-iaO8-ek/edit?usp=sharing))
Check out different tracking sheets. If you'd like to use this same sheet as a template, follow along. If you were just looking for some inspiration, feel free to integrate things you like here into your own personal finance management system.

## Google Forms ([Link to create your own copy](https://docs.google.com/forms/d/1BUTJ5y90_NdvGrV6U8_6c_3iX_fNs5TJnn1VZxLLst0/copy))
The complete form is also shared as a PDF in the samples folder.

## How to set this up?
* Make sure you're logged into your Google Drive
* Create copies of the sheet and the form. Here's how:
  * Open the google sheet using [this link](https://docs.google.com/spreadsheets/d/1Xk02BzBike5RoEALE8rTHT_TwGrNbB3R-vG-iaO8-ek/edit?usp=sharing).
  * `File -> Make a copy`

  <img src="https://user-images.githubusercontent.com/29622482/185689092-50007366-7267-4131-8163-cf7b74f1f27e.png" width=500>

  * Note: This option is only accessible when you're logged into your Drive account.
  * The Form [link](https://docs.google.com/forms/d/1BUTJ5y90_NdvGrV6U8_6c_3iX_fNs5TJnn1VZxLLst0/copy) should directly suggest creating a copy once logged in.

  <img src="https://user-images.githubusercontent.com/29622482/185689230-48877933-4e33-4c68-9205-e72c585b352e.png" width=500>

* It's time to link your `form` to the `spreadsheet`.
  * Open your copy of the Form, head to the `Responses` tab, click on the green `Create Spreadsheet` button

  <img src="https://user-images.githubusercontent.com/29622482/185689449-679f48dc-23fa-486b-9934-8004016b163e.png" width=500>

  * Here, choose your copy of the Google `spreadsheet` in the Drive.
  * We're almost there.
* If you look at your `spreadsheet` closely, it now has a new sheet called `Form Responses`. This is the one we'll link to the back-end.

  <img src="https://user-images.githubusercontent.com/29622482/185689579-2aaaaee7-0af7-4018-b490-6068dbcac159.png" width=400>

  * Rename this sheet to something simpler like `res` (I'm avoiding using `responses` because it's already there)

  <img src="https://user-images.githubusercontent.com/29622482/185689644-a2f65c4d-0353-46f5-abed-fbaf00b5443d.png" width=300>

  * Head over to the sheet called `_responses` and in the first cell `A1`, change the formula to `=ARRAYFORMULA(res!A:I)`

  ![step8](https://user-images.githubusercontent.com/29622482/185689673-3d98320f-614b-4ea9-8b0d-fe257e2ea7f5.png)

  * We basically asked the back-end sheets to switch to the data in `res` (instead of the older `responses`)
* At this point, the dashboard and the rest of the sheets will look empty, so go ahead and fill out your form

![step9](https://user-images.githubusercontent.com/29622482/185689718-2e715539-6bef-469a-9143-5647b06773f9.png)

  * Open your form and fill out your first expense. (you can also click on the preview button and then fill it there)
  * This should populate the sheet as expected

  ![step11](https://user-images.githubusercontent.com/29622482/185689843-d56df56a-8850-4b8e-a82b-c2d094bb05f3.png)

* Once the sheet+form setup is working, go ahead and customize the options in the google form, names of your credit cards, your spending categories, etc.
  * Note: Do remember that changing the sequence / number of questions in the form will affect everything! If doing this, be careful, and always make sure to check that the filters are using the correct column sequences.
* Happy Tracking!

If you found this helpful, I look forward to hearing from you. Always up for a coffee @ https://ko-fi.com/sammitjain :)


