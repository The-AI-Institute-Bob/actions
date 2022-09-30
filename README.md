# Professor Bob Github Actions

## Create an action

1. Create a new folder with the action name
2. Under this new folder
   - Create a file `action.yml` with action definition
   - Create a `README.md` file with description/documentation
   - Add as many file as needed

```
root
+-- action-1
|	+-- action.yml
|	+-- README.md
|
+-- action-2
	+-- action.yml
	+-- README.md
```

## How to use an action

In github workflow or github action:

```yaml
- uses: The-AI-Institute-Bob/actions/<action-name>
  with:
    arg1: value
    arg2: value
    arg3: value
```

- In workflows &rightarrow; `jobs.steps.uses ...`
- In actions &rightarrow; `runs.steps.uses ...`
