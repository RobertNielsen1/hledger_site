# Convert CSV files

Here's a quick example of reading CSV data with hledger.

Say we have downloaded `checking.csv` from a bank for the first time:
```csv
"Date","Note","Amount"
"2012/3/22","DEPOSIT","50.00"
"2012/3/23","TRANSFER TO SAVINGS","-10.00"
```

We tell hledger how to intepret this with a file named `checking.csv.rules`, using the [CSV rules syntax](http://hledger.org/manual.html#csv-format). Eg:
```rules
# skip the first CSV line (headings)
skip 1

# use the first three fields in each CSV record as transaction date, description and amount respectively
fields   date, description, amount

# prepend $ to CSV amounts
currency $

# always set the first account to assets:bank:checking
account1 assets:bank:checking

# if the CSV record contains ‘SAVINGS’, set the second account to assets:bank:savings
# (if not set, it will be expenses:unknown or income:unknown)
if SAVINGS
  account2 assets:bank:savings
```

Now hledger can read this CSV file as journal data:

```shell
$ hledger -f checking.csv print
using conversion rules file checking.csv.rules
2012/03/22 DEPOSIT
    income:unknown             $-50.00
    assets:bank:checking        $50.00

2012/03/23 TRANSFER TO SAVINGS
    assets:bank:savings         $10.00
    assets:bank:checking       $-10.00
```

We might save this output as `checking.journal`, and/or merge it (manually, or using the [import](http://hledger.org/manual.html#import) command) into the main journal file.

We could also just run reports on the CSV file directly:
```shell
$ hledger -f checking.csv balance
using conversion rules file checking.csv.rules
              $50.00  assets:bank
              $40.00    checking
              $10.00    savings
             $-50.00  income:unknown
--------------------
                   0
```

Here are more [CSV rules examples](https://github.com/simonmichael/hledger/tree/master/examples/csv).

Here's how to [[Customize default CSV accounts]].

There are many alternate CSV conversion tools at [plaintextaccounting.org -> data import/conversion](https://plaintextaccounting.org/#data-importconversion) (nine CSV->*ledger tools at last count). [hledger-import-dsl](https://github.com/hpdeifel/hledger-import-dsl) is a fully programmable hledger-ish option.
