# Layout Properties

## Value description

As a user I want to adjust the layout of my plot to have a clearly represented plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/d1ff2adb-9cfd-43b8-b4ee-70244bc20dfd)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/82be2238-277e-465a-9553-36ac85fa5025)

## Acceptance criteria

- [ ] Heading with text "Layout properties".
- [ ] Paragraph with text "Show grid (helper lines) for axes:".
- [ ] User can decide to have a grid separately for the x- and y-axis by using radio-buttons ("yes"/"no").
- [ ] Only when the user clicked yes on the radio buttons above:
  - [ ] Paragraph with text "Grid linestyle:".
  - [ ] User can choose from two dropdown-menus the grid linestyle for the x- and y-axis, options are: solid, dash, dot, longdash, dashdot.
- [ ] Paragraph with text "Range of values for axes:".
- [ ] User can set the range of values separately for the x- and y-axis from a list with radio-buttons ("yes, normal range"/"yes, reversed range"/"no, set minimum and maximum").
- [ ] Only when the user has chosen thie "no" option in the menu above:
  - [ ] Paragraph with text "Minimum and maximum values for ax(es)".
  - [ ] User can set the minimum and maximum values separately for the x- and y-axis: one input of type "number" for the minimum value, one input of type "number" for the maximum value.
- [ ] Paragraph with text "Logarithmic scale for axes:". At the right of the paragraph is an "Info" button.
  - [ ] When the user clicks on the "Info" button, a dialogue with a "x" button gets displayed. The dialogue has for text the text about log scale shown in the Acceptance Criteria.
  - [ ] When the user clicks on the "x" button, the dialogue closes.
- [ ] User can decide to have a logarithmic scale separately for the x- and y-axis by using radio-buttons ("yes"/"no, use a linear scale").
- [ ] "Next" button which stays disabled until the user has entered values in all the fields.
- [ ] The plot gets updated with the layout properties.

## Tasks

- [ ] Create a new feature branch "Layout-properties".

- [ ] Create a `LayoutProperties` component.
  - [ ] Write a `handleSubmit function` which does event.preventDefault().
  - [ ] Declare a `handleLayoutProperties` function with an alert message.
  - [ ] Declare a `completedLayoutProperties` function to disable the "Next" button until the user has selected values in all menus.
  - [ ] Returns: `Heading` and `form` element.
  - [ ] The form takes the `handleSubmit` function as prop to the `onSubmit` attribute.
  - [ ] Inside `form`: `GridProperties`, `RangeProperties`, `LogScaleProperties` and `StyledInputTypeSubmit`.
- [ ] The `StyleInputTypeSubmit` component has "Next" as value to the value attribute, the handleLayoutProperties function as value to the `onClick` attribute and `completedLayoutProperties()` function as value to the disabled attribute.

- [ ] In the index.js, add the `LayoutProperties` component to the return (before `Plotting`) and remove GridProperties, RangeProperties and LogScaleProperties from the return.

- [ ] In the `Plotting` component, access the `GridXAxis`, `GridYAxis`, `GridLineStyleXAxis`, `GridLineStyleYAxis`, `rangeXAxis`, `rangeYAxis`, `minXAxis`, `maxXAxis`, `minYAxis`, `maxYAxis`, `logXAxis` and `LogYAxis` variables.
  - [ ] Use these variables in the conditional rendering.
  - [ ] Use these variables in the `layout` attribute in the Plot component.
