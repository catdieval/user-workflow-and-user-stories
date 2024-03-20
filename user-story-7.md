# Graph-Title

## Value proposition

As a user I want to give a title to the graph to better understand what the plot is about.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148149765/ffc1cb5c-7ffa-4447-ae08-519a0d382bfb)

## Acceptance Criteria

- [ ] Title with logo at the top of the page.
- [ ] A paragraph with text "Label for the x-axis:".
- [ ] A paragraph with the value entered by the user for the x label.
- [ ] A paragraph with text "Label for the y-axis:".
- [ ] A paragraph with the value entered by the user for the y label.
- [ ] A paragraph with text "Title:".
- [ ] An input of type "text" where the user can enter the title of the graph. The input has a placeholder text to guide the user.
- [ ] A "Submit" button to confirm what the user entered in the form. The button stays disabled until the user has entered a value for the title.

## Tasks

- [ ] Create a feature branch "Graph-title".

- [ ] Create a GraphTitle component and an index.js file inside.

  - [ ] Retrieve the xLabel and yLabel variables from local storage.
  - [ ] useState for the titleLabel variable with initial value set to "".
  - [ ] Declare a handleSubmit function which does event.preventDefault() .
  - [ ] Declare a handleTitleChange function which sets setTitleLabel to event.target.value and sets setHasEnteredTitle to true.
  - [ ] Declare a handleTitle function which sends an alert with the text set to "Title of the graph is assigned".
  - [ ] Write a completedTitle function to disable the "Next" button until the user has entered a value for the title.
  - [ ] The component renders 4 instances of Paragraph and a form.
  - [ ] Inside the form is nested the Container component, and inside of it are nested the InputTypeText component and the StyledInputTypeSubmit component.
  - [ ] The Container component has the $centered attribute set to "center".
  - [ ] The form takes the handleSubmit function as prop to the onSubmit attribute.
  - [ ] The first Paragraph has for text "Label for the x-axis:".
  - [ ] The second Paragraph has for text xLabel.
  - [ ] The third Paragraph has for text "Label for the y-axis:".
  - [ ] The fourth Paragraph has for text yLabel.
  - [ ] The InputTypeText takes "Fill me with title" as prop to the placeholderString attribute and the handleTitleChange function as prop to the onChange attribute and "Title" as prop to the idString attribute.
  - [ ] The StyleInputTypeSubmit component has "submit" as value to the type attribute, "Next" as value to the value attribute, the handleTitle function as value to the onClick attribute and completedTitle() as value to the disabled attribute.

- [ ] In the Plotting Component, access titleLabel.
  - [ ] Use titleLabel != "" as additional condition for the rendering of the Plot component.
  - [ ] Set titleLabel as value to the title key in the layout attribute of the Plot component, like
        `title: {
  text: titleLabel,
},`
- [ ] Add the GraphTitle component to the index.js file (before the Plotting component).
