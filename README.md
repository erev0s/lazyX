# lazyX
A simple and small python script to call [dex2jar](https://github.com/pxb1988/dex2jar) and then [cfr](http://www.benf.org/other/cfr/).

It takes as an argument an apk and output the converted dex files to jar files and then feeds these jar files to cfr which decompiles them to Java.



### Example usage
~~~~
$ python lazyX.py example.apk
dex2jar ----> Converting...
dex2jar example/classes.dex -> example/classes.jar
cfr ----> Decompiling...
Completed!
~~~~


### Adding it to the Path
As you would add any script to your path you can put lazyX for example in `/usr/local/bin`.  

You can run something like the following from within the repo after you have download it.
 - `dex-tools-2.1-SNAPSHOT` is the dex2jar directory.
 - `cfr-0.149.jar` is the cfr jar file.
~~~~
sudo mv dex-tools-2.1-SNAPSHOT lazyX cfr-0.149.jar /usr/local/bin && sudo chmod +x /usr/local/bin/lazyX
~~~~



### Updating versions of `dex2jar` and `cfr`
If you would like to update the versions of dex2jar and cfr that are being used by the script then all you have to do is delete and replace the directory `dex-tools-2.1-SNAPSHOT` with the new version of dex2jar downloaded from [here](https://github.com/pxb1988/dex2jar/releases) and also delete `cfr-0.149.jar` and download the new version from [here](http://www.benf.org/other/cfr/).  

**As a final step you have to update the following two variables accordingly:**
~~~~
name_of_the_DEX2JAR_directory = "dex-tools-2.1-SNAPSHOT"
name_of_the_cfr_jar = "cfr-0.149.jar"
~~~~
