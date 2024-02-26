# Upload a CSV file and convert it to an array of objects

## Value proposition

As a user
I want to upload my csv file with data inside
So that I can finally generate a plot.

## Description

- Title at the top with the name of the website and a logo.
- Heading with text ""Step 1: Upload a CSV file to get the data.".
- Paragraph with text "Note: the file should have a
  header.
  Note: the file should be comma-delimited and the decimal
  separator for numbers should be a period (.).
  Note: if the file contains missing values, then replace
  these values in the file by null.".
- A button with a text "Choose a file" which starts the upload process and the default text "no file chosen" is displayed below the .
- Once the file is uploaded the filename gets displayed.
- A button with text "Submit" which is disabled by default and becomes enabled once the upload is successful.
- The elements do not extend to each end of the page but are centered in the middle.

![wireframe Upload](/assets/Wireframe-User-story-1bis.png)

## Acceptance criteria

- [ ] When the user clicks on the "Choose a file" button then an upload window opens where the user can select a file with a csv extension.
- [ ] When the user clicks on the "Submit" button then the content of the file gets converted to an array of objects and an alert gets displayed with the text "File processed successfuly".

## Tasks

- [ ] Create a new feature branch - upload-data.

### styles.js file

- [ ] In the properties of body inside the createGlobalStyle, add:
      display: grid;
      margin: auto;
      place-items: center;
      min-height: 100vh;
      max-width: 50rem;

### assets folder

- [ ] Create an asset folder and put inside the image for the logo of the website.
      ![Logo](/assets/Plotdata-Logo.png)

### Components folder and subfolders

- [ ] Create a Components folder

### CenteredDiv component

- [ ] Create a CenteredDiv component folder with an index.js file.
- [ ] In the index.js file export by default a CenteredDiv function which returns a StyledDiv element.
- [ ] Import styled from "styled-components".
- [ ] The StyledDiv styles the div element using styled with text-align set to center.

### Title component

- [ ] Create a Title component folder with an index.js file.
- [ ] In the index.js file export by default a Title function which returns the StyledDiv component and nested within an img element.
- [ ] In the index.js filemake a default import of styled from "styled-components".
- [ ] Make a default import of CenteredDiv from "/CenteredDiv".
- [ ] Give to the img element a src attribute set to the path of the logo image.

### Layout component

- [ ] Create a Layout component folder with an index.js file.
- [ ] In the index.js file export by default a Layout function which returns Head & main elements and the Title component.
- [ ] Import the Title component by default from "../Title".
- [ ] Import Head by default from "next/head.js".
- [ ] The Layout function takes children as prop.
- [ ] Nest the children props within the main element.
- [ ] Nest a title element within the Head element. The title has for text "PlotData".

### \_app.js file

- [ ] In the \_app.js file import the Layout component from "../components/Layout".
- [ ] The App function returns the Layout component, and nested within are the GlobalStyle component and the Component element.

### Button component

- [ ] Create a Button component folder with an index.js file.
- [ ] In the index.js file export by default a Button function which returns a StyledButton element.
- [ ] Make a default import of styled from "styled-components".
- [ ] The StyledButton styles the button using styled with background-color set to # 1f77b4, padding set to 10px, cursor set to pointer, font-size set to 16px, color set to white and font-weight set to bold.

### InputTypeSubmit component

- [ ] Create a InputTypeSubmit component with an index.js file.
- [ ] In the index.js file export by default a InputTypeSubmit function which returns a StyledInputTypeSubmit element.
- [ ] Make a default import of styled from "styled-components".
- [ ] The StyledInputTypeSubmit styles the input[type="submit"] element using styled with background-color set to # 1f77b4, padding set to 10px, cursor set to pointer, font-size set to 16px, color set to white and font-weight set to bold.

### Heading component

- [ ] Create a Heading component folder with an index.js file.
- [ ] In the index.js file export by default a Heading function which returns a StyledH2 element.
- [ ] Make a default import of styled from "styled-components".
- [ ] The StyledH2 styles the h2 element using styled with text-align set to center.

### Paragraph component

- [ ] Create a Paragraph component folder with an index.js file.
- [ ] In the index.js file export by default a Paragraph function which returns a StyledP element.
- [ ] Make a default import of styled from "styled-components".
- [ ] The StyledP styles the p element using styled with text-align set to center.

