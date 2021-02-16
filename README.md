# ASPLOS 2021 Artifacts

These are the artifacts for the ASPLOS 2021 paper: [Rethinking Software Runtimes for Disaggregated Memory](https://asplos-conference.org/abstracts/asplos21-paper210-extended_abstract.pdf).

## Instructions  
These instructions have been tested on a clean Ubuntu 20.04 installation running on a CloudLab C6420 machine.  
Make sure you run everything on a bare-metal Linux server, that you have sudo access and at least 128 GB RAM and 100 GB free storage space for application datasets and logs.  
It is best to launch everything inside a screen session.

Clone the repository and submodules
```
git clone --recurse-submodules https://github.com/project-kona/asplos21-ae.git  
cd asplos21-ae
```

### Applications  

Set up applications and download data sets. To do so, run the following from the asplos21-ae folder:
```
cd apps/scripts
./setup.sh
```

### KTracker 

Run all applications and produce the KTracker data. To do so, run the following from the asplos21-ae folder: 
```
cd KTracker/scripts  
./run_all.sh  
```

All output data and plots will be generated in the `results` directory.  
For each run, a new directory is created `res_<date>`.   
The generated plots are in a `plots` directory, under this `res_<date>` directory (redis\_amplif.pdf and results\_wp.pdf).  

### KCacheSim 

Refer to instructions in [KCacheSim](https://github.com/project-kona/KCacheSim) repository.
