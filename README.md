# medstation-redesign
This is the redesign of the front-end for Butler Community College's Electronic Health Record system. The medstation-redesign project is also called MedstationV2

Demo: https://trentschnee.github.io/medstation-redesign/
## Contents:

- About Page
- Instructions Page
- Screenshots Page
- Libraries / Utilities Page
- Functionalities Page


About

MedstationV2 is a dynamic patient medical records system. This means patient pages are

generated with a template, which displays his or her chart data pulled from the database. Not

only do patient’s medication records show to the nursing students in the patient page, but the

students are also able to interactively scan medications and a patient wristbands with custom

Javascript functionalities. This of course simulates a clinical environment for the nursing

students.


Instructions

Refer to this part of the documentation for operation instructions, regarding MedstationV 2

Logging In

In order to login to MedstationV2, you need to login with an email and password. For
demonstration purposes only, any email and password should work with the project I have
submitted. However, in my full-stack web application, emails and passwords are verified within.

Note: In the github pages demo, you must refresh the page to see everything.


the sql database I have setup.

- Data Needed:
    o Any email
    o Any password

Logging Out

To log out, go to the top right hand corner of the screen and press “Logout”. For mobile users,
please click the hamburger dropdown icon and then press “Logout”.

Viewing A List of Patients

To see a list of all available patients, click the “Patient Records” link on the navigation bar.
Please note, you must be logged in to do this. Also you can view all the available patients by just
simply logging in.

**Viewing A Patient’s Medical Administrati** on Record

Once you have logged in, you should be able to see a patient selection window. From here you
will be able to see information about each patient such as the: age, gender, medication record
number, admission date, and the physician. If there are too many entries, you can choose to show
only 10,25,50,75, or 100. You can also search for your patient by entering in his or her name.
Once you have found your desired patient simply click the name to access the medication
administration records.

Scanning A Patient

The best way to scan a patient is to click in the input bar labeled “Scan patient” and scan the
patient’s wrist band. However, you can also manually scan the patient manually by entering in
the patient’s last name middle initial and first name in uppercase. Then press enter.

- Data Needed for Roberto A Hernandez:
    o Barcode: “HERNANDEZ ROBERTO A”


Scanning A Medication

Once the patient is scanned and you are able to click into a medication page, you will need to
scan the appropriate medication barcode and press enter. Once you have done this, the status
should display as “scanned”

- Data Needed for Clopidogrel:
    o Barcode: “CLOPID”
- Data needed for Metoprolol
    o Barcode: “METOIV”
- Data needed for NS Flush
    o Barcode: “NSFLU”
- Data needed for Heparin Bolus
    o Barcode: “HEPA1”
- Data needed for Heparin Infusion
    o Barcode: “HEPARINIV”
- Data needed for Morphine Sulfate
    o Barcode: “MORPHINE”
- Data needed for Sodium Choloride 0.9%
    o Barcode: “9%SODCHL”
- Data needed for Nitroglycerin
    o Barcode: “NITROG”
    o

Viewing Chart Data

To view the patient’s chart data, all you need to do is have the patient scanned and then click any
of the following tabs: history, orders, labs, and radiology.

Viewing New Orders

To view new orders, you must have the patient scanned first. Then you will be able to click the
“New Orders” tab. From there you should see similar chart data from Roberto Hernandez.
However, you will be able to see the medication discontinued from the old chart highlighted in
yellow.


Screenshots

Here is every page type/important front-end contents MedstationV2 has.

Login Page

Patient List Page

Medication Administration Records Page (Unscanned)


Medication Administration Records Page (Scanned)

Patient Tabs (Unscanned)

Patient Tabs (Scanned)


Medication Page (Unscanned)

Medication Page (Scanned)

New Orders

Footer


Error Popup


Libraries / Utilities

Here you can find all the libraries and utilities MedstationV2 uses to provide a rich experience
for users.

DataTables

DataTables, a plugin for JQuery, is utilized by this application to create highly attractive data
tables for the patient list and patient data. You can find out more about DataTables here:
https://datatables.net/

SweetAlert 2

SweetAlert2 is used for the responsive, customizability, and smooth design it provides for error
handling. By using SweetAlert 2 , we do not have the old alert() Javascript interface. You can find
out more about SweetAlert 2 here: https://sweetalert2.github.io/

JsBarcode

JSBarcode is utilized to generate barcodes for the patient charts. You can find out more about
JSBarcode here: https://lindell.me/JsBarcode/

PDFObject

PdfObject is a Javascript utility used for embedding PDF’s in a webpage. MedstationV2 uses
PDFObject for displaying particular chart data.


Functionalities

Here you can find all the custom and used functionalities MedstationV2 utilizes to make this
application possible.

Patient Barcode Scanner

The patient barcode scanner is a Javascript function which has been created to verify that the
correct patient’s barcode has been scanned. If the barcode matches what is on the page, the
program will redirect you to the scanned webpage. If the barcode inputted doesn’t match what is
on the page, the user will get a message like this:

For example, if you are on Roberto A Hernadez’s patient record and scan the barcode
“HERNANDEZ ROBERTO A” in the “Scan patient” input box, you should get redirected to a
new webpage. From here, you will be able to click the different medications and view the patient
charts such as: history, orders, labs, and radiology. This functionality provides security so that
the nursing student is absolutely on the right patient screen for his or her patient.

Medication Barcode Scanner

The medication barcode scanner is a javascript function which has been created to let the nursing
student know his or her patient’s correct medication has been scanned. If the barcode inputted
matches with what is on the page, the input box will turn green, along with the status message.
Then the input value will say what the specific medication is. For example, if you scan
“CLOPID” in the Clopidogrel page, the value of unscanned will change to “scanned” like this:


If the wrong medication is scanned, the user will get a notification like this:

Barcode Generator

JsBarcode is used to display a visual representation of what the patient’s barcode looks like. This
function is only on the new orders page and the scanned page. When the function is initiated, the
barcode looks something like this:


Displaying Chart PDF **’** s

If the patient isn’t scanned, the user will only be able to see this.

However, if the patient is scanned, the user will be able to access the chart data.


