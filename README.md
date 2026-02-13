# LINGO 22 Linux Beta

To install LINGO on Linux place `LINGO64_22.0.143.tar.gz` in your `/opt` directory.
next run the command

```bash
tar  -xvzf  LINGO64_22.0.141.tar.gz
```
to extract the file into /opt/LINGO64_22. Next open `.bashrc` and add the following lines

```bash
export LINGO_22_HOME=\opt\LINGO64_22
export PATH="/opt/LINGO64_22/bin
```

Next place the `lndlng.lic` license file in `/opt/LINGO64_22/` directory.
Now you will be able to run `.ltf` scripts through the `runlingo` command.

```
runLingo /opt/LINGO64_22/samples/TRAN.ltf
```

The only modification to an `.lng` file required is adding `go` after the `END` in the model.
See `/opt/LINGO64_22/samples` for more information. 

If you are using a GUI version of Linux install the VS Code editor and download the `LINGO LSP` extension.  This provides syntax highlighting, auto complete, hover hints, and a runLingo button for running your `.ltf` models in the editor.

The next update to the runLingo command will extend support for `.lng` models and other LINGO features. Please let us know what you would like to see in a Linux version. 
