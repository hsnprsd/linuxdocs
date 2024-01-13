# mpstat
Report processor related statistics.
## Example Usage:
```
mpstat 1
```
## Notes
### What is iowait?
IOWait is important because it often is a key metric to know if you're bottlenecked on IO. But absense of iowait does not necessarily mean your application is not bottlenecked on IO. Consider two applications running on a system. If program 1 is heavily io bottlenecked and program 2 is a heavy CPU user, the `%user + %system` of CPU may still be something like ~100% and correspondingly, iowait would show 0. But that's just because program 2 is intensive and relatively appear to say nothing about program 1 because all this is from the CPU's point of view.


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


# iostat
Report (disk) I/O statistics.
## Example Usage:
```
iostat -d -c -x -h 1

-d: disk stats
-c: cpu stats
-x: extended
-h: human readable
```
## Notes
_Empty_

# netstat
_Empty_
