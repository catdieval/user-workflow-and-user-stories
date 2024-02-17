# Select a chart

## Value proposition

As a user
I want a see a list of possible chart types (e.g. line, scatter, bar),
so that I can click on the type I want.

## Description

- h1 heading with "PLOTDATA".
- h2 heading with "Step 1: Decide what type of chart.".
- List (without bullet points) of images corresponding to examples of each type of chart, with corresponding deepskyblue button named after the type of chart, displayed in a row with possibility of wrapping.
- The elements do not extend to each end of the page, but are centered in the middle.

## Acceptance criteria

- [ ] Clicking on a button saves the text of the button to a clickedChartType variable.
- [ ] Clicking on a button brings the user to the page with the data upload.

## Tasks

- [ ] Create a lib folder.

- [ ] Inside this folder create a listofcharttypes.js file.

- [ ] Go to listofcharttypes.js and declare an array chartarray containing objects with the keys "type", "mode" and "name".

  - The type key has for value a string corresponding to the name of the type of chart (e.g. "scatter", "bar").
  - The mode key has for value a string corresponding to the name of the type of plotting mode (e.g. "lines", "markers", "lines+markers").
  - The name key has for value a string corresponding to the name of the associated picture.

- [ ] Make a named export of chartarray.

- [ ] Create an asset folder that will contain the images for each type of chart, with filenames like "lines plot", "scatter plot", "lines+markers plot", "bar plot".

- [ ] In the pages folder, create a UploadDataPage.js file.

- [ ] Inside the Component folder create a ChartItem folder.

- [ ] Inside the ChartItem folder create a ChartItem.js file.

- Inside the pages folder go to the ListOfChartsPage.js file and make a default import to the ChartItem component from "../Component/ChartItem.js".

- [ ] Make a named import of StyledTitle from "../Components/Title/Title.styled".

- [ ] Make a named import of StyledHeading from "../Component/Heading/Heading.styled".

- [ ] Make a named import of chartarray from "../lib/listofcharttypes".

- [ ] Make a default import of styled from "styled-components".

- [ ] Declare a ListOfCharts function and export it by default.

- [ ] Inside the function write a StyledDiv component which styles a div element using styled, with the display set to flex, the flex-direction set to row, the flex-wrap set to wrap and the justify-content set to space-around.

- [ ] Inside the function write a StyledUl component which styles a ul element using styled, with the list-style-type set to none.

- [ ] The function returns a fragment, and nested within, the StyledTitle component, several line breaks, the StyledHeading component, several line breaks, the StyledDiv component, and nested within is the StyledUl component.

- [ ] StyledTitle has for text "PLOTDATA".

- [ ] StyledHeading has for text "Step 1: Decide what type of chart.".

- [ ] Nest curly brackets within the StyledUl, where you use forEach over chartarray to render a li element.

- [ ] Within the li, nest the ChartItem component.

- [ ] Give the key name as prop to ChartItem.

- [ ] Go to the ChartItem.js file, and inside make a named import of useRouter from "next/router".

- [ ] Make a default import of useLocalStorageState from "use-local-storage-state".

- [ ] Make a named import of StyledButton from "../Button/Button.styled".

- [ ] Declare a ChartItem function and export it by default.

- [ ] The function takes for argument the prop name.

- [ ] Inside the function use a local storage state for the clickedChartType variable, with "" as default value.

- [ ] Declare a constant router = useRouter().

- [ ] Write an handleClick function, taking event as argument.

- [ ] This function uses the setter setClickedChartType with the value event.target.value.

- [ ] This function calls an alert function with the text `You chose "${clickedChartType}"`.

- [ ] This function pushes using router to the UploadDataPage.js page.

- [ ] The ChartItem function returns, within a fragment, the StyledButton component and an img element.

- [ ] The img element takes an src attribute set to the path of the associated picture, using the name prop.

- [ ] The StyledButton of type "button" takes an onClick attribute which has handleClick as prop. The text of the button is the name prop.