### FileUploader component

- [ ] Create a FileUploader component folder with an index.js file.
- [ ] In the index.js file use the logic from the FileUploader.js file in https://codesandbox.io/p/sandbox/test-upload-conversion-csv-4-cfd2zh?file=%2Fsrc%2FFileUploader.js%3A1%2C1.
- [ ] Remove the import "./styles.css";
- [ ] Make a default import of CenteredDiv from "../CenteredDiv".
- [ ] Make a default import of Button from "../Button".
- [ ] In the function return replace the div element by the CenteredDiv component.
- [ ] In the function return replace the button element by the Button component. Remove the className attribute.

### CorrectArrays component

- [ ] Create a CorrectArrays component folder with an index.js file.
- [ ] In the index.js file use the logic from the CorrectArrays.js file in https://codesandbox.io/p/sandbox/test-upload-conversion-csv-4-cfd2zh?file=%2Fsrc%2FCorrectArrays.js%3A5%2C1.

### UploadData component

- [ ] Install these libraries: convert-csv-to-array and convert-string-to-number.
- [ ] Add a UploadData component folder and inside create an index.js file.
- [ ] In the index.js file export by default an UploadData function.
- [ ] Make a default import of Heading from "../Heading".
- [ ] Make a default import of Paragraph from "../Paragraph".
- [ ] Make a default import of CenteredDiv from "../CenteredDiv".
- [ ] Make a default import of InputTypeSubmit from "../InputTypeSubmit".
- [ ] Make a named import of FileUploader from "../FileUploader".
- [ ] Make a default import of CorrectArrays from "../CorrectArrays".
- [ ] Make a named import of useState from "react".
- [ ] Make a default import of useLocalStorageState from "use-local-storage-state".
- [ ] Add const { convertCSVToArray } = require("convert-csv-to-array");
- [ ] Declare a state for the variable keynames using useLocalStorageState with a default value set to []. This will contain the names of the columns in the CSV file.
- [ ] Declare a state for the variable vals using useLocalStorageState with a default value set to []. This will contain the array of objects obtained from the conversion of the CSV file.
- [ ] Declare a state for the variable fileObj using useState with an initial value set to {}. This will contain the object representing the uploaded file.
- [ ] Declare a state for the variable isUploaded using useState with an initial value set to false. This variable will contain the status about the upload and will serve to enable or disable the InputTypeSubmit component.
- [ ] Declare a handleFile function taking file as argument. The function sets the setFileObj to file and sets the setIsUploaded to true.
- [ ] Declare a fileName variable set to fileObj.name.
- [ ] Declare a handleSubmit function which takes event as argument and does event.preventDefault().
- [ ] Declare a handleConversion function which does `
      const reader = new FileReader();

      reader.onload = function (e) {
        const arrayOfObjects = convertCSVToArray(e.target.result, {
          separator: ",",
        });

        // The output of the convertCSVToArray function needs further processing
        const [keys, ...correctValues] = CorrectArrays(arrayOfObjects);

        setKeynames(keys);
        setVals(correctValues);
        alert("File processed successfully");
      };

      reader.readAsText(fileObj);

  `

- [ ] The function returns, within a fragment, the Heading component, the Paragraph component and a form element.
- [ ] The Heading component has for text "Step 1: Upload a CSV file to get the data.".
- [ ] The Paragraph component has for text "Note: the file should have a header.
      Note: the file should be comma-delimited and the decimal
      separator for numbers should be a period (.).
      Note: if the file contains missing values, then replace
      these values in the file by null.".
- [ ] Inside the form element are nested the FileUploader component, a curly bracket with conditional rendering and the CenteredDiv component.
- [ ] The curly bracket contains `fileName ? <p>Uploaded file: {fileName}</p> : <p>No file chosen</p>` .
- [ ] The FileUploader component takes the handleFile as prop.
- [ ] The form element takes handleSubmit as prop to the onSubmit attribute.
- [ ] Inside the CenteredDiv component is nested the InputTypeSubmit component.
- [ ] The InputTypeSubmit component takes "Submit" for the value attribute and !isUploaded for the disable attribute and handleConversion as prop for the Onlick attribute.

### index.js file

- [ ] Import UploadData by default from "/Components/UploadData".
- [ ] The Homepage function returns the UploadData component.
