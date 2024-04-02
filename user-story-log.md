# Log Scale Properties

## Value description

As a user
I want to choose the scale for the x-and y-axis (linear or logarithmic)
So that I can improve the visualisation of my data if I have very large/very small numbers.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/0b5e493f-6efa-4225-91da-52af7bc77910)

## Acceptance Criteria

- [ ] Paragraph with text "Logarithmic scale for axes:". At the right of the paragraph is an "Info" button.
- [ ] When the user clicks on the "Info" button, a dialogue with a "x" button gets displayed. The dialogue has for text the text about log scale shown in the description.
- [ ] When the user clicks on the "x" button, the dialogue closes.
- [ ] User can decide to have a logarithmic scale separately for the x- and y-axis by using radio-buttons ("yes"/"no, use a linear scale").

## Tasks

- [ ] Create a feature branch "Log-scale-properties".
- [ ] Create a `DialogueBox` component:

  - [ ] Use the Material-Ui library: `npm install @mui/material @emotion/react @emotion/styled`.
  - [ ] Import the Dialog and DialogTitle components from the Material Ui library.
  - [ ] Declare a `useState` for `openDialog`.
  - [ ] Declare a `openDialogBox` function -> sets `setOpenDialog` function true.
  - [ ] Declare a `handleClose` function -> sets `setOpenDialog` function false.
  - [ ] Return: `button` (with onClick = openDialogBox), `Dialog` (with onClose = handleClose) and `DialogTitle` with the text described in the acceptance criteria/wireframe.

- [ ] Create a `LogScaleProperties` component:

  - [ ] Declare the `useState` and handle functions for: `logXAxis`, `logYAxis`, `handleLogXAxis` and `handleLogYAxis`.
  - [ ] Return: `Paragraph`,`DialogBox` and `Container`($direction = "row").
  - [ ] Inside Container are nested 2 instances of `Container` (one for x-axis grid and one for y-axis grid) ($direction="column").
  - [ ] Inside these instances of `Container` are nested `Paragraph` and 2 instances of `InputTypeRadio`.
  - [ ] For x-axis: the first / second instance of `InputTypeRadio` has handleLogXAxis as prop to the onClick attribute, "x-axis-log" as value to the labelString attribute and "yes" / "no, use a linear scale" as value to the idString attribute.
  - [ ] For y-axis: the first / second instance of `InputTypeRadio` has handleLogYAxis as prop to the onClick attribute, "y-axis-log" as value to the labelString attribute and "yes" / "no, use a linear scale" as value to the idString attribute.

- [ ] In the index.js, add the LogScaleProperties component to the return (before Plotting).
