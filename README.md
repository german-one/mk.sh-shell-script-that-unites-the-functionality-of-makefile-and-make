## **`mk.sh` - shell script that unites the functionality of `makefile` and `make`**  
  
Copy the script into the folder with your C and C++ source files to compile and link them into a ELF binary.  
Optionally run the app as soon as it is created or perform a memory check.  
The script requires `gcc`, `g++` and `valgrind` to be installed. Apart from that, only POSIX-compliant tools and syntax are used in the code.  
Adjust settings for the compilation in the script. Run the script with or without additional options or arguments as described:  
```
./mk.sh [-drmh] [argument...]
 -d Compile a debug build. (release build by default)
 -r Run the compiled application.
 -m Perform a memory check. (implies -r)
 -h Print the help message and quit. (further options ignored)
 argument... Arguments passed to the application. (applies to -r or -m)
```
  
The script searches recursively for `*.c` and `*.cpp` source files in all subdirectories.  
It automatically creates an `obj` folder for the compiled objects and a `bin` folder for the linked apps.  
<br>
  
#### Example Commands  
  
- Compile all source files using the default configuration.  
`./mk.sh`  
  
- Compile all source files using the default configuration. Run the app with arguments -x and foo.  
`./mk.sh -r -- -x foo`  
  
- Compile all source files using the `debug` configuration. Run the app while performing a memory check.  
`./mk.sh -dm`  
  
<br>
