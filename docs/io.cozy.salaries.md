[Table of contents](README.md#table-of-contents)

# Salaries doctype

## `io.cozy.salaries`

- `vendor`: {string} - Vendor which issued the salary
- `date`: {date} - Date the salary was emitted
- `amount`: {number} - Amount of the bill, __always positive__ even if it is the salary of an employee


### Relationships

The eventual related documents
- `payslip`: {object} - The associated file. ex: 
```
{
  data: {
    _id: "c43645a93831827c7ec512eac3006e51",
    _type: "io.cozy.files"
  }
}
```


### Some more attributes for employee's payslip

The are some more possible attributes for employee salaries.

- `isEmployee`: {boolean} - Indicate if this salary is paid to an employee of the owner of the cozy. If false, this is a salary received by the owner.
- `beneficiary`: {string} - Indicate the name of the employee

### Example

```
{
  "_id": "62e5d80d6e11d19992b7efce794263f0",
  "amount": 2000,
  "date": "2018-02-07T23:00:00.000Z",
  "vendor": "Payfit",
  "payslip": "io.cozy.files:c43645a93831827c7ec512eac3006e51",
  "metadata": {
    "version": 1
  },
  $relationships: {
    payslip: { data: { _id: "c43645a93831827c7ec512eac3006e51", _type: "io.cozy.files" } }
  }
}
```

```
{
  "_id": "62e5d83d6e11d19992b7efce794263f0",
  "amount": 100,
  "date": "2018-04-07T03:00:00.000Z",
  "vendor": "CESU",
  "isEmployee": true,
  "beneficiary": "Pierre Richard",
  "metadata": {
    "version": 1
  },
  $relationships: {
    payslip: { data: { _id: "c43645a93831827c7ec512eac3006e51", _type: "io.cozy.files" } }
  }
}
```
