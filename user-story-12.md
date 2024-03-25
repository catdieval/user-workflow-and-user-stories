# Plotting properties

## Value proposition

As a user I want to make preferences for the style and the layout of my plot to have a nice plot

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/e78b1071-2e83-420e-a9e9-d3e929e7c060)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/f29bb295-2ec7-4a59-bb61-c0b375e1b41c)

## Acceptance criteria

- [ ] Title with logo at the top pf the page.
- [ ] Paragraph: "Step 6: Assign properties to the graph".
- [ ] If the user clicked **line-plot**, then the LineProperties component is displayed.
- [ ] If the user clicked **scatter-plot** or **line-markers-plot**, then the MarkerProperties component is displayed.
- [ ] If the user clicked **bar-plot**, then the BarProperties component is displayed.
- [ ] LayoutProperties component.
- [ ] The plot gets updated with the layout properties and with the relevant category of graph properties.

## Tasks

- [ ] Create a new feature branch "Plotting-properties".

- [ ] Create a PlottingProperties Component:

  - [ ] It returns the Heading component and the LayoutProperties component.
  - [ ] The Heading takes "Step 6: Assign properties to the graph" for text.
  - [ ] Between Heading and LayoutProperties, add a conditional rendering for a component: if clickedChartType = "line-plot" / "bar-plot" / "scatter-plot" or "line-markers-plot", then render LineProperties / BarProperties / MarkerProperties.

- [ ] In the index.js, add the PlottingProperties component (before Plotting) and remove MarkerProperties, BarProperties, LineProperties and LayoutProperties from the return.
