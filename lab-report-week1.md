# Lab Report Week 1
=======
## cd
-------
With no arguments:

If the directory was not changed, i.e. one is still in the default directory, nothing happens. Leaving it blank means cd changes directory to home, which would be the default directory.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/b74ba093-93d6-49df-836c-d3fc904e532e)

If cd was already used with another directory (in this cace lecture1), cd without arguments returns directory to home:

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/c6f5ecb7-3f2a-44a2-b229-d41f5017dcd7)

WIth directory as argument:

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/b3257877-b396-4e56-84d6-66826a80c395)

The directory is changed to the specified directory.

With file as argument:

Error message since directory is required.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/0eb9fdff-94ff-4428-8efb-f1987ff4f29b)

## ls
-------

All code from here on out has the default directory. 


With no arguments:

The contents of the current set directory is listed.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/bac59a9d-76f0-4a88-b97a-c9eb5cc406fc)

With directory as argument:

The contents of the specified directory is listed.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/530a6a9c-edf3-4589-8fb8-ad26d54c3514)

With file as argument:

The path of the specified file is listed.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/59b89d34-172b-48ee-87a9-d897dc43f687)

## cat
-------
With no arguments:

The terminal becomes bugged as cat is meant to print. It is not possible to enter more commands. Pressing CTRL-C fixes the terminal.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/f2c1367a-faf7-453d-a8a9-386f40a91d1b)

With directory as argument:

A message confirming that it is a drectory appears, since nothing can be printed.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/b77d2f57-3aca-4ae5-89d4-b396c84db5ae)

With file as argument:

THe content of the file is printed.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/b7363bee-4b81-451a-9252-3e632eb67143)

The contents of the file are printed. 
