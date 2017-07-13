# Linux Commands

## Operating System
* Print operating system info  
```
uname -a (kernel name, release, version; host name; processor architecture etc)
```
* Check CPU info  
	* cat /proc/cpuinfo
	```
	cat /proc/cpuinfo
	cat /proc/cpuinfo | grep processor | wc -l (query number of processors or cores)  
	cat /proc/cpuinfo | grep 'clflush size' (query cache line size)
	```
	
	> Each processor or core is listed seperately, the number of processors shown by /proc/cpuinfo
	> might not be the actual number of cores on the processor. For example a processor with 2 cores
	> and hyperthreading would be reported as a processor with 4 cores.
			
	* lscpu
	> lscpu gathers CPU architecture information from sysfs and /proc/cpuinfo and display in a user
	> friendly format
		
	* nproc (print the number of processing units available)


## Networking
* Find port number for a particular process is using  
```
netstat -pl | grep <process_id>
```
* Find process using a particular port number  
```
lsof -i :<port_number>
```
  
