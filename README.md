# **TUSH**
## **T**emple **U**niveristy **S**Hell

### Build the executable file by running 
```bash
make
```
.The executable `shell` will be generated in the root directory of the project, so just run `./shell` to run the shell.

The `build/` folder will contain all the .o files that are generated upon compilation.  I decided to set those apart from the files in the `src/` folder because I want to keep the program space as clean as possible.  

The source code is in the `src` folder. I modularized the project structure to the best of my ability since this is going to be a large project.

All functions that perform parsing of input are located in `src/parsingUserInput/helpers.c`, including the given `parse()` function, `buildUserEntry()`, which builds the userEntry struct, and `splitCommand()` which builds each Command struct in the userEntry array, pipeParsedInput(). 

All of the built-in shell functions live in `src/builtInShellFunctions/builtIn.c` and are imported and used the same way as the parser files.  

The code for building pipes, changing file descriptors and running new processes is in `src/programExecution/runProcess.c`

The given `README.md` along with the other project detail files in the `projectDetails` folder.

Make sure that you run make clean after you are done
```bash
make clean
```

 make clean will delete everying in the `build/` folder and remove the `shell` executable


### Find more information about how to shell works in `outline.txt`