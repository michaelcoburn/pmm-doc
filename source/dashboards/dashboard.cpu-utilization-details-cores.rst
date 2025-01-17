.. _dashboard.cpu-utilization-details-cores:

CPU Utilization Details (Cores)
================================================================================

.. contents::
   :local:

.. _dashboard.cpu-utilization-details-cores.overall:

Overall CPU Utilization
--------------------------------------------------------------------------------

The Overall CPU Utilization metric shows how much of the overall CPU
time is used by the server. It has 4 components:

- system
- user
- iowait
- softirq

In addition, sampling of the Max utilization of a single
core is shown.

System
	    
   This component the proportion of time the CPUs spent inside the Linux kernel
   for operations like context switching, memory allocation and queue handling.

User

   This component is the time spent in the user space.  Normally, most of the
   MySQL CPU time is in user space. A high value of user time indicates a CPU
   bound workload.

Iowait

   This component is the time the CPU spent waiting for disk IO requests to
   complete.  A high value of iowait indicates a disk bound load.

Softirq

   This component is the portion of time the CPU spent servicing software
   interrupts generated by the device drivers.  A high value of softirq may
   indicates a poorly configured device.  The network devices are generally the
   main source of high softirq values.

Be aware that this metric presents global values: while there may be a
lot of unused CPU, a single core may be saturated.  Look at the Max
Core Utilization to see if any core is reaching close to 100%.

.. _dashboard.cpu-utilization-details-cores.current:

Current CPU Core Utilization
--------------------------------------------------------------------------------

The Current CPU Core Utilization metric shows the total utilization of each CPU
core along with the average utilization of all CPU cores.  Watch for any core
close to 100% utilization and investigate the root cause.

|view-all-metrics| |this-dashboard|

.. _dashboard.cpu-utilization-details-cores.all-total:

All Cores - Total
--------------------------------------------------------------------------------

The All Cores - total graph shows the average distribution of all the CPU times.
It has 5 components:

- system
- user
- iowait
- steal
- other

.. rubric:: Components

System

   This component is the proportion of time the CPUs spent inside the Linux
   kernel for operations like context switching, memory allocation and queue
   handling.

User

   This component is the time spent in the user space.  Normally, most of the
   MySQL CPU time is in user space. A high value of user time indicates a CPU
   bound workload.

Iowait

   This component is the time the CPU spent waiting for disk IO requests to
   complete.  A high value of iowait indicates a disk bound load. Steal is non
   zero only in a virtual environment.

Steal

   When multiple virtual machines share the same physical host, some virtual
   machines may be allowed to use more of their share of CPU and that CPU time
   is accounted as Steal by the virtual machine from which the time is taken.

Other

   This component is essentially the softirq time which is the portion of time
   the CPU spent servicing software interrupts generated by the device drivers.
   A high value of softirq may indicates a poorly configured device.  The
   network devices are generally the main source of high softirq values.

Be aware that this metric presents global values: while there may be a lot of
unused CPU, a single core may be saturated.

|view-all-metrics| |this-dashboard|

.. |this-dashboard| replace:: :ref:`dashboard.cpu-utilization-details-cores`

.. include:: ../.res/replace.txt

	     
