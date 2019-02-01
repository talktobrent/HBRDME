# HBRDME
README generator for Holberton School projects
### Requirements
- ```apt-get install grip```
### How it works
Generates HTML based README from raw Holberton project html files
- Save raw html project pages into a ```projects/``` child directory of the root direcoty of HBRDME
- Run ```./HBRDME [OPTIONS]```
- Projects are parsed and the default browser is launched to confirm generation (unless `-blind` option added)
- Successful html project paths are saved in the local file: ```passed```
- Files logged in ```passed``` are skipped in future iterations, unless `-force` option is chosen, or ```passed``` is edited or deleted
- READMEs are saved in a child tree of the HBRDME location: ```<REPO>/<DIRECTORY>```, which corresponds with Github locations of each parsed project
- Upon, completion, total number of successful projects is printed, as well as the total number of failed projects
### Options
- ```-b``` ```-blind```: Run without launching browser to verify README content
- ```-f``` ```-force```: Force parsing of all projects saved in ```projects/``` (Existing READMEs will be overwritten)
- ```-h``` ```-help```: Print help
### Pending features:
- Github integration
- Style options
