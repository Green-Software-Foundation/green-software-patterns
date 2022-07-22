# Rightsizing oversized VMs

## Version
1.0

## Submitted By
Bill Johnson

## Published Date
TBD

## Intent

Choose servers that are the right size for the task at hand.

## Tags
Cloud, Compute, Cloud Engineer, Small

## Problem

It's better to have one VM running at a higher utilization than two running at low utilization rates. This is both from an energy proportionality angle. 2 servers running at low utilization rates will consume more energy than one server running at a high rate of utilization. But also, from an embodied carbon angle, the unused capacity on the underutilized server could be more efficiently used for another task or process.

## Solution

Change the number of resources allocated to a VM to match the utilization requirements of the VM. For example, adding a vCPU if the VM is running high CPU utilization or removing memory if the server is not using all of its allocated memory.

Select a pre-configured server that better matches the utilization requirements of the process.

## SCI Impact

`SCI = (E * I) + M per R`

With respect to the SCI equation. Rightsizing oversized VMs will impact two parts:

- `M`: By reducing the total number of servers required to run a process, we reduce the total embodied carbon, the `M` of the equation.
- `E`: Rightsizing oversized VMs will **increase** the total server utilization. The more a server is utilized, the more efficient it becomes at turning energy into useful operations, as per the [energy proportionality](https://principles.green/principles/energy-proportionality/) principle. Therefore rightsizing VMs should reduce the energy consumption of your processes, and consequently, the `E` number should decrease.

## Assumptions

If we chose an oversized VM because *occasionally* there is a burst of work, a peak load, then undersizing them will reduce the headroom available to handle the peak traffic. A better solution would be to consider an auto-scaling architecture that would automatically scale the number of VM.

## Pros & Cons

- **PRO**: It may reduce your cloud bill as reducing the spec of your VMs will cost less.
- **CON**: If you do not have an auto-scaling architecture, there is less overhead for handling spikes in load.
