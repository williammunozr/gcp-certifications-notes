# Exam Essentials

## Compute with Compute Engine Virtual Machines

- **Understand how to use Cloud Console and Cloud SDK to create, start, and stop VMs.** Parameters that you would need to provide when creating a MV include name, machine type, region, zone, and boot disk. Understand the need to create a VM in a project.
- **Know how to configure a spot VM using Cloud Console and the gcloud commands.** Know when to use a spot VM and when not to. Know that spot VMs cost up to 80 percent less than standard VMs.

## Chapter 6 - Managing Virtual Machines

- `Understand how to navigate Cloud Console`. Cloud Console is the graphical interface for working with Google Cloud. You can create, configure, delete, and list VM instances from the Compute Engine area of the console.
- `Unserstand how to install Cloud SDK`. Cloud SDK allow you to configure default environment variables, such as a preferred zone, and issue commands from the command line. If you use Cloud Shell, Cloud SDK is already installed.
- `Know houw to create a VM in the console and at the command line.` You can specify machine type, choose an image, and configure disks with the console. You can use commands at the command line to list and describe, and you can find the same information in the console. Understand when to use customized images and how to deprecate them. Images are copies of content of a disk, and they are used to create VMs. Deprecated marks an image as no longer supported.
- `Understand why GPUs are used and how to attach them to a VM.` GPUs are used for compute-intensive operations; a common use case for using GPUs is machine learning. It is best to use an image that has GPU libraries installed. Understand how to determine which locations have GPUs available, because there are some restrictions. The CPU must be compatible with the GPU selected, and GPUs cannot be attached to shared memory machines. Know how GPU costs are charged.
- `Understand images and snapshots.` Snapshots save the contents of disks for backup and data-sharing purposes. Images save the operating system and related configurations so that you can create identical copies of the instance.
- `Understand instance groups and instance group templates.` Instance groups are sets of instances managed as a single entity. Instance group templates specify the configuration of an instance group and the instances in it. Managed instance groups support autoscaling and load balancing.

