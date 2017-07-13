# Linux Commands

## Operating System
* Print operating system info  
```
uname -a (kernel name, release, version; host name; processor architecture etc)
```
* Check CPU info  
```
cat /proc/cpuinfo 
cat /proc/cpuinfo | grep processor | wc -l (query number of processors or cores)
```



## Networking
* Find port number for a particular process is using  
```
netstat -pl | grep <process_id>
```
* Find process using a particular port number  
```
lsof -i :<port_number>
```
  
