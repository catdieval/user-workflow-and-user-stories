## Title

## Value proposition

As a user
I want to upload my csv file with data inside
So that I can finally generate a plot.

## Description

- Title at the top with the name of the website
- Heading which explains the step one - "Upload"
- a button with a text "Upload" which started the upload process
- once the file is uploaded the filename is displayed with delete button on the side
- paragraph with note to explain what to do when there are missing values
- a button with a text "Approve this file" appears after successful upload

![wireframe Upload](/assets/plotdata-wireframe%20-1.png)

## Acceptance criteria

- [ ] When the user clicks on the upload button then an upload window opens where the user can select a file with a csv extension
- [ ] when the user wants to delete the uploaded file, the filename disappears from the screen and the upload button is displayed again
- [ ] when the user clicks on the "Approve this file" the file will be converted to an array of objects

## Tasks

- [ ] create a new feature branch - upload-data
- [ ] create a Components folder
- [ ] create a Title Component with index.js file which returns h1 Heading with the Text "Plotdata"
- [ ] import styled from styled-components and style the heading with text-align set to center
- [ ] create LayoutComponent to return Head & Main elements and the TitleComponent.
- [ ] render LayoutComponent to \_app.js
- [ ] create a ButtonComponent which returns a button element
- [ ]
- [ ] add Component UploadData and inside create an index.js file
- [ ] the Component returns an input element which wrap the ButtonComponent
- [ ] implement the logic that handle the upload of a file
- [ ] create a PreviewDeleteButton Component to return a <div> with list of the uploaded file, a button to remove the uploaded file and a <p> element with an info text
- [ ] implement logic for the delete function
- [ ] import useState from react
- [ ] create a boolean isUploaded to toggle between UploadData & PreviewDeleteButton components
- [ ] create a Navigation to render the Next button???
- [ ]
