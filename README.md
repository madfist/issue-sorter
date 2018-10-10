# issue-sorter
Sorts and groups issue based on state.

## Build
```
npm install
```

## Usage
```
node main.js <input_json>
```

### Input structure
A `json` file containing the list off issues and the list of states.
```
{
	issues: [
		{
			"issue": "Issue name",
			"state": "State 1"
		},
		...
	],
	states: [
		{
			"from": "State 1",
			"to": "State 2"
		},
		...
	]
}
```

*Fault tolerance*: By default the first state is the *root* but it can change with a later pair. If a new state is introduced without existing parent, it will belong to the *root* state.