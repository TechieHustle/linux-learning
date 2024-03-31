# Microkernels
- QNX uses microkernels (IPC, Scheduling, Interrupt Dispatch)
# Resource Managers
- Sensors data is collected by device resource manager, and passed to the application resource manager using microkernel's message passing feature.
- We can add resource manager in QNX without worrying about the kernel. Bugs in resource manager cannot affect the kernel.
- Resource managers have their own protected address space.
- Resource managers can be started/stopped dynamically - offering a great flexibility.
- Easy portability to other devices with minimal changes.
- Helps reduce the runtime memory footprint of the system.
  ## Types:
  ### 1. Device Resource Manager
    #### Device Resource Manager Layers:
    1. Thread Pool Layer: Handles thread functionalities like creating, deleting, blocking threads.
    2. Dispatch Layer:
       1. Dispatch Block: Blocks the incoming messages, analyses them and pass them to Dispatch Handler.
       2. Dispatch Handler: Dispatches the messages to the approperiate message handler functions.
    3. Resmgr layer:
       1. Connect Message Layer: If the incoming message is connect message, it calls the Open handler for connection.
       2. Read/Write Message Layer: If the incoming message is read/write, it calls read/write handler.
    4. Iofunc Layer:
       1. Default Functions: Called when no user-defined functions are available to handle the incoming messages.
       2. Helper Functions: Used by users in their codes to handle the incoming messages.
  They all have APIs which can be used to create resource managers.
  ### 2. Filesystem Resource Manager
  
