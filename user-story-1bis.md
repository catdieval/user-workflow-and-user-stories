## Title

## Value proposition

As a user
I want to upload my csv file with data inside
So that I can finally generate a plot.

## Description

- Title at the top with the name of the website
- Heading which explains the step one of the process
- Paragraph with note to explain that the file should be comma-delimited and have a period(.) for the decimal separator for numbers, that the file should have a header and what to do when there are missing values.
- A button with a text "Choose a file" which starts the upload process and the default text "no file chosen" is displayed next to the button
- Once the file is uploaded the filename is displayed
- A button with text "Submit" which is disabled by default and becomes enabled once the upload is successful
- The elements do not extend to each end of the page but are centered in the middle.

![wireframe Upload](/assets/plotdata-Step1.png)

## Acceptance criteria

- [ ] When the user clicks on the "Choose a file" button then an upload window opens where the user can select a file with a csv extension.
- [ ] When the user clicks on the "Submit" button the file will be converted to an array of objects.

## Tasks

- [ ] Create a new feature branch - upload-data.

### styles.js file

- [ ] Create a styles.js file.
- [ ] In this file make a named import of CreateGlobalStyle from "styled-components".
- [ ] Make a default export of createGlobalStyle, which you style as:
      \*,
      \*::before,
      \*::after {
      box-sizing: border-box;
      }

  body {
  display: grid;
  margin: auto;
  font-family: system-ui;
  place-items: center;
  min-height: 100vh;
  max-width: 50rem;
  }

### assets folder

- [ ] Create an asset folder and put inside the image for the logo of the website.

### Components folder and subfolders

- [ ] Create a Components folder

### Div component (centered)

- [ ] Create a Div component folder with an index.js file.
- [ ] In the index.js file export by default a Div function which returns a StyledDiv element.
- [ ] Import styled from "styled-components".
- [ ] The StyledDiv styles the div using styled with text-align set to center.

### Title component

- [ ] Create a Title component folder with an index.js file.
- [ ] In the index.js file export by default a Title function which returns the StyledDiv component and nested within an img element.
- [ ] In the index.js file import styled from "styled-components".
- [ ] Make a default import of Div from "/Div".
- [ ] Give to the img element a src attribute set to the path of the logo image.

### Layout component

- [ ] Create a Layout component folder with an index.js file.
- [ ] In the index.js file export by default a Layout function which returns Head & main elements and the Title component.
- [ ] Import the Title component by default from "../Title".
- [ ] Import Head by default from "next/head.js".
- [ ] The Layout function takes children as prop.
- [ ] Nest the children props within a main element.
- [ ] Nest a title element within the Head element. The title has for text "PlotData".

# \_app.js file

- [ ] In the \_app.js file import the Layout component from "../components/Layout".
- [ ] Import GlobalStyle by default from "../styles.js";
- [ ] Export by default an App function. It takes Component and pageProps as props.
- [ ] The App function returns the Layout component, and nested within the GlobalStyle component and the Component element.
- [ ] The Component element takes ...pageProps as prop.

### Button component

- [ ] Create a Button component folder with an index.js file.
- [ ] In the index.js file export by default a Button function which returns a StyledButton element.
- [ ] Import styled from "styled-components".
- [ ] The StyledButton styles the button using styled with a color set to deepskyblue.

### Heading component

- [ ] Create a Heading component folder with an index.js file.
- [ ] In the index.js file export by default a Heading function which returns a StyledH2 element.
- [ ] Import styled from "styled-components".
- [ ] The StyledH2 styles the h2 using styled with text-align set to center.

### Paragraph component

- [ ] Create a Paragraph component folder with an index.js file.
- [ ] In the index.js file export by default a Paragraph function which returns a StyledP element.
- [ ] Import styled from "styled-components".
- [ ] The StyledP styles the p using styled with text-align set to center.

### UploadData component

- [ ] Add a UploadData component folder and inside create an index.js file.
- [ ] In the index.js file export by default an UploadData function.
- [ ] Make a default import of Heading from "../Heading".
- [ ] Make a default import of Paragraph from "../Paragraph".
- [ ] Make a default import of Div from "../Div".
- [ ] The function returns, within a fragment, the Heading component, the Paragraph component, an input element and the Button component nested inside the Div component.
- [ ] The Heading component has for text "Step 1: Upload a CSV file to get the data.".
- [ ] The Paragraph component has for text notes about the header of the file, the delimiter in the file and missing values.
- [ ] implement the logic that handle the upload of a file
- [ ] import useState from react
- [ ]
- [ ]
