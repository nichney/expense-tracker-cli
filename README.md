# Expense Tracker CLI

https://roadmap.sh/projects/expense-tracker

A simple command-line interface (CLI) expense tracker written in Python that allows users to add, remove, list, and summarize expenses. Expenses are stored in a JSON file (`expenses.json`).

## Features
- Add a new expense with a description and amount.
- Remove an expense by ID.
- List all expenses in a formatted table.
- Summarize expenses for a specific month.
- Stores expenses persistently in `expenses.json`.


### Commands

#### Add an expense
```sh
$ python expense_tracker.py add --description "Groceries" --amount 50
```
- `--description`: Description of the expense (required)
- `--amount`: Amount spent (required)

#### Remove an expense
```sh
$ python expense_tracker.py delete --id 1
```
- `--id`: The ID of the expense to remove (required)

#### List all expenses
```sh
$ python expense_tracker.py list
```

#### Summarize expenses (optionally by month)
```sh
$ python expense_tracker.py summary --month 3
```
- `--month`: (Optional) Specify a month (1-12) to filter expenses

## Example Output
```
ID    | Description    | Amount     | Date       |
------------------------------------------------
1     | Groceries     | 50         | 2024-03-25 |
2     | Coffee        | 5          | 2024-03-26 |
```

## Notes
- If `expenses.json` does not exist, it will be created automatically.
- The script prevents adding empty descriptions or missing amounts.
- The `summary` command will sum expenses for a given month or all expenses if no month is specified.

## License
This project is open-source and available under the MIT License.


