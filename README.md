chmod
=====
`chmod` is a linux command
We can use `chmod` to change the access permission ([file](https://en.wikipedia.org/wiki/Computer_file) and [directories](https://en.wikipedia.org/wiki/Directory_(computing)))

### Table 1

|select file|user    |groups      |others      |file|
|----------|:----------:|:----------:|:----------:|----------:|
|-(dash)means file|rwx|rwx|rwx|test.txt(file name)|
|1|rw-|r-x|-wx|test.txt|
|2|r-x|rw-|rw-|test.txt|
|3|rwx|rwx|rwx|test.txt|

## rwx meaning
> r means read permission
> w means write permission
> and x means execute permission.

+  we can see the table1 of row1 **user** have **rw-** read and write pesmirrion not execute permission
+ we can see the table1 of row1 **group** have **r-x** read and execute pesmirrion not write permission
+ we can see the table1 of row1 **others** have **-wx** write and execute pesmirrion not read permission


we have a file like **test.txt**
so we want to see **test.txt** file access permissions
just write this command in terminal
```bash
ls -l test.txt
````
then you will see like this:
![alt text](https://user-images.githubusercontent.com/20683034/31855828-d476720a-b6d4-11e7-8bd8-2ff3e573157a.png)

In this photo we see the ***user*** have read and write permission don't have execute permission. then we see ***group*** have  only read permission don't have weite and execute permission and ***others*** have aslo read permission only don't have write and execute permission
If we want to change the permission we need to use `chmod` command
we just write this command in terminal to change the permission:
```bash
chmod u+x test.txt
```
if you wrote this command the **user** have execute permission now,
(+means give the permission)
```bash
chmod u-x test.txt
```
if we wrote this command the **user** don't have execute permission now,
(-means take the permission)
let me show you a photo  both command:
![alt text](https://user-images.githubusercontent.com/20683034/31856163-8eedd45a-b6dc-11e7-800d-6ad81774ae87.png)
you can see this photo **user** didn't have execute permission, write this command  `chmod` **u+x test.txt** to gave **user** execute permission then i wrote `chmod` **u-x test.txt** to take execute permission from **user**
