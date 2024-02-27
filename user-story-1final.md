# Upload a CSV file and convert it to an array of objects

## Value proposition

As a user
I want to upload my csv file with data inside
So that I can finally generate a plot.

## Description

![wireframe Upload](/assets/Wireframe-User-Story-1bis.png)

## Acceptance criteria

- [ ] When the user clicks on the "Choose a file" button then an upload window opens where the user can select a file with a csv extension.
- [ ] When the user clicks on the "Submit" button an alert gets displayed with the text "File processed successfuly".
- [ ] Title at the top with the name of the website and a logo.
- [ ] Heading with text ""Step 1: Upload a CSV file to get the data.".
- [ ] Paragraph with text "Note: the file should have a header. Note: the file should be comma-delimited and the decimal separator for numbers should be a period (.). Note: if the file contains missing values, then replace these values in the file by null.".
- [ ] A button with a text "Choose a file" which starts the upload process and the default text "no file chosen" is displayed below.
- [ ] Once the file is uploaded the filename gets displayed.
- [ ] A button with text "Submit" which is disabled by default and becomes enabled once the upload is successful.
- [ ] The elements do not extend to each end of the page but are centered in the middle.

## Tasks

- [ ] Create a new feature branch - upload-data.
- [ ] Create the global styles
- [ ] Create an asset folder and put inside the image for the logo of the website.
- [ ] Create a Components folder with:

  - [ ] CenteredDiv component
  - [ ] Title component including the logo image.
  - [ ] Layout component which includes the title.
  - [ ] Integrate the Layout component in the \_app.js
  - [ ] Button component
  - [ ] InputTypeSubmit component.
  - [ ] Heading component
  - [ ] Paragraph component
  - [ ] FileUploader component with logic from the FileUploader.js file in https://codesandbox.io/p/sandbox/test-upload-conversion-csv-4-cfd2zh?file=%2Fsrc%2FFileUploader.js%3A1%2C1.
  - [ ] CorrectArrays component using the logic from the CorrectArrays.js file in https://codesandbox.io/p/sandbox/test-upload-conversion-csv-4-cfd2zh?file=%2Fsrc%2FCorrectArrays.js%3A5%2C1.

  - [ ] UploadData component

    - [ ] Install these libraries: convert-csv-to-array and convert-string-to-number.
    - [ ] Add const { convertCSVToArray } = require("convert-csv-to-array");
    - [ ] Declare a state for the variable keynames using useLocalStorageState with a default value set to [].
    - [ ] Declare a state for the variable vals using useLocalStorageState with a default value set to [].
    - [ ] Declare a state for the variable fileObj using useState with an initial value set to {}. This will contain the object representing the uploaded file.
    - [ ] Declare a state for the variable isUploaded using useState with an initial value set to false. This variable will contain the status about the upload and will serve to enable or disable the InputTypeSubmit component.
    - [ ] Declare a handleFile function taking file as argument. The function sets the setFileObj to file and sets the setIsUploaded to true.
    - [ ] Declare a fileName variable set to fileObj.name.
    - [ ] Declare a handleSubmit function which takes event as argument and does event.preventDefault().
    - [ ] Declare a handleConversion function which takes the logic from: https://codesandbox.io/p/sandbox/test-upload-conversion-csv-4-cfd2zh?file=%2Fsrc%2FApp.js%3A48%2C1
    - [ ] The function returns, within a fragment, the Heading component, the Paragraph component and a form element.
    - [ ] The FileUploader component takes the handleFile as prop.
    - [ ] The form element takes handleSubmit as prop to the onSubmit attribute.
    - [ ] The InputTypeSubmit component takes "Submit" for the value attribute and !isUploaded for the disable attribute and handleConversion as prop for the Onlick attribute.

  - [ ] The Homepage function in index.js file returns the UploadData component.
