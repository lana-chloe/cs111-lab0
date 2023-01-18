# A Kernel Seedling

Kernel module that creates a /proc/count file that shows the current number of running processes or tasks running.

## Building

Run the following commands to build and load the kernel module:
    
    make
    sudo insmod proc_count.ko

To check if the module was loaded correctly:

    lsmod // this should list out all the loaded modules, so you should be able to see proc_count in that list

## Running

After loading the kernel module, the command

    cat /proc/count

outputs an integer that represents the current number of running processes or tasks running.

## Cleaning Up

To remove the kernel module and clean up the code before loading the newly compiled module, run the following command:

    sudo rmmod proc_count

Then follow the previous steps ot load it back in.

## Testing

The kernel release version the module was tested on is 5.14.8-arch1-1.