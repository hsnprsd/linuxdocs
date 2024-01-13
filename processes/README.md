# TOC
- [nice](#nice)

# nice
nice - change process priority

As a simple example, when two otherwise identical CPU-bound processes are running simultaneously on a single-CPU Linux system, each one's share of the CPU time will be proportional to `20 − p`, where `p` is the process' priority.

The __range of the nice value__ is __+19 (low priority)__ to __-20 (high priority)__.  Attempts to set a nice value outside the range are clamped to the range.

The default niceness for processes is inherited from its parent process and is usually 0.

Only the superuser (`root`) may set the niceness to a lower value (i.e. a higher priority).

The related `renice` program can be used to change the priority of a process that is already running.

## Examples
nice:
```
sudo nice -n -20 python3 main.py    # high prio
sudo nice -n 19  python3 main.py    # low  prio
```

renice:
```
renice -n <inc> -p <pid>
```
