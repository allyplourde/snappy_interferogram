# snappy_interferogram
creating interferograms using SNAP's Python API

The following program automates the processing of creating an interferogram in ESA's image processing tool SNAP. It has been tested for Sentinel-1 imagery. 

It is recommended that the user has Anaconda installed on their machine. The .yml file should be used to create a conda environment. If you are running Windows 10, these steps can be used to configure snappy to this conda environment. 

If this is the first time configuring snappy, complete all steps.
If you have already configured snappy on your account and know the
directory found in step 4, proceed to step 5.

1. In the "Anaconda Prompt" run:

		conda activate SigLib
	
2. Search for the SNAP command-line desktop app and open it

3. In the SNAP command-line app run:

		snappy-conf your\path\to\conda\env\python
	
4. Look for a directory similar to the one below in the output:

	""The SNAP-Python interface is located in 'C:\Path\to\snappy\.snap\snap-python\snappy'""

5. In the anaconda prompt, set the PYTHONPATH variable with the following cmd

		set PYTHONPATH=<your\path\to\conda\env\python>
	
6. In the anaconda prompt, add snappy to the python path variable pointing it to 
   the directory found in step 4:

		set PYTHONPATH=%PYTHONPATH%;<C:\Path\to\snappy\.snap\snap-python\snappy>
		
7. Verify the path has been added with the command:
		python -m site
		
8. Verify snappy is working by opening up python in the command line
   and running
   
		from snappy import ProductIO
   
   if no error results, you have successfully confirgured your environment to run snappy!
