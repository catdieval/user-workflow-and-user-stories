# Range Properties

## Value description

As a user
I want to adjust the range of the x-and y-axis
So that I can have a detailed look of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148491107/dfaf868e-16ac-4c41-be83-14c79400b765)

## Acceptance Criteria

- [ ] Paragraph with text "Range of values for axes:".
- [ ] User can set the range of values separately for the x- and y-axis from a list with radio-buttons ("yes, normal range"/"yes, reversed range"/"no, set minimum and maximum").
- [ ] Only when the user has chosen the "no" option in the menu above:
  - [ ]  Paragraph with text "Minimum and maximum values for ax(es)".
  - [ ] User can set the minimum and maximum values separately for the x- and y-axis: one input of type "number" for the minimum value, one input of type "number" for the maximum value.

## Tasks

- [ ] Create a feature branch "Range-properties".

- [ ] Create a ` InputTypeNumber` component:

  - [ ] Function with props `idString`, `placeholderString`, `onChange`.
  - [ ] Returns `label` and `input` elements.
  - [ ] label has idString as prop for the text / htmlFor attribute.
  - [ ] input has the required attribute, "number" as value to the type attribute, idString as prop to the id / name attribute, onChange / placeholderString as prop to the onChange / placeholder attribute.

- [ ] Create a `RangeProperties` component:

  - [ ] Declare the `useState` and handle functions for:

    - `rangeXAxis` , `rangeYAxis`.
    - `handleRangeXAxis` , `handleRangeYAxis`.
    - `minXAxis`, `minYAxis`,`maxXAxis`, `maxYAxis`.
    - `handleMinXAxis`, `handleMaxXAxis`, `handleMinYAxis`, `handleMaxYAxis`.

  - [ ] Return: `Paragraph`,`Container` ($direction = "row") and a conditional rendering.
    - [ ] Inside Container are nested 2 instances of `Container` (one for x-axis range and one for y-axis range) ($direction="column").
    - [ ] Inside these instances of `Container` are nested `Paragraph` and 3 instances of `InputTypeRadio`.
    - [ ] For x-axis: the first / second / third instance of `InputTypeRadio` has handleRangeXAxis as prop to the onClick attribute, "x-axis-range" as value to the labelString attribute and "yes, normal range" / "yes, reversed range" / "no, set minimum and maximum" as value to the idString attribute.
    - [ ] For y-axis: the first / second / third instance of `InputTypeRadio` has handleRangeYAxis as prop to the onClick attribute, "y-axis-range" as value to the labelString attribute and "yes, normal range" / "yes, reversed range" / "no, set minimum and maximum" as value to the idString attribute.
    - [ ] Conditional rendering: if the user clicked "no, set minimum and maximum" in at least one of the previous menus then render `Paragraph` and `Container` ($direction = "row").
    - [ ] Inside `Container` are nested 1 or 2 instances of `Container`($direction="column") depending on if the user clicked "no, set minimum and maximum" for 1 or 2 axes.
    - [ ] Inside these instances of `Container` are further nested `Paragraph` and 2 instances of `InputTypeNumber`.
    - [ ] Separately for x-axis and y-axis (if applicable): the first / second render of `InputTypeNumber` has "Minimum value:" / "Maximum value:" as value to the idString attribute and "Fill me with number, e.g. 1, -1, 1.5" as value to the placeholderString attribute.
    - [ ] For x-axis (if applicable): the first / second render of `InputTypeNumber` has handleMinXAxis / handleMaxXAxis as prop to the onChange attribute.
    - [ ] For y-axis (if applicable): the first / second render of `InputTypeNumber` has handleMinYAxis / handleMaxYAxis as prop to the onChange attribute.

- [ ] In the index.js, add the RangeProperties component to the return (before Plotting).
