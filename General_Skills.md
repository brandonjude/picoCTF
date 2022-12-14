### Obedient Cat

Download the flag file link using “wget” command:
```console
~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag   
```
Then output the contents of file, which is the flag, to the terminal using “cat” command:
```console
~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
```

&nbsp;

### Python Wrangling

Download the Python script, password file, and encrypted flag file using “wget” command:
```console
~$ wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py 
~$ wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/pw.txt
~$ wget https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en  
 ```

Run the Python script, use the -d (decrypt) argument, and use the encrypted flag file as an input
```console
~$ python ende.py -d flag.txt.en
```

Copy and paste the password from the password file then the flag is revealed
```console
Please enter the password:68f88f9368f88f9368f88f9368f88f93
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}
```
&nbsp;

### Wave a flag

Download the provided program
```console
~$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
```
Make the program an executable
```console
~$ chmod +x warm
```
Run the executable but add a -h (or --help) argument to show flag. On other UNIX/LINUX programs,\
-h or --help will display a manual for using the program or command
```console
~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
Notice that the current directory needed to be specified (./). This is because executables can only be executed in predefined directories such as in the following:
```console
/usr/local/nvm/versions/node/v18.10.0/bin
/usr/local/sbin
/usr/local/bin
/usr/sbin
/usr/bin
/sbin
/bin
```
To run an executable from any other directory, it must be specified. You can view default directories where executables are located by running the following ($PATH is an environment variable : 
```console
~$ echo $PATH | tr ':' '\n'
```






