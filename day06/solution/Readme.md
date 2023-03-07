### Shell Script

> Check Which type of shell installed in your system
```python
cat /etc/shells
```
> We can create any file for shell script
> 
> But best prectice is to create .sh file for script
```python
touch file_name.sh

# using nano editor
nano file_name.sh

# using vim editor
vim file_name.sh
```
> After that we need to give execute permission.
```shell
chmod +x fileName

# or (end with .txt)
chmod +x *.txt

# or (start with a pattern)
chmod +x patt*

# or (all file)
chmod +x *
```

> Then run it 
```python

# Here . means current directory
# Then /file_name.sh
./file_name.sh

```

> Create bash script
> Defalt is /bin/sh
> Here (#!) is called shebang
```shell
#!/bin/bash

echo "Hello World"
```

> Create python script
> First check weather python is installed or not `python --version`
> Then check python location `type python`
```shell
#!/usr/bin/python

print("Hello World")
```