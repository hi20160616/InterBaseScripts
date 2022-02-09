# Usage

## 1. command:
```
isql "TEST1.GDB" -u 'SYSDBA' -p 'masterkey' -i 'test1.sql' -Page 2048 -o 'output.txt'
```
 - `"TEST1.GDB"`: gdb file's fullpath
 - `'SYSDBA'`: default db master username
 - `'masterkey'`: default password
 - `'test1.sql'`: sql script file's fullpath
 - `'output.txt'`: script standard output save path


## 2. test1.sql:
```
INSERT INTO TEST1_TABLE1 (ID, FIELD1, UPDATETIME)
                  VALUES (5, 'testtesttest5', '2022-02-05 11:37:30');

COMMIT WORK;
```


# test log

## Prepare
Register>LocalServer>Description:>UserName:SYSDBA>Password:masterkey>OK

## Create test database

> Importent! start Interbase Server first!!!
```
CREATE DATABASE 'C:\Documents and Settings\Administrator\Desktop\gdbTool\test1.gdb' PAGE_SIZE 2048;
```

## Test isql to insert data
1. command:
```
isql "TEST1.GDB" -u 'SYSDBA' -p 'masterkey' -i 'test1.sql' -Page 2048 -o 'output.txt'
```
2. test1.sql:
```
INSERT INTO TEST1_TABLE1 (ID, FIELD1, UPDATETIME)
                  VALUES (5, 'testtesttest5', '2022-02-05 11:37:30');

COMMIT WORK;
```
