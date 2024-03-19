# Markers-properties

## Value proposition

As a user I want to set the properties of the markers (color, symbol, size) of my plot (if I chose "scatter-plot" or "line+markers-plot") to have a nice plot of my data.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/a78a70b0-d346-40bb-816f-58b2388b7b50)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/e1924bb9-db0b-4f5c-99a6-e90f82a7f7b6)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/a487dfb6-c933-4385-b363-b1376262990a)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/ce526e5c-8122-49e1-b427-2144be38c636)

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/13d0ae05-bce9-4b2d-b921-fc186df13bcb)

## Acceptance Criteria

- [ ] The component is displayed only if the user chose line+markers-plot or scatter-plot.
- [ ] Heading with text: "Marker properties".
- [ ] Paragraph with text "Marker color".
- [ ] The user can choose from a dropdown menu the color of the markers, options: red, blue, green, yellow, orange, pink, purple, maroon, black, grey.
- [ ] Paragraph with text "Marker symbol".
- [ ] The user can choose from a dropdown menu the symbol of the markers, options: filled circle, open circle, filled square, open square, filled diamond, open diamond, cross, x, filled triangle up, open triangle up, filled triangle down, open triangle down.
- [ ] Paragraph with text "Marker size".
- [ ] The user can choose from a dropdown menu the size of the markers, options: 6, 7, 8, 9, 10, 11.
- [ ] "Next" button.
- [ ] When the user clicks on the "Next" button, an alert message is displayed "You chose the marker properties.".
- [ ] The plot gets updated with the marker properties (only if the user chose line+markers-plot or scatter-plot).

## Tasks

- [ ] Create a new feature branch "Marker-properties".

- [ ] In the lib folder create a `listOfMarkerProperties.js` file.
  - [ ] Declare a `markerColorArray, a markerSymbolArray and a markerSizeArray` arrays.
  - [ ] `markerColorArray / markerSymbolArray / markerSizeArray` contain the options for the color, the symbol and the size.
  - [ ] Declare a `completedAllDropDownMenus` function to disable the "Next" button until the user has selected values in all dropdown menus.
- [ ] Create a `MarkerProperties` component.

  - [ ] useState for the `markerColor / markerSymbol / markerSize` variable with initial value set to "" / "" / 0.
  - [ ] Declare a `handleMarkerColorChange / handleMarkerSymbolChange / handleMarkerSizeChange` function which declares a choice variable set to event.target.value.
  - [ ] Declare a `completedAllDropDownMenus` function to disable the "Next" button until the user has selected values in all dropdown menus.
  - [ ] Declare a `handleMarkerProperties` function with an alert message.
  - [ ] Write a `handleSubmit function` which does event.preventDefault().
  - [ ] The function returns the `Heading` component and a form.
  - [ ] The form takes the `handleSubmit` function as prop to the `onSubmit` attribute.
  - [ ] Inside the form is nested the `Container` component, and inside of it, 3 instances of the `Paragraph` component, 3 instances of the `DropDownMenu` component and the `StyledInputTypeSubmit` component.
  - [ ] The `Container` component has the $centered attribute set to "center".
  - [ ] The first / second / third render of `DropDownMenu` has "Marker color" / "Marker symbol" / "Marker size" as prop to the `idString` attribute and the `handleMarkerColorChange / handleMarkerSymbolChange / handleMarkerSizeChange` function as prop to the `onChange` attribute and `markerColorArray / markerSymbolArray / markerSizeArray` as prop to the arrayOfOptions attribute.
  - [ ] The `StyleInputTypeSubmit` component has "Next" as value to the value attribute, the handleMarkerProperties function as value to the `onClick` attribute and and `completedAllDropDownMenus` function as value to the disable attribute.
  - [ ] Use conditional rendering in the return to display the output only if clickedChartType = "line+markers-plot" or if clickedChartType = "scatter-plot" and otherwise display null.

- [ ] In the index.js file, add the MarkerProperties component (before the Plotting component).

- [ ] In the Plotting component, access the markerColor, markerSymbol and markerSize variables.
  - [ ] If clickedChartType="line+markers-plot" or if clickedChartType="scatter-plot", declare as var a dataOptions variable like `dataOptions = {
  x: XVariable,
  y: YVariable,
  mode: selectedMode,
  type: selectedType,
  marker: {
    color: markerColor,
    symbol: markerSymbol,
    size: Number(markerSize),
  },
}`.
  - [ ] In the return of the function, add a conditional expression with ternary operator between : and null, like X ? Y : , where X is a copy of the conditional statement and Y is a copy of the Plot render.
  - [ ] In the second render of Plot replace the value of the data attribute by {[dataOptions]} and in the first conditional expression add markerColor.length > 0 as additional condition.
