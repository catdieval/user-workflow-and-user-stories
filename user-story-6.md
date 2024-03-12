# Labels-to-axes

## Value Proposition

As a user I want to give labels to the x- und y-axis to have a descriptive plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148149765/ad24ee53-9dac-4ca3-acad-b6a86678b1a5)

## Acceptance Criteria

- [ ] Title with logo at the top of the page.
- [ ] Paragraph with text "Step 4: give labels to the axes".
- [ ] Paragraph with text "For the x variable you chose:" + xKey value (reminder).
- [ ] Paragraph with text "For the y variable you chose:" + yKey value (reminder).
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
- [ ] Create a XLabelYLabelGraph component.

  - [ ] Access the xKey and the yKey variables.
  - [ ] useState for the hasEnteredYLabel variable with initial value set to false.
  - [ ] useLocalStorageState for the xLabel variable with default value set to "".
  - [ ] useLocalStorageState for the yLabel variable with default value set to "".
  - [ ] Declare a handleSubmit function which does event.preventDefault() .
  - [ ] Declare a handleXLabelChange function which sets setXLabel to event.target.value.
  - [ ] Declare a handleYLabelChange function which sets setYLabel to event.target.value and sets setHasEnteredYLabel to true.
  - [ ] Declare a handleAxesLabels function which sends an alert with the text set to "Labels for the x-axis and the y-axis of the graph are assigned".
  - [ ] The component renders 2 instances of Paragraph and a form.
  - [ ] Inside the form are nested two instances of the InputTypeText component and the StyledInputTypeSubmit component.
  - [ ] The form takes the handleSubmit function as prop to the onSubmit attribute.
  - [ ] The first InputTypeText takes "Fill me with name and unit, e.g. Age (years)" as prop to the placeholderString attribute and the handleXLabelChange function as prop to the onChange attribute and "x-axis" as prop to the idString attribute.
  - [ ] The second InputTypeText takes "Fill me with name and unit, e.g. Height (inches)" as prop to the placeholderString attribute and the handleYLabelChange function as prop to the onChange attribute and "y-axis" as prop to the idString attribute.
  - [ ] The StyleInputTypeSubmit component has "submit" as value to the type attribute, "Next" as value to the value attribute, the handleAxesLabels function as value to the onClick attribute and !ihasEnteredYLabel as value to the disable attribute.

- [ ] In the Plotting Component, access xLabel and yLabel.
  - [ ] Use xLabel != "" and yLabel !="" as additional conditions for the rendering of the Plot component.
  - [ ] Set xLabel as value to the title key of the x-axis in the Layout attribute of the Plot component.
  - [ ] Set yLabel as value to the title key of the y-axis in the Layout attribute of the Plot component.
- [ ] Add the XLabelYLabelGraph component to the index.js file (after the ListOfCharts component).

%%%%%%%

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
