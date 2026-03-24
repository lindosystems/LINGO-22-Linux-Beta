# LINGO 22 for Linux Beta

## Getting Started

To install LINGO on Linux place `LINGO64_22.0.147.tar.gz` in your `/opt` directory. next run the command

```bash
tar  -xvzf  LINGO64_22.0.147.tar.gz
```
to extract the file into /opt/LINGO64_22. Next open `.bashrc` and add the following lines

```bash
export  LINGO_22_HOME=/opt/LINGO64_22
export  PATH="/opt/LINGO64_22/bin/linux64:$PATH"
```

then reload 

```bash
source ~/.bashrc
``` 

## Running LINGO models

The `runlingo` command is able to run both the `.lng` and `.ltf` LINGO model extensions. As long as your `.bashrc` file was updated following the previous chapter the following should work fine. To get started with `runlingo` first try the following help command 

```bash
runLingo -h
```
  to see all available flags and commands
 ```bash
 Usage:
        runlingo [flags] <model_file>
        runlingo [command]

Flags:
        --callback, -c  Enable callbacks
Commands:
        --version, -v   Show version information
        --demo, -d      Write demo license
        --help, -h      Show this help message
```

. Before running a LINGO model, a license file `lndlng22.lic` must be located in `/opt/LINGO64_22/license/linux64`. If you do not already have a file run the following command

```bash
runLingo -d
```
```
Saving user info to /opt/LINGO64_22/userinfo.txt

      A six-month demo license was successfully created a demo license /opt/LINGO64_22/license/linux64/lndlng22.lic and user file /opt/LINGO64_22/userinfo.txt.
      This demo installation is limited in capacity. If you are an educational user,
      you can request a demo license for a full version of LINGO. To request a full demo,
      you will need to email /opt/LINGO64_22/userinfo.txt to sales@lindo.com. You will then be sent a demo license
      for a full capacity version of LINGO.
```

from the above output a license was generated to run small models and userinfo.txt was generated to send to us for a full license. 

With a license file in the correct location LINGO models can be ran with the runlingo command. Your LINGO installation comes with a directory of sample models for you to try to run `Tran.lng` for example run the following command

```
runlingo /opt/LINGO64_22/samples/Tran.lng
```

. This will run the model and display the log output. For a periodic status report of the model use the flag `-c` with runlingo 

 ```
runlingo -c /opt/LINGO64_22/samples/Tran.lng
```

. Use this for a model that is not solved instantly, and you would like to stay informed of what is going on. 

##  The VS Code extension

If you are using a GUI-based Linux distribution, you can install Visual Studio Code and add the **LINGO LSP** extension. This provides syntax highlighting, autocomplete, hover hints, and a _Run LINGO_ button for executing LINGO models directly from the editor.

 