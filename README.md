This is my latest Ansible code for blibli.com future program batch 4 phase 2. I integrated all the services in this code using Jenkins (as a CI/CD tool), which is a multibranch pipeline.

Initially, I tried it at https://github.com/yohannafrans/ansible to install each part needed by the virtual machine one by one. But when I try to run it on Jenkins, my Ghost service doesn't work because it conflicts with a virtual machine.

Finally, I made this new file by combining the installation of each service in one file, and everything went smoothly. For code that only uses a docker container, you can check it at https://github.com/yohannafrans/secondphasefinalproject.git. Even in this code, it can install the coding from that container.

--- Take a look and understand more deeply. Cheers! ---
