# Homepage

## Value proposition

As a user
I want to see a homepage with an introduction to the website, a row of example images for different types of charts and a "Get Started" button so that I can go start the plotting process on the next page.

## Description

- h1 header with name of website.
- Paragraph to introduce the concept of the website.
- List of example images for different types of charts.
- h2 header to announce a list of the steps for the plotting process.
- Unordered list containing these steps.
- Paragraph to announce that a chart is generated.
- Unordered list of possible actions once a chart is generated.
- A deepskyblue button with the text "Get started".
- The elements do not extend to each end of the page, but are centered in the middle.

## Acceptance criteria

- [ ] A click on the button brings the user to the page with the list of chart types.

## Tasks

### Creation of global styling file

- [ ] Create a styles.js file.

- [ ] Go to styles.js and make a named import of createGlobalStyle from "styled-components".

- [ ] Make a default export of createGlobalStyle, where you write the following styling properties:
      \*,
      \*::before,
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

### Creation of the pages folder and files inside

- [ ] Create a "pages" folder.

- [ ] Inside this folder create a index.js file.

- [ ] Inside this folder create a ListOfChartsPage.js file.

- [ ] Inside this folder create a \_app.js file.

### \_app.js file

- [ ] Go to the \_app.js file and make a default import of createGlobalStyle from "../styles".

- [ ] Declare a function App and export it by default.

- [ ] The function returns the createGlobalStyle component.

### Creation of the assets folder and chart-examples subfolder, and creation of images

- [ ] Create an "assets" folder and inside of it a "chart-examples" folder.

- [ ] In the browser go to the codesandbox website, log in, click on "Create a sandbox", then click on "React, then give the name chart-examples for the file.

- [ ] In the dependencies menu, search and install these libraries: plotly.js 2.29.1 and react-plotly.js 2.6.0.

- [ ] Go to the App.js file that was generated and open the preview. Make a default import of Plot from "react-plotly.js".

- [ ] Replace the content of the return statement by this code snippet:
      `<div
      className="App"
      style={{
        display: "flex",
        justifyContent: "center",
        alignItems: "center",
        height: "100vh",
      }}
    >
  <Plot
        data={[
          {
            x: [1, 2, 3, 4, 6, 8, 10, 12, 14, 16, 18],
            y: [32, 37, 40.5, 43, 49, 54, 59, 63.5, 69.5, 73, 74],
            mode: "lines",
            type: "scatter",
            name: "Boys",
            line: {
              color: "blue",
              dash: "solid",
              width: 5,
            },
          },
           {
            x: [1, 2, 3, 4, 6, 8, 10, 12, 14, 16, 18],
            y: [30, 36, 39, 42, 48, 53, 58, 62, 67.5, 68, 68.5],
            mode: "lines",
            type: "scatter",
            name: "Girls",
            line: {
              color: "red",
              dash: "dash",
              width: 5,
            },
           }, 
          ]}
        layout={{
          title: {
            text: "Growth Rate in Children",
          },
          legend: {
            groupclick: "toggleitem",
            itemclick: false,
            itemdoubleclick: false,
          },
          xaxis: {
            title: {
              text: "Age (years)",
            },
            showgrid: true,
            showline: true,
            ticks: "outside",
          },
          yaxis: {
            title: {
              text: "Height (inches)",
            },
            showgrid: true,
            showline: true,
            ticks: "outside",
          },
          width: 600,
          height: 500,
        }}
        config={{
          displayModeBar: true,
          modeBarButtonsToRemove: ["lasso2d", "select2d"],
        }}
      />
    </div>
`

- [ ] Hover over the chart, an interactive menu will appear. Then click on "Download plot as a png".

- [ ] Move the figure file to the chart-examples folder and rename the file with the name "lines plot example".

- Repeat the process for other types of charts. The figure files will have names like "lines plot example", "scatter plot example", "lines+markers plot example", "bar plot example".

### Creation of lib folder and listofchartexamples.js file inside

- [ ] Create a lib folder.

- [ ] Inside this folder create a listofchartexamples.js file.

- [ ] Go to listofchartexamples.js and declare an array examplearray containing objects with the key "name".

  - The name key has for value a string corresponding to the name of the picture contained in the chart-examples folder.

- [ ] Make a named export of examplearray.

### Creation of Components folder and subfolders of components inside

- [ ] Create a Component folder.

- [ ] In this folder create a Button folder.

- [ ] In the Button folder create a Button.styled.js file.

- [ ] Go to Button.Styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledButton component which styles a button element using styled, with background-color set to deepskyblue.

- Make a named export of StyledButton.

- [ ] In the Component folder create a Title folder.

