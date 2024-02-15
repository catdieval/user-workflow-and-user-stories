# Homepage

## Value proposition

As a user
I want to see a homepage with an introduction to the website, and a "Get Started" button so that I can go start the plotting process on the next page.

## Description

- h1 header with name of website.
- Paragraph to introduce the concept of the website.
- h2 header to announce a list of the steps for the plotting process.
- Unordered list containing these steps.
- Paragraph to announce that a chart is generated.
- Unordered list of possible actions once a chart is generated.
- A deepskyblue button with the text "Get started".
- The elements do not extend to each end of the page, but are centered in the middle.

## Acceptance criteria

- [ ] A click on the button brings the user to the page with the list of chart types.

## Tasks

- [ ] Create a styles.js file.

- [ ] Go to styles.js and make a named import of "createGlobalStyle" from "styled-components".

- [ ] Make a default export of createGlobalStyle, where you write the following styling properties:
      _,
      _::before,
      \*::after {
      box-sizing: border-box;
      }

  body {
  display: grid;
  margin: auto;
  font-family: system-ui;
  place-items: center;
  min-height: 100vh;
  max-width: 50rem;
  }

- [ ] Create a "pages" folder.

- [ ] Inside this folder create a index.js file.

- [ ] Inside this folder create a "ListOfChartsPage.js" file.

- [ ] Inside this folder create a \_app.js file.

-[ ] Go to the \_app.js file and make a default import of createGlobalStyle from "../styles".

- [ ] Declare a function "App" and export it by default.

- [ ] The function returns, nested within a fragment, the createGlobalStyle component.

- [ ] Create a "Component" folder.

- [ ] In this folder create a Button folder.

- [ ] In the Button folder create a Button.styled.js file.

- [ ] Go to Button.Styled.js and make a default import of "styled" from "styled-components".

- [ ] Write a StyledButton component which styles a button element using styled, with background-color set to "deepskyblue".

- Make a named export of StyledButton.

- [ ] In the "pages" folder go to index.js, and make a named import of useRouter from "next/router".

- [ ] Make a named import of StyledButton from "../Component/Button/Button.styled".

- [ ] Declare a "Homepage" function and export it by default.

- [ ] Inside the function declare a constant router = useRouter();

- [ ] Write an handleClick function, which pushes using router to the "ListOfChartsPage.js" page.

- [ ] The function returns, nested in a fragment, a h1 heading, several line breaks, a paragraph, several line breaks, a h2 heading, an unordered list, a paragraph, an unordered list, several line breaks and finally the StyledButton component.

- [ ] The h1 has for text "PLOTDATA".

- [ ] The first p has for text "With PLOTDATA you can use data to easily make customizable publication-quality charts, all without programming.".

- [ ] The h2 has for text "Overview of the different steps".

- [ ] The first ul has li elements nested with the following text:

  - Step 1: Decide what type of graph.
  - Step 2: Upload a CSV file to get the data.
  - Step 3: Choose from the columns in the file which variables to plot.
  - Step 4: Give labels to the axes (and to the legend).
  - Step 5: Give a title to the chart.
  - Step 6 (last step): Assign plotting properties to the chart.

- [ ] The second p has for text "Et voila! A interactive chart gets generated, with the help of the Plotly Javascript library."

- [ ] The second ul has li elements nested with the following text:

  - You can export the chart as PNG image to share with others or include in reports or presentations.
  - You can also go back to the previous steps to use different parameters and regenerate the chart.

- [ ] The StyledButton of type "button" takes an onClick attribute which has handleClick as prop. The text of the button is "Get started".
