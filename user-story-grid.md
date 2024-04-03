# Grid Properties

## Value description

As a user
I want to have the possibility to choose to have a grid for the x-and y-axis and determine the line style of the grid.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/3895a9d1-0075-4420-b6d7-812ce3de1a65)

## Acceptance Criteria

- [ ] Paragraph with text "Show grid (helper lines) for axes:".
- [ ] User can decide to have a grid separately for the x- and y-axis by using radio-buttons ("yes"/"no").
- [ ] Only when the user clicked yes on at least one of the radio buttons above:
  - [ ] Paragraph with text "Grid linestyle:".
  - [ ] User can choose from two dropdown-menus the grid linestyle for the x- and y-axis (if applicable), options are: solid, dash, dot, longdash, dashdot.

## Tasks

- [ ] Create a new feature branch "Grid-properties".

- [ ] Create a component `InputTypeRadio`:

  - [ ] Function with props `idString`, `labelString`, `valueString`, `checked` and `onChange`.
  - [ ] Returns `label` and `input`.
  - [ ] label has idString as prop for text / htmlFor attribute.
  - [ ] input has the required / checked attribute, "radio" as value to the type attribute, onChange / labelString / valueString as prop to the onChange / name / value attribute and idString as prop to the id attribute.

- [ ] Create a component `GridProperties`:

  - [ ] Access `lineStyleArray` from the `listOfLineProperties.js` file in the `lib` folder.
  - [ ] Declare the `useState` and handle functions for:
    - `gridXAxis`,`gridYAxis`.
    - `handleGridXAxis`, `handleGridYAxis`.
    - `gridLineStyleXAxis`,`gridLineStyleYAxis`.
    - `handleGridLineStyleXAxis`,`handleGridLineStyleYAxis`.
  - [ ] Return: ` Paragraph`, `Container` ($direction = "row") and a conditional rendering.
  - [ ] Inside Container are nested 2 instances of `Container` (one for x-axis grid and one for y-axis grid) ($direction="column").
  - [ ] Inside these instances of `Container` are nested `Paragraph` and 2 instances of `InputTypeRadio`.
  - [ ] For x-axis: the first / second instance of `InputTypeRadio` has handleGridXAxis as prop to the onChange attribute, "x-axis-grid" as value to the labelString attribute, "yes" / "no" as value to the idString attribute and "true" / "false" as value to the valueString attribute.
  - [ ] For y-axis: the first / second instance of `InputTypeRadio` has handleGridYAxis as prop to the onChange attribute, "y-axis-grid" as value to the labelString attribute, "yes" / "no" as value to the idString attribute and "true" / "false" as value to the valueString attribute.
  - [ ] Conditional rendering: if the user clicked "yes" in at least one of the previous menus then render `Paragraph` and `Container` ($direction = "row").
  - [ ] Inside `Container` are nested 1 or 2 instances of `DropDownMenu` depending on if the user clicked "yes" for 1 or 2 axes.
  - [ ] Separately for x-axis and y-axis (if applicable): `DropDownMenu` has lineStyleArray as prop to the arrayOfOptions attribute.
  - [ ] For x-axis / y-axis (if applicable): `DropDownMenu` has handleGridLineStyleXAxis / handleGridLineStyleYAxis as prop to the onChange attribute, "x-axis:" / "y-axis:" as value to the idString attribute.

- [ ] In the index.js, add the GridProperties component to the return (before Plotting).
