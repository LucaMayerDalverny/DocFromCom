# DocFromCom User Manual (Version 1.0)

## Table of contents

1. [Use advices](#advices)
2. [Documentation generator](#generator)
    1. [Command](#commandgenerator)
    2. [Writting the comments](#commentgenerator)

## Use advices <a name="#advices"></a>

DocFromCom is a `.phar` archive. Instead of placing this archive in the folder containing your project and copying it at every creation of a new project, it is recommended to place the archive in the folder where all your projects are.

## Documentation generator <a name="#generator"></a>

### Command <a name="#commandgenerator"></a>

To generate the documentation out of a file, open a prompt in the the folder where the `.phar` archive is and execute the following command :  

```bash
php DocFromCom.phar document:generate "Path/MyFile" "FileExtension" [Output extension] [Language]
```

The path to the source code file can be absolute or relative. The programming languages available for the input file are :

+ Every programming languages that has multilign comment in the form `/** Comment */` like c, c++, java and php languages.
+ Every programming languages that has comment in the form `#Comment` like Python language.

The output file extensions available are :  

+ `md` to have the documentation in [markdown](https://en.wikipedia.org/wiki/Markdown) (Default value)
+ `tex` to have the documentation in [LaTeX](https://en.wikipedia.org/wiki/LaTeX)

The language available for the added elements to the output file by DocFromCom are :

+ `EN` for english (default value)
+ `FR` for french

### Writting the comments <a name="#commentgenerator"></a>

#### File Header

#### Data structure

#### Functions

#### Oriented Object specifications (class, methods, attributes)