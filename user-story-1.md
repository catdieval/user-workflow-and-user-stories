# Select a chart

## Value proposition

As a user
I want a see a list of possible chart types (e.g. line, scatter, bar),
so that I can click on the type I want.

## Description

- h1 header with "PLOTDATA".
- h2 header with "Step 1: Decide what type of chart.".
- List (without bullet points) of images corresponding to examples of each type of chart, with corresponding button named after the type of chart, displayed in a row with possibility of wrapping.

## Acceptance criteria

- [ ] Clicking on a button brings the user to the page with the data upload.

## Tasks

- [ ] In the "pages" folder, create an empty "UploadDataPage.js" file.

- [ ] Create a component folder and inside create a ChartItem.js file.

- [ ] Create an asset folder that will contain the images for each type of chart, with filenames like "line-plot", "scatter-plot".

- Go to the "ListOfChartsPage.js" file and make a default import to the ChartItem component.

- [ ] Make a default import of "styled" from "styled-components".

- [ ] Declare a ListOfCharts function and export it by default.

- [ ] Inside the function declare an array chartarray containing objects with the keys "name" and "image". The "name" key has for value a string corresponding to the name of each type of graph (e.g. "line-plot", "scatter-plot"). The "image" key has for value a string corresponding to the path to the associated picture.

- [ ] Write a StyledDiv component which styles a div element using styled, with the display set to "flex", the flex-direction set to "row", the flex-wrap set to "wrap" and the justify-content set to "space-around".

- [ ] Write a StyledUl component which styles a ul element using styled, with the list-style-type set to "none".

- [ ] The function returns a fragment, and nested within, a h1 heading, several line breaks, a h2 heading, several line breaks, the StyledDiv component, and nested within is the StyledUl component.

- [ ] The h1 has for text "PLOTDATA".

- [ ] The h2 has for text "Step 1: Decide what type of chart.".

- [ ] Nest curly brackets within the StyledUl, where you use forEach over the chartarray to render a li element.

- [ ] Within the li, nest the ChartItem component.

- [ ] Give the keys "name" and "image" as props to ChartItem.

- [ ] Go to the ChartItem.js file, and inside make a named import of useRouter from "next/router".

- [ ] Declare a "ChartItem" function and export it by default.

- [ ] The function takes for arguments the "name" prop and the "image" prop.

- [ ] Inside the function declare a constant router = useRouter().

- [ ] Write an handleClick function, which pushes using router to the "UploadDataPage.js" page.

- [ ] The ChartItem function returns, within a fragment, a button element and an img element.

- [ ] The img element takes an src attribute set to the "image" prop.

- [ ] The button takes an onClick attribute which has handleClick as prop. The text of the button is the "name" prop.
