# Select type of plot

## Value proposition

As a user
I want to select a type of chart
So that I can finally generate a plot.

## Description

- Start with the component for Step 1 UploadData, where we add a "Next" button.
- The "Next" button is disabled until the user clicks on the "Submit" button.
- Clicking on the "Next" button causes a rendering of the ListOfChartTypes component (component for step 2, which is created in this user story).
- Title at the top with the name of the website and a logo.
- Heading with text "Step 2: Decide what type of graph.".
- List (without bullet points) of images corresponding to examples of each type of chart, with corresponding button named after the type of chart.
- The elements do not extend to each end of the page, but are centered in the middle.

## Acceptance criteria

- [ ] Clicking on the "Submit" button enables the "Next" button.
- [ ] Clicking on the "Next" button causes a rendering of the ListOfChartTypes component.
- [ ] Clicking on the button for a chart type shows an alert message to inform the user which type of chart was selected.

## Tasks

### Creation of chart-types folder in the assets folder and icon images

- [ ] Inside the assets folder create a chart-types folder.
- [ ] Search on the Internet for icon images for each type of chart and add them to the chart-types folder. Rename the images like so: "lines plot", "scatter plot", "lines+markers plot", "bar plot".

### Creation of a lib folder and a listofcharttypes.js file inside

- [ ] Create a lib folder and inside create a listofcharttypes.js file.
- [ ] Inside this file declare an array chartarray and export it by default.
- [ ] chartarray contains objects with the keys "type", "mode" and "name".
  - The type key has for value a string corresponding to the name of the type of chart (e.g. "scatter", "bar").
  - The mode key has for value a string corresponding to the name of the type of plotting mode (e.g. "lines", "markers", "lines+markers").
  - The name key has for value a string corresponding to the name of the associated picture contained in the chart-types folder.

### FlexDiv component

- [ ] Create a FlexDiv component folder with an index.js file.
- [ ] In the index.js file export by default a FlexDiv function which returns a StyledDiv element.
- [ ] Import styled from "styled-components".
- [ ] The StyledDiv styles the div element using styled, with display set to flex, flex-direction set to row, flex-wrap set to wrap and justify-content set to space-around.

### Img component

- [ ] Create a Img component folder with an index.js file.
- [ ] In the index.js file export by default a Img function which returns a StyledImg element.
- [ ] Import styled from "styled-components".
- [ ] The StyledImg styles the img element using styled, with flex-shrink set to 1

### ChartItem component

- [ ] Inside the Components folder create a ChartItem component folder and inside create a index.js file.
- [ ] In the index.js file make a default import of useLocalStorageState from "use-local-storage-state".
- [ ] Make a default import of Button from "../Button".
- [ ] Make a default import of Img from "../Img".
- [ ] Declare a ChartItem function and export it by default.
- [ ] The function takes for argument the prop name.
- [ ] Declare a local storage state for the clickedChartType variable, with "" as default value.
- [ ] Write an handleClick function, taking event as argument.
- [ ] This function uses the setter setClickedChartType with the value event.target.value.
- [ ] This function calls an alert function with the text `You chose "${clickedChartType}"`.
- [ ] The ChartItem function returns, within a fragment, the Button component and the Img component.
- [ ] Img takes an src attribute set to the path of the associated picture, using the name prop.
- [ ] The Button of type "button" takes an onClick attribute which has handleClick as prop. The text of the button is the name prop.

### ListOfCharts component

- Create a ListOfCharts component folder and inside create an index.js file.
- [ ] In the index.js file make a named import of useState from "react".
- [ ] Make a default import of ChartItem from "../ChartItem".
- [ ] Make a named import of Heading from "../Heading".
- [ ] Make a named import of FlexDiv from "../FlexDiv".
- [ ] Make a named import of chartarray from "../lib/listofcharttypes.js".
- [ ] Declare a ListOfCharts function and export it by default.
- [ ] The function returns a fragment, and nested within, the Heading component and the FlexDiv component.
- [ ] Heading has for text "Step 2: Decide what type of chart.".
- [ ] Nest curly brackets within the FlexDiv, where you use map over chartarray to render the ChartItem component.
- [ ] Give the key name as prop to ChartItem.

### \_app.js file

- [ ] Make a named import of useState from "react".
- [ ] In the App function declare a state for the variable hasCompletedStep1 using useState with an initial value set to false.
- [ ] Pass the hasCompletedStep1 and the setHasCompletedStep1 as props to Component.

### index.js file

- [ ] Pass hasCompletedStep1 and setHasCompletedStep1 as props to the Homepage function.
- [ ] In the return, conditionally render the UploadData component if hasCompletedStep1 is false, and render the ListOfChartTypes component otherwise.
- [ ] Pass setHasCompletedStep1 as prop to the setHasCompletedStep1 attribute in the UploadData component.

### UploadData component

- [ ] In the index.js file make a default import of Button from "../Button".
- [ ] Pass the setHasCompletedStep1 as prop to the UploadData function.
- [ ] Declare a state for the hasConvertedFile variable using useState with an initial value set to false.
- [ ] In the handleConversion function set hasConvertedFile to true.
- [ ] Declare a handleClick function which sets setHasCompletedStep1 to true.
- [ ] In the function return add the Button component after the form element.
- [ ] The Button component has for text "Next" and takes the handleClick as prop to the onClick attribute and takes !hasConvertedFile for the disabled attribute.
