
* INFO:
  http://ihfoam.ihcantabria.com/
  infoam@ihcantabria.com

* COMPILE THE CODE:
Enter the folder "code/":
- copy "multiphaseMangrovesSource" and "multiphaseMangrovesTurbulenceModel" into src/fvOptions/.
- modify fvOptions/Make/files by adding (before the last line):
        multiphaseMangrovesSource/multiphaseMangrovesSource.C
        multiphaseMangrovesTurbulenceModel/multiphaseMangrovesTurbulenceModel.C
- recompile (with command "wmake").


* TEST TUTORIAL:
Load OpenFOAM bashrc and enter the folder "tutorial/":
- create mesh:
	$ blockMesh
- set variables:
	$ setFields
	$ topoSet
- decompose domain:
	$ decomposePar
- execute in parallel:
	$ mpirun -np 2 interFoam -parallel

