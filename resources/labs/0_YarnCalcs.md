```

Value of operating system is adjusted as 0,075 of total memory that is a reasonable value of 9,6 GB.

yarn.scheduler.maximum-allocation-mb is adjusted to 8192 MB.
The node can run 15 container (based on vcore max availability) with 8192 MB without waste of memory, occupying all available memory of Yarn.

mapreduce.map.memory.mb is increased to 2048 to allow for greater memory availability. 
mapreduce.map.java.opts.max.heap is increased as 80% of mapreduce.map.memory.mb.

mapreduce.reduce.memory.mb is increased to 4096 that is twice mapreduce.map.memory.mb to allow for greater memory availability. 
mapreduce.reduce.java.opts.max.heap is increased as 80% of mapreduce.reduce.memory.mb.

yarn.app.mapreduce.am.resource.mb is increased to 2048 to allow for greater memory availability. 
yarn.app.mapreduce.am.resource.command-opts is increased as 80% of yarn.app.mapreduce.am.resource.mb.

Hadoop is a disk I/O-centric platform by design.
The number of independent physical drives (“spindles”) dedicated to DataNode use limits how much concurrent processing a node can sustain.
Workload factor is the workload (cpu work) that disks can sustain.
Increase a workload factor means that the disks can sustain much work therefore a greater number of parallel tasks.
lower value for workload factor limit number of tasks, So if i have 6 disk with load factor of 2 it can sustain 12 tasks.

```