# PID notes  

Working with processes is a really common task, so evaluate their performance, close, manage them and ultimately understanding them is really important and useful.  

## What PID means?  
A **Process ID** (PID) is a numerical unique identifies of an instance of a running program. The kernel assigns an identifier sequentially. This is useful for system operations to specific processes, terminating them or monitoring their performance.  

## ps  
Displays information about a selection of the active processes, it is installed by default in bash.  
> ps -Flww -p THE\_PID  
> watch ps -m  (to execute it every two seconds)  

## pidstat  
Is a command that show additional stats like time spent in user mode or the occupation of the CPU.  
It is installed by default in debian.  
> pidstat  
With **-d** flag to add details:  
> pidstat -p 51648 -d  
Integers can be added to make the command refresh each **n** seconds, it stakes as a table:  
> pidstat -p 51648 -d 1  

## px  
Described in apt packages as **ps and top for human beings**, needs to be installed.  
> px  

## References  
* Abdull; Statox and Diesch (2016). AskUbuntu. *How to see a detailed information about a given PID?*.  
    * <https://askubuntu.com/questions/831513/how-to-see-detailed-information-about-a-given-pid>  

