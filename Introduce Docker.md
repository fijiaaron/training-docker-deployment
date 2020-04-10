What is Docker
==============

Tool for running applications in isolated environment

Advantages
----------

1. Consistency: Everything from development to production runs on the same environment
2. Security: Isolate projects to reduce risk
3. Simplicity: Easier to cet started without complex setup and installing dependencies
4. Speed: Docker containers start up in seconds
5. Efficiency: Containers maximize system usage and save cost on hardware


Containers vs Virtual Machines
------------------------------

They are similar in that that provide isolation and share hardware.

Containers have less overhead


### VM ###

	App
	Libraries & Tools
	Kernel
	- - -
	Hypervisor
	Host OS
	Machine


### Container ###

	App
	Libraries & Tools
	- - - 
	Host OS with Kernel
	Machine


