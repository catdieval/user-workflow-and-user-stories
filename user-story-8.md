# Line-properties

## Value proposition

As a user I want to set the properties (color, style and width) of my lines (if I have chosen a line plot or line + markers plot) in the plot to have a nice plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/d77268b3-e02e-4d25-bc43-8d1681bb63a0)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/957d484f-eeb1-4bb1-ac14-b42c57617869)

## Acceptance Criteria

- [ ] The component is displayed only if the user chose a line plot.
- [ ] Header with text "Line properties".
- [ ] Paragraph with text "Line color".
- [ ] The user can choose from a dropdown menu the color of the line, options: red/blue/green/yellow/orange/pink/purple/maroon/black/grey.
- [ ] Paragraph with text "Line style".
- [ ] The user can choose from a dropdown menu the linestyle, options: solid, dash, dot, long dash, dash dot.
- [ ] Paragraph with text "Line width (in pixels)".
- [ ] The user can choose from a dropdown menu the thickness of the line, options: 1, 2, 3, 4, 5.
- [ ] "Next" button.
- [ ] When the user clicks on the "Next" button, an alert message is displayed "You chose the line properties.".
- [ ] The plot gets updated with the line properties.

## Tasks

- [ ] Create a new feature branch "Line-properties".

- [ ] In the lib folder create a `listOfLineProperties.js` file.
  - [ ] Declare a `lineColorArray`, a `lineStyleArray` and a `lineWidthArray` arrays.
  - [ ] `lineColorArray` / `lineStyleArray` / `lineWidthArray` contain the color / style / width options.
- [ ] Create a `LineProperties` component.

  - [ ] useState for the `lineColor / lineStyle / lineWidth` variable with initial value set to "" / "" / 0.
  - [ ] Declare a `handleLineColorChange / handleLineStyleChange / handleLineWidthChange` function which declares a choice variable set to event.target.value.
  - [ ] Declare a `completedAllDropDownMenus` function to disable the "Next" button until the user has selected values in all dropdown menus.
  - [ ] Declare a `handleLineProperties` function with an alert message.
  - [ ] Write a `handleSubmit` function which does event.preventDefault().
  - [ ] The function returns the `Heading` component and a form.
  - [ ] The form takes the `handleSubmit` function as prop to the `onSubmit` attribute.
  - [ ] Inside the form is nested the `Container` component, and inside of it, 3 instances of the `Paragraph` component, 3 instances of the `DropDownMenu` component and the `StyledInputTypeSubmit` component.
  - [ ] The `Container` component has the $centered attribute set to "center".
  - [ ] The first / second / third render of `DropDownMenu` has "Line color" / "Line style" / "Line width" as prop to the `idString` attribute and the `handleLineColorChange / handleLineStyleChange / handleLineWithChange` function as prop to the `onChange` attribute and `lineColorArray / lineStyleArray / lineWidthArray` as prop to the `arrayOfOptions` attribute.
  - [ ] The `StyleInputTypeSubmit` component has "Next" as value to the value attribute, the `handleLineProperties` function as value to the `onClick` attribute and and `completedAllDropDownMenus()` as value to the disable attribute.

  - [ ] Use conditional rendering in the return to display the output only if `clickedChartType = "line-plot"` and otherwise display null.

- [ ] In the index.js file, add the `LineProperties` component (before the Plotting component).

- [ ] In the `Plotting` component, access the `lineColor, lineStyle and lineWidth` variables.
  - [ ] If `clickedChartType="line-plot"`, declare as var a dataOptions variable like `dataOptions = {
  x: XVariable,
  y: YVariable,
  mode: selectedMode,
  type: selectedType,
  line: {
    color: lineColor,
    dash: lineStyle,
    width: Number(lineWidth),
  },
}`.
  - [ ] In the return of the function, add a conditional expression with ternary operator between : and null, like X ? Y : , where X is a copy of the conditional statement and Y is a copy of the Plot render.
  - [ ] In the first render of Plot replace the value of the data attribute by {[dataOptions]} and in the first conditional expression add `lineStyle.length > 0` as additional condition.
