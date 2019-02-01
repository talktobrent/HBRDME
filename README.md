# HBRDME
README generator for Holberton School projects
### Requirements
- ```apt-get install grip```
### How it works
Generates HTML based README from raw Holberton project html files
- Save raw html project pages into a ```projects/``` child directory of the root direcoty of HBRDME
- Run ```./HBRDME [OPTIONS]```
- Projects are parsed. Via Grip, The default browser is launched for each project to confirm generation (unless `-blind` option added). After terminating Grip (CTRL-C), the user is prompted Y/N if README was good. A [Nn] response will ignore saving, and proceed to next project. Any other response, and the the README is saved.
- Successful html project paths are saved in the local file: ```passed```
- Files logged in ```passed``` are skipped in future iterations, unless `-force` option is chosen, or ```passed``` is edited or deleted
- READMEs are saved in a child tree from the user HOME location: ```$HOME/<REPO>/<DIRECTORY>```, which corresponds with Github locations of each parsed project
- Upon, completion, total number of successful projects is printed, as well as the total number of failed projects
### Options
- ```-b``` ```-blind```: Run without launching browser and prompting to verify README content
- ```-f``` ```-force```: Force parsing of all projects saved in ```projects/``` (Existing READMEs will be overwritten)
- ```-h``` ```-help```: Print help
### Pending features:
- Github integration
- Style options
