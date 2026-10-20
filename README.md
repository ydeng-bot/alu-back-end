# alu-back-end

Back-end projects focused on consuming a REST API with Python and exporting the data to different formats.

All scripts use the [JSONPlaceholder](https://jsonplaceholder.typicode.com/) API and the `requests` module.

## Requirements

- Python 3
- `requests` module (`pip install requests`)

## Project structure

```
alu-back-end/
├── README.md
└── api/
    ├── 0-gather_data_from_an_API.py
    ├── 1-export_to_CSV.py
    ├── 2-export_to_JSON.py
    └── 3-dictionary_of_list_of_dictionaries.py
```

## Tasks

### 0. Gather data from an API
`api/0-gather_data_from_an_API.py`

Takes an employee ID as an argument and prints the employee's TODO list progress:

```
$ python3 api/0-gather_data_from_an_API.py 2
Employee Ervin Howell is done with tasks(8/20):
	 distinctio vitae autem nihil ut molestias quo
	 ...
```

### 1. Export to CSV
`api/1-export_to_CSV.py`

Takes an employee ID and exports all of that employee's tasks to `USER_ID.csv`.

Format: `"USER_ID","USERNAME","TASK_COMPLETED_STATUS","TASK_TITLE"`

```
$ python3 api/1-export_to_CSV.py 2
$ cat 2.csv
```

### 2. Export to JSON
`api/2-export_to_JSON.py`

Takes an employee ID and exports all of that employee's tasks to `USER_ID.json`.

Format: `{"USER_ID": [{"task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS, "username": "USERNAME"}, ...]}`

```
$ python3 api/2-export_to_JSON.py 2
$ cat 2.json
```

### 3. Dictionary of list of dictionaries
`api/3-dictionary_of_list_of_dictionaries.py`

Exports the tasks of all employees to `todo_all_employees.json`.

Format: `{"USER_ID": [{"username": "USERNAME", "task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS}, ...], ...}`

```
$ python3 api/3-dictionary_of_list_of_dictionaries.py
$ cat todo_all_employees.json
```

## Author

Yom Deng Garang ([ydeng-bot](https://github.com/ydeng-bot))
