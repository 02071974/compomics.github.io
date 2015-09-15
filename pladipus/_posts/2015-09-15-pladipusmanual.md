---
name: PladipusManual
project: pladipus
layout: default
permalink: /pladipus/wiki/pladipusmanual.html
github_project: https://github.com/compomics/pladipus
---

# Manual

The Pladipus software can be run in two modes:

* Management mode, which launches as a graphical user interface that allows for the easy management of data
* Execution mode, which executes and draws jobs from the queue

----

## Management mode

### Login screen

The login screen will query you for your Pladipus user and password (can be generated upon installing the software)

![alt text](https://github.com/compomics/pladipus/wiki/Pladipus_login.png)

### Main GUI

Users can oversee the proceedings of runs and their jobs. A status update is posted by the executing workers to the controller and these can be viewed through the user interface.

By right clicking the selected runs, the user is provided with an option to either start a run, cancel a run (withdraw it from Pladipus) or delete the run.

Similarly, when selected jobs are right clicked, the user can start/cancel and even modify those individual jobs.

![alt text](https://github.com/compomics/pladipus/wiki/Pladipus_main.png)

### Run Creation

A run can be created in two ways:

1. by creating a run template in the GUI (File > Create Run)
2. by importing an existing run template as an XML (File > Create Run)

### Creating a run template using the GUI

The user can create a run template by starting the Run Creation dialog. A preview of the XML file is then displayed to the right. 

![alt text](https://github.com/compomics/pladipus/wiki/Run_Creation_GUI.png)

There are several options:

* A unique run name should be specified. Use the slider to set the priority of the run. This is especially useful to create background tasks.
* Several presets are included in the Pladipus build, making it fairly easy to cobble together powerful processing pipelines. Click "Set" after selecting the preset in order to update the preview!
* The template can be expanded with other steps and the order can be changed by clicking the up/down arrows

![alt text](https://github.com/compomics/pladipus/wiki/Run_Creation_Window_presets.png)

* The default process step parameters are automatically loaded in. More can be added, a useful feature for custom processes.

Important to note is the "Run" field of the parameter table. This checkbox indicates whether the variable should be used across the entire run.

Example: a fasta would be used for every job in the run, so it is a **fixed** parameter, whereas the input file is different for every search, making it a **variable** parameter

![alt text](https://github.com/compomics/pladipus/wiki/Run_Creation_Window_parameters.png)

* Machine preferences can be set for this run by clicking the "Preferences" tab at the top of the window. By selecting these prerequisites, the worker will first scan if it is capable of running the given job. If it is incapable, the job gets rolled back to the queue, not increasing the failcount.
These preferences include the operating system, architecture (32 or 64 bit), the amount of usable memory (RAM), the amount of processing cores for multi-threading  and the amount of available disk space.

Example: a search is requested using Andromeda, which is not available for Linux systems. Should a non-windows worker receive this job, it will detect that it is not able to fully run the job, passing it back to the controller

![alt text](https://github.com/compomics/pladipus/wiki/Run_Creation_Window_preferences.png)

* After clicking "create" an XML file is generated for future use, along with an empty configuration file. The latter is a TSV file Every column represents a parameter, where each row will form a job. An example is available [here](/pladipus/wiki/example-configuration.html)

### Populating a run

* Jobs can be added to processes through the processes section of the main GUI after selecting a run. This is not recommended to create larger runs, as the jobs are created one by one this way.
This functionality is only intended to add a new process to a run. A dialog appears by clicking the + sign, allowing the user to provide parameters for the new job.
 
![alt text](https://github.com/compomics/pladipus/wiki/Job_Creation_Dialog.png)

* It is however possible to batch insert jobs by importing a configuration file (see the run creation section). These files can be imported by either selecting File > Import from the job creation dialog.

* Another option is to load a template XML file and a configuration file simultanuously in order to instantly set up a run and jobs. This can be done by clicking File > Import in the main GUI screen

----

## Admin console

The GUI also comes with an admin console if the user possesses the right privileges (admin rights). This console can be used to:

* Create and delete new users
* Change user privileges
* Manage user runs/processes
* Broadcast system wide operations

![alt text](https://github.com/compomics/pladipus/wiki/Administration_Console.png)

----

## Execution mode

* The execution mode is command line only and has several switches

### Drawing jobs from the queue
  
To pull a single task: `java -jar Pladipus-execution-X.Y.Z.jar -pull`

To pull tasks continuously: `java -jar Pladipus-execution-X.Y.Z.jar -auto_pull`

----

### Posting jobs to the queue

`java -jar Pladipus-execution-X.Y.Z.jar -push -template [template.xml] -job_config [config.tsv] -u [username] -p [password]`