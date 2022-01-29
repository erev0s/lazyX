# lazyX
A simple and small python script to call [dex2jar](https://github.com/pxb1988/dex2jar) and then [cfr](http://www.benf.org/other/cfr/) or [procyon](https://github.com/mstrobel/procyon).

It takes as an argument an apk which is converted to the corresponding jar files from dex2jar and then depending on your choice cfr or procyon decompile it to Java.



### Example usage
~~~~
$ python3 lazyX -d procyon basic.apk
dex2jar ----> Converting...
dex2jar basic/classes.dex -> basic/classes.jar
procyon ----> Decompiling...
Completed!
~~~~


### Adding it to the Path
As you would add any script to your path you can put lazyX for example in `/usr/local/bin`.  

You can run something like the following from within the repo after you have download it.
~~~~
sudo mv libs lazyX /usr/local/bin && sudo chmod +x /usr/local/bin/lazyX
~~~~
**Do remember to update the shebang line depending on your environment!**



### Updating versions of `dex2jar` and `cfr`
If you would like to update the versions of dex2jar and cfr that are being used by the script then all you have to do is delete and replace the directory `dex-tools-2.2-SNAPSHOT` with the new version of dex2jar downloaded from [here](https://github.com/pxb1988/dex2jar/releases) and also replace the cfr and procyon jar files with the new ones you would like.

**As a final step you have to update the following three variables in the script accordingly:**
~~~~
name_of_the_DEX2JAR_directory = "libs/dex-tools-2.2-SNAPSHOT"
name_of_the_cfr_jar = "libs/cfr-0.152.jar"
name_of_procyon_jar = "libs/procyon.jar"
~~~~
