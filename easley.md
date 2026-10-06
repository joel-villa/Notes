# Notes on running on Easley

To ssh:

```linux
ssh <user name>@easley.alliance.unm.edu
```

To run a bash script:

```
sbatch <bash file name>.sh
```

Seeing the queue on the debug partition:

```
squeue --partition debug
```

Cancelling a job:

```
scancel <job ID>
```

