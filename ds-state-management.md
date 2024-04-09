## Value proposition

As a developer
I want to refactor the code
so that the number of useState calls is being reduced and to have an overall well structured state management.

## Acceptance Criteria

- [ ] In components with more than two states the states are stored in one state with the help of an object.

## Tasks

- [ ] Create a feature branch "State-management".

- [ ] In general:

  1.  Create an object for the initial values: `const initialvalues ={state1:"", state2:"", state3:""}`
  2.  Create a state: `const [data, setData] = useState(initialvalues)`
  3.  Add an `handleChange`: `function handleChangeData(event) {setData({ ...data, [event.target.name]: event.target.value })}`

- [ ] Refactor the states for the step 1, step 3, `LineProperties` and `MarkerProperties` components.

Suggestion from coach:

// Simplified state example
const [chartSettings, setChartSettings] = useState({
clickedChartType: "",
xVariable: [],
yVariable: [],
xKey: "",
yKey: "",
// More settings...
});

// Update chartSettings state in a more generic way
const updateChartSettings = (key, value) => {
setChartSettings((prevSettings) => ({
...prevSettings,
[key]: value,
}));
};
