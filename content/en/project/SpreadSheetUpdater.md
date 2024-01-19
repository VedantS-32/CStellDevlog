---
author: "Vedant Shahare"
title: "SpreadSheet Updater"
date: 2024-01-07
description: "Automation python script to update data at specific position spreadsheet using Google Form"
tags: ["Spreadsheet", "GoogleAPI", "Python"]
thumbnail: "/CStellDevlog/SpreadSheetUpdater/SSUThumbnail.png"
---

### SpreadSheetUpdater

A simple python script to extract data collected from Google form and update data in Google Sheet at a specific location

[GitHub Repositary](https://github.com/VedantS-32/CStellDevlog/SpreadSheetUpdater.git)

### Why does this exist?

When I was living in a hostel, there I was given work to collect details from all 110+ students from our hostel. Collecting there Home Address, Home Number, Personal Number, College Name, Timing and 10 items more. That was too much for me to handle. So I found out that I can access Google Sheet with Python and also results from Google Form can be linked to Google Sheet.
And "this" came into existance.
Now students only needs to fill a simple Google Form to update their monthly details.
As for me, I just need to run "this" script.

### Requirements

- Python
- gspread Python Module
- Google Sheet API
- Google Drive API
- Google Cloud API key

### Authenticating

Fill your credential in following format in a separate .json file

``` json
{
  "type": "service_account",
  "project_id": "",
  "private_key_id": "",
  "private_key": "",
  "client_email": "",
  "client_id": "",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "",
  "universe_domain": "googleapis.com"
}
```

Accessing your credentials in main script

``` python
credentials = Credentials.from_service_account_file(
    'your_APIkeys.json',
    scopes=scopes
)
```

Open your Google Sheet by URL

``` python
# Opens Google Sheet by Url
sh = gc.open_by_url("your_Google_Sheet_URL")
```

### Specifying worksheet number and column

Here enter your Form and Main worksheet number

``` python
# Opens Google Form Sheet(Index 0) and Main Sheet(Index 1)
FormWorkSheet = sh.get_worksheet(0)
MainWorkSheet = sh.get_worksheet(1)
```

Enter Form Worksheet column number and Main Worksheet column number in enum
``` python
# Google Form Order
# Note while I was testing Columns in Form Spread Sheet
# was zeroth index for some reason
# be aware of this while setting enums
class FormField(Enum):
    TimeStamp = 0
    Name = 1
    Question1 = 2
    Question2 = 3
    Question3 = 4

# Google Sheet Order
# Columns in main worksheet are indexed from 1
class MainField(Enum):
    Name = 1
    QuesA = 2
    QuesB = 3
    QuesC = 4
    LastUpdate = 5
```

Now mention column numbers from Form to Main Worksheet like this
``` python
# Update QuestionA Field
if (FormRowValue[FormField.Question1.value] != ''):
    CellQuestionA = Cell(MainWorkSheetCell.row, MainField.QuesA.value, FormRowValue[FormField.Question1.value])
    CellToUpdate.append(CellQuestionA)
```

That's all you need to get this working

![FormWorksheet](/CStellDevlog/SpreadSheetUpdater/FormWorksheet.png)

In Action

{{< embedVideo "SSU" "/CStellDevlog/SpreadSheetUpdater/SSUClip.mp4">}}

### External

[GitHub Repositary](https://github.com/VedantS-32/CStellDevlog/SpreadSheetUpdater.git)

Thank you for reading!