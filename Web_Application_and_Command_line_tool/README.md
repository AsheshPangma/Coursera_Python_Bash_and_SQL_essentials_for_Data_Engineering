# Web Application and Command-Line Tool

## Week 1

### Introductio to Jupyter Notebook

#### Code Cells in Jupyter

Jupyter notebook contains executable documents, Cells, Code, text and images. The kernel comprise of Python, R or Julia.

To install Jupyter notebook, type:
```
pip install jupyter
```
To run Jupyter notebook, type:
```
jupyter notebook
```
Then the Jupyter notebook prompt will open. Choose python3 kernel and proceed.
To run codes in the cell, press the "run" button or press "shift+enter".

To see all the directories in os, type the following:
```
import os
os.listdir()
```

To read a csv file:
```
import pandas as pd
df = pd.read_csv('path/file_name.csv')
df
```

`!ls` commands list all the files in the current directory.

To print the working directory, type the following:
```
curl_pwd = !pwd
print(curl_pwd)
```

#### Text Cells in Jupyter

In this section we learned about markdown files in Jupyter notebook. To use a cell as markdown from the dropdown menu select "Markdown". Then, proceed with the text as markdown file.
To include link, type:
`.[Duke.org](link)`

To include image, type:
`!.[Duke_Image](./filename.png)`

#### Magics in Jupyter

To run Magics command in Jupyter notebook we usr "%" symbol. A single "%" for single line command and "%%" for command in a cell. To view all the commands available in magic, type `%lsmagic` in the cell and run the command.
`%timeit` command can be used to view the time required to execute the code. For example:
`% timeit [x for x in range(1000)]`
```
%%timeit
for x in range(10000):
    z = x + 1
```
An example showing write to a file is shown below:
```
%%writefile hello.py

def say_hello():
    print("hello")
    
say_hello()
```
To run the python file, type `%run filename.py` in the cell and run it.

```
%env
```
```
%env USER_KEY=1234
%env USER_KEY
```
To run Ruby code in the cell, we run magic script followed by code in Ruby as follows:
```
%%script ruby
puts "Hello!"
```

#### Overview of Jupyter Lab

To install Jupyterlab, type `pip install jupyterlab` in the prompt. After installing Jupyterlab, you can run it by using the command `jupyter lab`. Then a prompt will open showing Jupyterlab. It provides several windows to work similar to that of an IDE. We can debug our code as well as add other extensions on Jupyterlab for better experience.
The picture below shows the prompt for Jupyterlab.
![](Web_Application_and_Command_line_tool/images/jupyterlab_prompt.png)

## Week 2


## Week 3


## Week 4


