## Title

## Value proposition

As a user
I want to upload my csv file with data inside
So that I can finally generate a plot.

## Description

- Title at the top with the name of the website
- Heading which explains the step one - "Upload"
- paragraph with note to explain that the file should be comma-delimited and have a period(.) for the decimal separator for numbers, what to do when there are missing values and that the file should have a header.
- a button with a text "Choose a file" which started the upload process and the default text "no file chosen" is displayed next to the button
- once the file is uploaded the filename is displayed
- a button with text "Submit" which is disabled by default and becomes enabled once the upload is successful

![wireframe Upload](/assets/)

## Acceptance criteria

- [ ] When the user clicks on the upload button then an upload window opens where the user can select a file with a csv extension.
- [ ] when the user clicks on the "Submit" button the file will be converted to an array of objects

## Tasks

- [ ] create a new feature branch - upload-data
- [ ] create a Components folder
- [ ] create a Title component with index.js file which returns h1 Heading with the Text "Plotdata"
- [ ] import styled from styled-components and style the heading with text-align set to center
- [ ] create Layout component to return Head & Main elements and the Title component.
- [ ] render Layout component to \_app.js
- [ ]
- [ ] create a Button component with an index.js file which returns a button element
- [ ] import styled from "styled-components" and style the button with a color set to "deepskyblue"
- [ ] add Component UploadData and inside create an index.js file
- [ ] the Component returns an input element and the Button component which are nested in a styled div element
- [ ] implement the logic that handle the upload of a file
- [ ] import useState from react
- [ ]
- [ ]
