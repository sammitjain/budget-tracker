# Budget Tracking with Google Sheets, Google Forms, Siri Shortcuts (WIP)

Google Sheets + Forms Setup to track expenses quickly and effectively without other 3rd party apps/dependencies. Keep track of Income/Expense of different kinds, Credit Card usage, Budget targets all in one spreadsheet. Here's how this works  
- Google Sheets to track and maintain expenses (and income).
- Google Form to quickly record expenses (and income).
- Both of these are web-based environments and therefore work super well as app-like shortcuts on your mobile homescreen.
- [New](https://github.com/sammitjain/budget-tracker-datastudio) - Use Google Data Studio to turn your Google Sheet into a beautiful dashboard

## Forms + Sheets + Data Studio Workflow
<img src="https://user-images.githubusercontent.com/29622482/185693437-cad54fc0-ceae-42c6-bfa4-c69f5e3e8df8.jpeg" alt="mobile_UX" width=240>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img alt="googledatastudio_expenses" src="https://user-images.githubusercontent.com/29622482/194036520-cf8f18b5-700e-4f68-80d9-d5c7b1c11e32.png" width=300>

<img src="https://user-images.githubusercontent.com/29622482/185695489-b4b2ec49-4173-4e82-8520-7459e2d84221.png" alt="dashboard" width=500>


## Siri Shortcuts Integration (Work in progress)
<img src="https://user-images.githubusercontent.com/29622482/185752191-14ee30a8-a86c-4a2b-8165-6d5c936d5294.png" alt="siri_integration" width=200>&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/29622482/185752253-b64977ad-3a83-4aec-9a8d-186b56bdf6a5.png" alt="siri_integration" width=200>&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/29622482/185752261-4c5bd382-50c5-427c-961d-2d13b029b9fe.png" alt="siri_integration" width=200>&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/29622482/185752262-4c9499a6-0e86-4e59-a92c-7e494f46c437.png" alt="siri_integration" width=200>

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

## Quick Update!
There's a more mobile-friendly way of looking at the budget sheet. You can create beautiful dashboards with minimal effort that look like this:

![googledatastudio_expenses](https://user-images.githubusercontent.com/29622482/194035913-7c2b9948-9a55-47bb-a152-841f32cbd832.png)

Check [this](https://github.com/sammitjain/budget-tracker-datastudio) out if you're interested in setting it up.
## Bonus: Siri (WIP)
Filling out the form too frequently can become cumbersome and that is one of the major drawbacks of a system like this one. 
A potential solution is setting up *Siri* to guide me through the form filling process - this is much more User Friendly than scrolling/clicking/typing inside the browser. Here's the [video](https://drive.google.com/file/d/1f9f0Est9_7SU09_xNYFyNJKLnQpAuooh/view?usp=sharing) of this in action.

The best part - this works hands-free, so it's easy to track expenses while you're on the move.
The template for this isn't quite ready yet but it's can be set up if you know your way around Forms + Siri Shortcuts. I'll share a more user-friendly template soon.

### Get Siri Shortcuts to work right away
* Download my `.shortcut` file and import into Siri Shortcuts.
* Get a pre-filled URL to your Google Form. It will look similar to the one inside the shortcut
* Separate out various elements and update entry IDs inside the shortcut
* This might take some effort right out the box

If you found this helpful, I look forward to hearing from you. Always up for a coffee. 

<a href='https://ko-fi.com/sammitjain' target='_blank'><img height='35' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' />
