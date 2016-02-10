# ASDO

The `script` file is the commands in Ubuntu terminal. 
Before using this script, you should:

1. Download the road data from 
[TAREEG](http://siwa-umh.cs.umn.edu/app/webroot/osme/).

2. Edit the `config` file to tell the paths to the `node.txt` and `edge.txt` files
of the road data you downloaded.

3. Follow the `script` commands. 



### Contraction Hierarchies
The script used the codes of Contraction Hierarchies (CH) algorithm from 
[KIT](http://algo2.iti.kit.edu/english/routeplanning.php).
In `script` file, we first move the `EDGE.txt` file into 
CH folder, and run the `./main` with `EDGE.txt` to generate
`inputCH`. Since the result from `./main` is a binary file,
we also implement a small Python program to translate the binary
file to readable file.

**Before running `./main` in CH folder, you may need to 
recompile the codes in CH folder using `make`.**

