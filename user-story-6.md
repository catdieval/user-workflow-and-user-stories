# Labels-to-axes

## Value Proposition

As a user I want to give labels to the x- und y-axis to have a descriptive plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148149765/ad24ee53-9dac-4ca3-acad-b6a86678b1a5)

## Acceptance Criteria

- [ ] Title with logo at the top of the page.
- [ ] Paragraph with text "Step 4: give labels to the axes".
- [ ] Paragraph with text "Label for the x-axis:"
- [ ] Input of type "text" where the user can enter the label for the x-axis. In the input is a placeholder text to guide the user.
- [ ] Paragraph with text "Label for the y-axis:"
- [ ] Input of type "text" where the user can enter the label for the y-axis. In the input is a placeholder text to guide the user.
- [ ] A "Submit" button to confirm what the user has written in the form. The button stays disabled until the user has entered a value for the y-axis label.

## Tasks

- [ ] Create a new feature branch "Labels-to-axis"

- [ ] Create an InputTypeText component:

  - [ ] The function has for argument the placeholderString prop, the onChange prop and the idString prop.
  - [ ] The function renders a label element and an input of type "text".
  - [ ] The label has the htmlFor attribute set to idString and has for text `${idString}:`.
  - [ ] The input has the placeholder attribute set to placeholderString as prop, has the onChange attribute set to onChange as prop and has the id attribute set to idString and the name attribute set to idString.

- [ ] Create a Axis - Component:
  - [ ] create two forms (input type text)
  - [ ] The XLabel variable and the YLabel variables are set to the text of the input for the x-axis and for the y-axis respectively.
  - [ ] Submit-Button :
    - [ ] handleAxisLabel function, which saves the text of the input fields to the local storage
    - [ ] use logical AND to disable button when there is YLabel value
- [ ] in the Plotting component set the xLabel and yLabel variables to the title key of the x-axis and the y-axis respectively, in the layout attribute of the Plot component, like
  - [ ] `title: {
    text: XLabel,
  },`
  - [ ] `title: {
    text: YLabel,
  },`.
- [ ] Add the Axis-Component to the index.js - file of the pages-folder.
