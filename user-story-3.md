## Value Proposition

As a user I want to select which variable is plotted on the x- and y-axis
to finally generate a nice plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148149765/0ee23bbe-bc88-4f3f-8ba6-cc55d0b68435)

## Acceptance Criteria

- [ ] Title at the top with the name of the website and a logo.
- [ ] Heading with text "Step 3: Choose the variables you want to plot".
- [ ] Paragraph with text "Variable for the x-axis:".
- [ ] Dropdown menu for the x-axis.
- [ ] Paragraph with text "Variable for the y-axis:".
- [ ] Dropdown menu for the y-axis.
- [ ] A "Submit" button that submits the selected options for x- and y-axes and stays disabled until the user has made a choice in both dropdown menus.
- [ ] When the user clicks on the "Submit" button then the values for the x and y variables get assigned.

## Tasks

- [ ] Create a feature branch "Choose-variables".

- [ ] Create a DropDownMenu component.

  - [ ] It takes as props: idString and onChange.
  - [ ] Retrieve the keynames array from the local storage.
  - [ ] The function returns, within a fragment, a menu of options (label, select and option elements).
  - [ ] The select element takes the required attribute and takes onChange as prop to the onChange attribute.
  - [ ] Write an option element with "Select" as text and "" for the value attribute.
  - [ ] Inside curly braces map over the keynames array to render an option element.
  - [ ] The option element has both for the text and for the value attribute the string in keynames.
  - [ ] The label element has both for the text and for the htmlFor attribute the idString prop.
  - [ ] The select element has both for the name attribute and for the id attribute the idString prop.

- [ ] Create a ChooseVariables component
  - [ ] useLocalStorageState for the XVariable variable with default value set to [].
  - [ ] useLocalStorageState for the YVariable variable with default value set to [].
  - [ ] useLocalStorageState for the XKey variable with default value set to "".
  - [ ] useLocalStorageState for the YKey variable with default value set to "".
  - [ ] useState for the hasChosenLastVariable variable with initial value set to false.
  - [ ] Write a handleSubmit function which does event.preventDefault().
  - [ ] Write a handleXChange function which declares a choice variable set to event.target.value and if choice is different from "" (if the user selects another option than Select) then sets setXKey to choice.
  - [ ] Write a handleYChange function which declares a choice variable set to event.target.value and if choice is different from "" (if the user selects another option than Select) then sets setYKey to choice and sets setHasChosenLastVariable to true.
  - [ ] Write a handleAssignVariables function which retrieves the vals array from the local storage and declares a tempXArray variable and a tempYArray variable. These variables are arrays with the number of columns equal to the number of objects in vals.
    - [ ] In tempXArray fill in with the values associated to the key in vals corresponding to the XKey value.
    - [ ] In tempYArray fill in with the values associated to the key in vals corresponding to the YKey value.
    - [ ] Set setXvariable to tempXArray and set setYVariable to tempYArray.
    - [ ] Use an alert message with text "Data for the x and y variables are assigned.".
  - [ ] if xKey !=="" && xKey==yKey then use an alert message with the text "Are you sure you want to use the same variable for x as y? It would give a meaningless plot."
  - [ ] ChooseVariables returns, within a fragment, the Heading component and a form element.
  - [ ] The Heading takes "Step 3: choose the variables you want to plot." for text.
  - [ ] The form element contains the CenteredDiv component and inside of it are nested one time the Paragraph component and the DropDownMenu component (for the x axis), then again these 2 components (for the y-axis) and the StyledInputTypeSubmit component.
  - [ ] The form takes the handleSubmit function as prop to the onSubmit attribute.
  - [ ] The first render of Paragraph has for text "Variable for the x-axis:".
  - [ ] The second render of Paragraph has for text "Variable for the y-axis:".
  - [ ] The first render of DropDownMenu takes "x" as prop to the idString attribute and the handleXChange function as prop to the onChange attribute.
  - [ ] The second render of DropDownMenu takes "y" as prop to the idString attribute and the handleYChange function as prop to the onChange attribute.
  - [ ] The StyledInputTypeSubmit takes "Submit" as value and !hasChosenLastVariable as prop for the disabled attribute and the handleAssignVariables as prop to the onClick attribute.
