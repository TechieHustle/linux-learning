# Virtual Machine running an OS
- To find out if running linux machine is virtual, use command `less   /proc/cpuinfo` and look for `hypervisor` flag.
- If a machine is capable of having other guest OSs, the `less /proc/cpuinfo` command will have flags with `vmx` (intel CPU) or `svm` (AMD CPUs).\\
  NOTE: WSL is type-1 hypervisor, and it has the `vmx`/`svm` flags.
### Creation of VMs can be done using any one of the following ways:
- `kvm`/`kvm-amd` handles the hypervisation inside Linux kernel.
- VMs can be created using a CD, cloning another VM, using OVF format files(can contain VM image, configuration files etc.). We can combine multiple files in OVF to create an archive using OVA.
- Templates - they are like cloning with the maching having specific kind of configurations for some use cases, for example a web server template. \\
  Downside of templates is that they copy all the information from the source OS to the template. Examples include UUID, UID, MAC Addresses of NIC etc.
