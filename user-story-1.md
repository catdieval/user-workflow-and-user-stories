# Select a chart

## Value proposition

As a user
I want a see a list of possible chart types (e.g. line, scatter, bar),
so that I can click on the type I want.

## Description

- h1 heading with "PLOTDATA".
- h2 heading with "Step 1: Decide what type of chart.".
- List (without bullet points) of images corresponding to examples of each type of chart, with corresponding deepskyblue button named after the type of chart, displayed in a row with possibility of wrapping.
- Button with text "Next".
- The elements do not extend to each end of the page, but are centered in the middle.

## Acceptance criteria

- [ ] Clicking on the button for a chart type shows an alert message to inform the user which type of chart was selected.
- [ ] The "Next" button stays disabled until the user has clicked on the button for a chart type.
- [ ] Clicking on the "Next" button brings the user to the page with the data upload.

## Tasks

### Creation of chart-types subfolder in the assets folder and creation of images

- [ ] Inside the assets folder create a chart-types folder.

- [ ] In the browser go to the codesandbox website, log in, click on "Create a sandbox", then click on "React, then give the name chart-types for the file.

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
            line: {
              color: "blue",
              dash: "solid",
              width: 5,
            },
          },
          ]}
        layout={{
          xaxis: {
            showline: true,
            ticks: "",
          },
          yaxis: {
            showline: true,
            ticks: "",
          },
          width: 600,
          height: 500,
        }}
      />
    </div>
`

- [ ] Hover over the chart, an interactive menu will appear. Then click on "Download plot as a png".

- [ ] Move the figure file to the chart-types folder and rename the file with the name "lines plot".

- Repeat the process for other types of charts. The figure files will have names like "lines plot", "scatter plot", "lines+markers plot", "bar plot".

### Creation of listofcharttypes.js file inside the lib folder

- [ ] Inside the lib folder create a listofcharttypes.js file.

- [ ] Go to listofcharttypes.js and declare an array chartarray containing objects with the keys "type", "mode" and "name".

  - The type key has for value a string corresponding to the name of the type of chart (e.g. "scatter", "bar").
  - The mode key has for value a string corresponding to the name of the type of plotting mode (e.g. "lines", "markers", "lines+markers").
  - The name key has for value a string corresponding to the name of the associated picture contained in the chart-types folder.

- [ ] Make a named export of chartarray.

### Creation of UploadDataPage.js in the pages folder

- [ ] In the pages folder, create a UploadDataPage.js file.

### Creation of a ChartItem subfolder in the Components folder

- [ ] Inside the Component folder create a ChartItem folder.

- [ ] Inside the ChartItem folder create a ChartItem.js file.

### ListOfChartsPage.js file

- Go to ListOfChartsPage.js and make a named import of useRouter from "next/router".

- Make a named import of useState from "react".

- [ ] Make a default import to the ChartItem component from "../Component/ChartItem.js".

- [ ] Make a named import of StyledTitle from "../Components/Title/Title.styled".

- [ ] Make a named import of StyledHeading from "../Component/Heading/Heading.styled".

- [ ] Make a named import of StyledDiv2 from "../Components/Div2/Div2.styled".

- [ ] Make a named import of StyledDiv from "../Components/Div/Div.styled".

- [ ] Make a named import of StyledButton from "../Components/Button/Button.styled".

- [ ] Make a named import of chartarray from "../lib/listofcharttypes.js".

- [ ] Declare a ListOfCharts function and export it by default.

- [ ] Inside the function declare a state for the isSelected variable using useState. The initial value is a boolean set to false.

- [ ] Declare a constant router = useRouter();

- [ ] Write an handleClick function, which pushes using router to the UploadDataPage.js page.

- [ ] The function returns a fragment, and nested within, the StyledTitle component, several line breaks, the StyledHeading component, several line breaks, the StyledDiv2 component, several line breaks, finally the StyledDiv component and nested within the StyledButton component.

- [ ] StyledTitle has for text "PLOTDATA".

- [ ] StyledHeading has for text "Step 1: Decide what type of chart.".

- [ ] The StyledButton of type "button" takes an onClick attribute which has handleClick as prop. The button has the disabled attribute set to !isSelected. The text of StyledButton is "Next".

- [ ] Nest curly brackets within the StyledDiv2, where you use forEach over chartarray to render the ChartItem component.

- [ ] Give the key name and setIsSelected as props to ChartItem.

### ChartItem.js file

- [ ] Install use-local-storage-state.

- [ ] Go to the ChartItem.js file, and inside make a default import of useLocalStorageState from "use-local-storage-state".

- [ ] Make a named import of StyledButton from "../Button/Button.styled".

- [ ] Make a named import of StyledImg from "../Img/Img.styled.js".

- [ ] Declare a ChartItem function and export it by default.

- [ ] The function takes for argument the prop name.

- [ ] Inside the function use a local storage state for the clickedChartType variable, with "" as default value.

- [ ] Write an handleClick function, taking event as argument.

- [ ] This function uses the setter setClickedChartType with the value event.target.value.

- [ ] This function calls an alert function with the text `You chose "${clickedChartType}"`.

- [ ] This function uses the setter setIsSelected with the boolean value true.

- [ ] The ChartItem function returns, within a fragment, the StyledButton component and the StyledImg component.

- [ ] StyledImg takes an src attribute set to the path of the associated picture, using the name prop.

- [ ] The StyledButton of type "button" takes an onClick attribute which has handleClick as prop. The text of the button is the name prop.
