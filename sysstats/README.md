# mpstat
Report processor related statistics.
## Example Usage:
```
mpstat 1
```
## Notes
### iowait?
Show the percentage of time that the CPU or CPUs were idle during which the system had an outstanding disk I/O request.

IOWait is important because it often is a key metric to know if you're bottlenecked on IO. But absense of iowait does not necessarily mean your application is not bottlenecked on IO. Consider two applications running on a system. If program 1 is heavily io bottlenecked and program 2 is a heavy CPU user, the `%user + %system` of CPU may still be something like ~100% and correspondingly, iowait would show 0. But that's just because program 2 is intensive and relatively appear to say nothing about program 1 because all this is from the CPU's point of view.
### irq?
Show the percentage of time spent by the CPU or CPUs to service __hardware interrupts__.
### soft?
Show the percentage of time spent by the CPU or CPUs to service __software interrupts__.
### guest?
Show the percentage of time spent by the CPU or CPUs to run a virtual processor. This will only show if the machine itself is a hypervisor - the amount of time spent serving virtual machines.

# vmstat
Report virtual memory statistics.
## Example Usage:
```
vmstat -S M 1

-S: unit (MB)
```
## Notes
### buffer vs cache
- buffer = internal OS buffers used during disk I/O
- cache  = disk page cache
