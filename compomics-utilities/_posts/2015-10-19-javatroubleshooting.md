---
name: JavaTroubleShooting
project: compomics-utilities
layout: default
permalink: /compomics-utilities/wiki/javatroubleshooting.html
github_project: https://github.com/compomics/compomics-utilities
---

# Java Troubleshooting #

The aim of this page is to provide help with common Java related issues that one can encounter when using software from the CompOmics group. If you have a Java related question that is not answered below please let us know.

## Installing Java ##

  * Do you have Java installed? Download the latest version of Java  [here](http://java.sun.com/javase/downloads/index.jsp). (You only need the JRE version (and not the JDK version) to run CompOmics tools.) [64 bit is always recommended!](#32-bit-vs-64-bit)

---

## Memory Issues ##

  * **Memory Issues I** - Big datasets can require a lot of memory. If the software fails on a big project, and the software mentions that it ran out of memory, try to give the program more memory. This can be done by selecting `Java Options` on the `Edit` menu in most tools. Set the memory limit in MB, e.g., `4000` for a maximum of appr. 4 GB of memory. _Please note that on a 32-bit operating system you cannot increase this value beyond 2000 (and usually the maximum limit is lower than this)._

  * **Memory Issues II** - Using more than 2 GB of memory requires 64 bit Java. Downloaded from the same location as the 32 bit version: [Java](http://java.sun.com/javase/downloads/index.jsp). _Note that 64 bit Java only works on 64 bit operating systems!_

---

## 32 bit vs 64 bit ##

  * **Java 32 bit vs 64 bit** - Java comes in two versions: 32 bit and 64 bit. The 32 bit version is limited to using a maximum of around 2 GB of memory. For bigger datasets this is not always enough. Most newer machines support the 64 bit version, and it is always recommended to use Java 64 bit if possible.

  * **Multiple Installations** - If you have both 32 and 64 bit versions of Java the operating system can get confused about which version to use when running Java tools. For Windows the CompOmics tools try to default to the 64 bit version of Java. You can override this option by setting your own Java Home, by creating a file called `JavaHome.txt` in the `resources\conf` folder of the tool, with the path to the bin folder of the Java installation, e.g., `C:\Program Files\Java\jdk1.7.0_21\bin\`. If the folder does not exist (or it does not contain the required files), the default Java version will be used.

---

## Tool Does Not Start ##

  * **Does Not Start I** - Do you have Java installed? Download the latest version of Java  [here](http://java.sun.com/javase/downloads/index.jsp) and try again. (You only need the JRE version (and not the JDK version) to run CompOmics tools.) [64 bit is always recommended!](#32-bit-vs-64-bit)

  * **Does Not Start II** - Have you unzipped the zip file? You need to unzip the file before double clicking the jar file. If you get the message "A Java Exception has occurred", you are most likely trying to run the tool from within the zip file. Unzip the file and try again.

  * **Does Not Start III** - Is the tool installed in a path containing special characters, i.e. `[`, `%`, æ, ø, å, etc? If so, move the whole folder to a different location or rename the folder(s) causing the problem and try again. (Note that on Linux, most tools have to be run from paths not containing spaces as well).

  * **Does Not Start IV** - If the tool fails during start-up many of our tools generate a file called `startup.log` in the tool's `resources\conf` folder. Here you can find detailed information about why the program was not able to start.

  * **Unidentified Developer** - If you run Java applications on a Mac you can get the warning _"Application" can't be opened because it is from an unidentified developer_. To escape this warning control-click on the file icon and then select "Open." This will give you the option of opening it regardless of its unidentified source. This only has to be done once for each version of the application.

---

## Need More Help? ##

  * **Problem Not Solved? Or Problem Not In List?** Contact the developers by setting up an issue describing the problem at the given tool's web page (available via the Issues tab).