# Program for Building a Commit Dependency Graph in PlantUML  
## General Description  
The program is written in **C++** and does not use any external libraries or tools.  
The configuration file is named **config.ini** and must be located in the same directory as the executable file.  

## Configuration File  
```
[options]
    plantuml_jar_path = path to the PlantUML visualization program
    repo_path = path to the repository to be processed
    output_path = path to the output file (in PNG format)
    date = date used to filter commits (Unix timestamp)
```

## Project Build  
```bash
git clone https://github.com/farblose/kalogit.git
```
Then edit the **config.ini** file.  
```bash
clang++ GitIdxParser.cpp GitPackParser.cpp main.cpp -lz -o graphviz && \
./graphviz
```

## Running Tests  
```bash
clang++ GitIdxParser.cpp GitPackParser.cpp test.cpp -lz -o test && \
./test
```
