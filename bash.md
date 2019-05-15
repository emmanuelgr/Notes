#Bash commands
**Must remember commands**

###Find file with text  
```sh
grep -R "stringToSearchFor" .
```

###Open app  
opens a file or a directory or URL
######-a application name
```sh
open
```

###Processes accessing the Internet  
```sh
sudo lsof -i
```

###DiskUsage
###### −s Display an entry for each specified file.
###### −h "Human-readable" output
```sh
du -sh xxxFileNamexxxx
```

###Prevent system sleeping
###### −i Create an assertion to prevent the system from idle sleeping.
###### −d Create an assertion to prevent the display from sleeping.
```sh
caffeinate
```

###Start http server
```sh
python -m SimpleHTTPServer 8000
```

###Stress mac
```sh
yes
```

###Running processes
```sh
top
```

###Find file
```sh
find ~/Desktop -name '*fileNameEnds'
```

###Locate file cached, db  
###### -i case insensitive
```sh
locate -i filename
```

### view man pages in Preview
```
man+(){
  man -t "${1}" | open -f -a /Applications/Preview.app/
}
```

###Kill program
pid process id, find with top or activity Monitor
name the name of the process
######  -9 flag terminates non responsive app
```sh
kill pid || name
```
