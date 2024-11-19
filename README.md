# GenerateProjectShort

This script analyzes the project structure and generates a single text file containing the directory tree and the contents of all readable files. This file is intended for use with LLMs (Large Language Models), allowing them to gain full context of the project and answer questions about its structure and code.

## Features

* **Single report file creation:** The script generates a file `ProjectOneFile.txt` containing all necessary information about the project.
* **Directory structure display:** Visualizes the project structure as a directory tree, making it easier for LLMs to navigate the project.
* **File content inclusion:** Includes the contents of files with supported extensions in the report, allowing LLMs to analyze the code and understand its functionality.
* **Wide range of extensions supported:** Supports numerous programming languages, scripting languages, configuration files, markup, and other file types. See the list of supported extensions below.
* **File and directory exclusion:** Allows ignoring specific files and directories, such as `.git`, `venv`, `node_modules`, and others, which are not necessary for LLM project understanding. This helps reduce the output file size and improve LLM performance.
* **Ease of use:** Simply place the `GenerateProjectShort.py` script in the root directory of your project and run it.

## Supported File Extensions

The script supports the following file extensions:

```
.txt .java .html .css .js .py .c .cpp .cs .go .php .rb .swift .kts .rs .scala
.pl .hs .clj .exs .erl .groovy .lua .r .pas .m .v .fs .jl .dart .kt .cl .sh
.bash .bat .ps1 .awk .perl .json .xml .yaml .properties .ini .toml .cfg
.conf .env .plist .gradle .sbt .md .markdown .rst .adoc .tex .org .doxygen
.log .csv .tsv .sql .sqlite .avro .parquet .gitignore .dockerfile .makefile
.cmake .qml .graphql .proto .tf .tfstate .webmanifest .svg .eml .mbox
```

## Usage

1. Copy the `GenerateProjectShort.py` file to the root directory of your project.
2. Run the script: `python GenerateProjectShort.py`
3. The report will be generated in the file `ProjectOneFile.txt` in the same directory.

## Configuration

You can customize the list of ignored files and directories by modifying the `IGNORE_LIST` variable in the script.

## LLM Compatibility

Tested on the following LLMs:

* GPT-4o-mini
* GPT-4o
* Gemini 1.5 Pro
* Gemini 1.5 Pro 002
* Claude 3.5 Sonnet
* OpenAI-o1-preview
* OpenAI-o1-mini

## Example

After running the script in your project's root directory, the `ProjectOneFile.txt` file will contain information about the project structure and file contents, for example:

```
MyProject/
├── src/
│   ├── main.py
│   └── utils.py
└── data/
    └── data.csv

main.py
```py
print("Hello, world!")
```


utils.py
```py
def my_function():
    print("Hoho, test function and test print!")
```

data.csv
```csv
Name,Age
Alice,30
Bob,25
```
