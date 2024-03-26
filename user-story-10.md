# Bar properties

## Value proposition

As a user I want to
set the properties of the bars in the plot
so that I can update the visual display.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/b3e86fe9-8905-48cd-ac38-900f4c8a5e9a)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/2cbaaf6b-84f3-47d4-b3b9-d8362093ba0c)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/2f9fb7f1-f411-45b4-9951-f18a51abe660)

## Acceptance Criteria

- [ ] The component is displayed only if the user chose "bar-plot".
- [ ] Heading "Bar properties".
- [ ] Paragraph "Bar color".
- [ ] User can choose from a dropdown menu the color of the bars, options: red, blue, green, yellow, orange, pink, purple, maroon, black, grey.
- [ ] "Next" button which stays disabled until the user has selected a value from the dropdown menu.
- [ ] When the user clicks on the "Next" button, an alert message is displayed "You chose the bar properties.".
- [ ] Plot gets updated with the bar properties (only if the user has clicked "bar-plot").

## Tasks

- [ ] Create a new feature branch "Bar-properties".

- [ ] In the lib folder create a `listOfBarProperties.js` file.

  - [ ] Declare a `barColorArray` array which contains the options for the color.

- [ ] Create a `MarkerProperties` component.

  - [ ] Access titleLabel.
  - [ ] useState for the `barColor` variable with initial value set to "".
  - [ ] Declare a `handleBarColorChange` function which declares a choice variable set to event.target.value.
  - [ ] Declare a `completedBarProperties` function to disable the "Next" button until the user has selected a value in the dropdown menu.
  - [ ] Declare a `handleBarProperties` function with an alert message.
  - [ ] Write a `handleSubmit function` which does event.preventDefault().
  - [ ] The function returns the `Heading` component and a form.
  - [ ] The form takes the `handleSubmit` function as prop to the `onSubmit` attribute.
  - [ ] Inside the form is nested the `Container` component, and inside of it, the `Paragraph` component, the `DropDownMenu` component and the `StyledInputTypeSubmit` component.
  - [ ] The `Container` component has the $centered attribute set to "center".
  - [ ] `DropDownMenu` has "Bar color" as prop to the `idString` attribute and the `handleBarColorChange` function as prop to the `onChange` attribute and `barColorArray` as prop to the arrayOfOptions attribute.
  - [ ] The `StyleInputTypeSubmit` component has "Next" as value to the value attribute, the handleBarProperties function as value to the `onClick` attribute and `completedBarProperties()` function as value to the disabled attribute.
  - [ ] Use conditional rendering in the return to display the output only if titleLabel.length > 0 and if clickedChartType = "bar-plot".

- [ ] In the index.js file, add the BarProperties component (before the Plotting component).

- [ ] In the Plotting component, access the barColor variable.
  - [ ] If clickedChartType="bar-plot", declare as var a dataOptions variable like `dataOptions = {
  x: xVariable,
  y: yVariable,
  mode: selectedMode,
  type: selectedType,
  marker: {
    color: barColor,
  },
}`.
  - [ ] In the return of the function, add a conditional expression with ternary operator between : and null, like X ? Y : , where X is a copy of the conditional statement and Y is a copy of the Plot render.
  - [ ] In the first render of Plot replace the value of the data attribute by {[dataOptions]} and in the first conditional expression add barColor.length > 0 as additional condition.
