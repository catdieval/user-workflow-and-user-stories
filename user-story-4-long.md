# Plotting

## Value Proposition

As a user I want to see the plot of my uploaded data.

## Description

## Acceptance Criteria

- [ ] Logo and Title at the top of page.
- [ ] Paragraph with text "You can interact with the graph by using the functions at the top of the graph.".
- [ ] Plot of the uploaded data.

## Tasks

- [ ] Create a new feature branch "Plotting".
- [ ] Install these libraries: npm install react-plotly.js plotly.js .
- [ ] Create a Plotting component and an index.js file inside.
  - [ ] Make a default import of Plot from "react-plotly.js".
  - [ ] Make a default import of Paragraph from "../Paragraph".
  - [ ] Make a default import of CenteredDiv from "../CenteredDiv".
  - [ ] Make a named import of chartArray from "../../lib/listOfPlotTypes.js".
  - [ ] Declare a Plot variable set to dynamic(() => import("react-plotly.js"), { ssr: false }) .
  - [ ] Retrieve clickedChartType from the local storage.
  - [ ] Retrieve XVariable and YVariable from the local storage.
  - [ ] Find which object in chartArray has the key "name" matching with the value of clickedChartType.
  - [ ] Declare a selectedMode variable and a selectedType variable and set their values to the values of the "mode" key and the "type" key found in the previous step.
  - [ ] The function returns, within a fragment, the Paragraph component and the CenteredDiv component.
  - [ ] Inside CenteredDiv is nested the Plot component.
  - [ ] The Paragraph has for text "You can interact with the graph by using the functions at the top of the graph.".
  - [ ] The Plot has the data attribute set to
        `{[
      {
        x: XVariable,
        y: YVariable,
        mode: selectedMode,
        type: selectedType,
      },
]}`.
  - [ ] The Plot has the layout attribute set to
        `{{
  xaxis: {
    showline: true,
    ticks: "outside",
  },
  yaxis: {
    showline: true,
    ticks: "outside",
  },
  width: 600,
  height: 500,
}}`.
  - [ ] The Plot has the config attribute set to
        `{{
       displayModeBar: true,
       modeBarButtonsToRemove: ["lasso2d", "select2d", "pan2d"],
}}`.