- [ ] In the Title folder create a Title.styled.js file.

- [ ] Go to Title.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledTitle component which styles a h1 element using styled, with text-align set to center.

- Make a named export of StyledTitle.

- [ ] In the Component folder create a Heading folder.

- [ ] In the Heading folder create a Heading.styled.js file.

- [ ] Go to Heading.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledHeading component which styles a h2 element using styled, with text-align set to center.

- [ ] Make a named export of StyledHeading.

- [ ] In the Component folder create a Paragraph folder.

- [ ] In the Paragraph folder create a Paragraph.styled.js file.

- [ ] Go to Paragraph.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledParagraph component which styles a p element using styled, with text-align set to center.

- [ ] Make a named export of StyledParagraph.

- [ ] In the folder Component create a Ul folder.

- [ ] In the Ul folder create a Ul.styled.js file.

- [ ] Go to Ul.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledUl component which styles a ul element using styled, with text-align set to center.

- [ ] Make a named export of StyledUl.

- [ ] In the Component folder create a Div folder.

- [ ] In the Div folder create a Div.styled.js file.

- [ ] Go to Div.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledDiv component which styles a div element using styled, with text-align set to center.

- [ ] Make a named export of StyledDiv.

- [ ] In the Component folder create a Div2 folder.

- [ ] In the Div2 folder create a Div2.styled.js file.

- [ ] Go to Div2.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledDiv2 component which styles a div element using styled, with the display set to flex, the flex-direction set to row, the flex-wrap set to wrap and the justify-content set to space-around.

- [ ] Make a named export of StyledDiv2.

- [ ] In the folder Component create a Img folder.

- [ ] In the Img folder create a Img.styled.js file.

- [ ] Go to Img.styled.js and make a default import of styled from "styled-components".

- [ ] Write a StyledImg component which styles a img element using styled, with the flex-shrink set to 1.

- [ ] Make a named export of StyledImg.

### index.js file

- [ ] In the "pages" folder go to index.js, and make a named import of useRouter from "next/router".

- [ ] Make a named import of examplearray from "../lib/listofchartexamples.js".

- [ ] Make a named import of StyledButton from "../Component/Button/Button.styled".

- [ ] Make a named import of StyledTitle from "../Components/Title/Title.styled".

- [ ] Make a named import of StyledHeading from "../Component/Heading/Heading.styled".

- [ ] Make a named import of StyledParagraph from "../Components/Paragraph/Paragraph.styled".

- [ ] Make a named import of StyledUl from "../Components/Ul/Ul.styled".

- [ ] Make a named import of StyledDiv from "../Components/Div/Div.styled".

- [ ] Make a named import of StyledDiv2 from "../Components/Div2/Div2.styled".

- [ ] Make a named import of StyledImg from "../Components/Img/Img.styled.js".

- [ ] Declare a Homepage function and export it by default.

- [ ] Inside the function declare a constant router = useRouter();

- [ ] Write an handleClick function, which pushes using router to the ListOfChartsPage UploadDataPage.js page.

- [ ] The Homepage function returns, nested in a fragment, the StyledTitle component, several line breaks, the StyledParagraph component, several line breaks, the StyledDiv2 component, the StyledHeading component, the StyledUl component, the StyledParagraph component, the StyledUl component, several line breaks and finally the StyledDiv component and nested within the StyledButton component. This div element is necessary in order to center the button horizontally.

- [ ] StyledTitle has for text "PLOTDATA".

- [ ] The first call to StyledParagraph has for text "With PLOTDATA you can use data to easily make customizable publication-quality charts, all without programming.".

- [ ] Nest curly brackets within the StyledDiv2, where you use forEach over examplearray to render the StyledImg component. StyledImg takes an src attribute set to the path of the associated picture, using the name prop.

- [ ] StyledHeading has for text "Overview of the different steps".

- [ ] The first call to StyledUl has li elements nested with the following text:

  - Step 1: Decide what type of graph.
  - Step 2: Upload a CSV file to get the data.
  - Step 3: Choose from the columns in the file which variables to plot.
  - Step 4: Give labels to the axes (and to the legend).
  - Step 5: Give a title to the chart.
  - Step 6 (last step): Assign plotting properties to the chart.

- [ ] The second call to StyledParagraph has for text "Et voila! A interactive chart gets generated, with the help of the Plotly Javascript library."

- [ ] The second call to StyledUl has li elements nested with the following text:

  - You can export the chart as PNG image to share with others or include in reports or presentations.
  - You can also go back to the previous steps to use different parameters and regenerate the chart.

- [ ] The StyledButton of type "button" takes an onClick attribute which has handleClick as prop. The text of StyledButton is "Get started".
