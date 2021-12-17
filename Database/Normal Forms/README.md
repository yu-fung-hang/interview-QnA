# Normal Forms

## 1NF
 
no table column can have tables as values (a cell could not have multiple values)

❌: 

|id    |name|address|
|:---:|:---:|:---:|
|1|Jerry|a-home-address & an-office-address|

✔:

|id    |name|home address|office address|
|:---:|:---:|:---:|:---:|
|1|Jerry|a-home-address|an-office-address|

## 2NF

