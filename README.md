# check_horizonview

I have recently started writing a collection of Nagios checks to monitor Horizon View to flag issues that need investigating. More in-depth monitoring can be done via vRealise. I am planning to add/remove/combine these checks as time goes on. The scripts are designed to used with NRPE/NSclient++ on a Windows host.

**Current Version:** Release v1.3

Checks:

 * check_horizonview_sessions.ps1 - checks the amount of sessions in a connected or disconnected state. (outputs perf data)
 * check_horizonview_provisioning_error.ps1 - checks for machines in a provisioning_error state.
 * check_horizonview_agent_unreachable.ps1 - checks for machines in a agent_unreachable state.

Use Powershell Get-Help for more detail on how to use each script.

## Script Dependencies

The Powershell scripts require the PowerCLI 6.5 R1 and Hv.Helper to be installed.

[VMware blog](https://blogs.vmware.com/euc/2017/01/vmware-horizon-7-powercli-6-5.html)

[Hv.Helper Github](https://github.com/vmware/PowerCLI-Example-Scripts)

## How it Works with Nagios Core

Nagios Core --> NRPE/NSClient++ --> Horizon View API

I plan to do a full guide on how to setup these checks in the furture.

## Release Notes

v1.0 - Initial version

v1.1 - Added per pool session count to perfdata string

v1.2 - The perfdata string now includes pools with zero sessions

v1.3 - Change perfdata delimiter to a space

## Contribute/Feature Requests

I am always happy to recieve feedback good or bad. I plan to improve and expand on these checks.

Drop me a line if you find a bug or want a feature adding to an existing check or have an idea for an addtional check.

Feel free to message me if you need help getting the checks working in your environment. 

https://github.com/tschubb/check_horizonview