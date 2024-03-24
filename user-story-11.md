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
- [ ] Paragraph with text "Logarithmic scale for axes:". At the right of the paragraph is an "Info" button where a click displays a dialogue with text "A logarithmic scale (or log scale) is a way of displaying numerical data over a very wide range of values in a compact way. As opposed to a linear scale in which every unit of distance corresponds to adding by the same amount, on a logarithmic scale, every unit of length corresponds to multiplying the previous value by the same amount." .
- [ ] User can decide to have a logarithmic scale separately for the x- and y-axis by using radio-buttons ("yes"/"no, use a linear scale").
- [ ] "Next" button which stays disabled until the user has entered values in all the fields.
- [ ] The plot gets updated with the layout properties.

## Tasks
