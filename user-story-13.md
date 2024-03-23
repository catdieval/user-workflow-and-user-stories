# Homepage

## Value Proposition

As a user I want to visit the homepage where i can read what is the App about and to get involved.

## Description

![Image](https://github.com/catdieval/capstone-plotdata/assets/148444485/e7380224-5d1f-4fb1-88ce-6b6529426436)

## Acceptance Criteria

- [ ] Title at the top with the name of the website and a logo.
- [ ] Paragraph with text "With PlotData you can easily make customisable publication-quality graphs, all without programming skills.".
- [ ] List of example images for different types of charts.
- [ ] Heading with text "Overview:".
- [ ] Unordered list containing:
  - [ ] "Step 1: Upload a CSV file".
  - [ ] "Step 2: Select the type of graph".
  - [ ] "Step 3: Choose which variables to plot".
  - [ ] "Step 4: Give labels to the axes".
  - [ ] "Step 5: Give a title to the graph".
  - [ ] "Step 6: Assign properties to the graph".
  - [ ] Paragraph with text "Et voila! An interactive graph gets generated, with the help of the Plotly JavaScript library" and where "Plotly" is a link directing to https://plotly.com/javascript/basic-charts/.
  - [ ] Unordered list containing:
    - [ ] "At the top of the graph are functions that allow you to interact with the graph: download plot as a png, zoom, zoom in, zoom out, autoscale, reset axes."
    - [ ] "You can share the graph with others or include in reports or presentations."
    - [ ] "You can also choose different parameters and regenerate the graph."
  - [ ] A "Get started" button where a click causes a render of the UploadData component.

## Tasks

- [ ] Create a feature branch "Homepage".

- [ ] In the lib folder create a file "unorderedListsofBulletPoints.js".

  - [ ] In the file create an arrayOfSteps / arrayOfPossibilities array which contains strings for the different steps / possibilities.

- [ ] Create an UnorderedList component:

  - [ ] It takes arrayOfBulletPoints as prop.
  - [ ] The component returns a ul element and nested inside is a mapping over arrayOfBulletsPoints using a bulletPoint argument to render a li element.
  - [ ] The li has for text bulletPoint and takes bulletPoint as value to the key attribute.

- [ ] Create a HomePage component:

  - [ ] useState for the clickedGetStarted variable with initial value set to false.
  - [ ] Write a handleGetStarted function which sets setHasClickedGetStarted to true.
  - [ ] HomePage renders these components: Paragraph, Container, Heading and Container.
  - [ ] Container has $centered attribute set to "center".
  - [ ] The first render of Container has UnorderedList nested inside.
  - [ ] The second render of Container has UnorderedList and Button nested inside.
  - [ ] The first / second render of UnorderedList takes arrayOfSteps / arrayOfPossibilities as prop to the arrayOfBulletPoints attribute.
  - [ ] Button has for text "Get started" and has handleGetStarted as prop to the onClick attribute.

- [ ] In the \_app.js, add the Homepage component (before UploadData).

- [ ] In UploadData access hasClickedGetStarted.
  - [ ] In the return of UploadData, use a conditional rendering such that the component is displayed only if hasClickedGetStarted is true.
