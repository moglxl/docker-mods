Docer image for compiling motorola Mods firmware(Base on Ubuntu 16.04).



## Windows 10

>1. Get Docker for Windows([Stable](https://download.docker.com/win/stable/InstallDocker.msi) [Edge](https://download.docker.com/win/edge/Docker%20for%20Windows%20Installer.exe)) from [Docker website](https://docs.docker.com/docker-for-windows/install/).
>
>2. Install(remember turn on virtualization tech in BIOS & Hyper-V in OS,Shared Drives in Docker Settings).
>
>3. Search & pull image from [Docker Hub](https://hub.docker.com/explore/), type in cmd window as below:
>
>   ```shell
>   docker pull moglxl/moto-mods:latest
>   ```
>
>4. Run
>
>   ```shell
>   docker run -it -w /home/mods -v <your VOLUME folder>:/data moglxl/moto-mods:latest
>   ```

#### Known Issues:
* repo sync failed with "OSError: [Errno 39] Directory not empty:"?

    It's a bug when call python API to access multi files on NTFS volume:
>1. use 'repo sync -j1' instead;
>2. under Ubuntu,use dd/mkfs.ext4 to create one raw image file with ext4 filesystem,mount it,then do works in mounted folder;
>3. wait for a fix from Docker...... 


* repo sync failed with "GitError("cannot initialize work tree")"?

    Downloaded wrong data caused by network traffic error,use 'repo --trace sync -j1' to find out error respiratory,delete it,sync again.
## Mac

> Just same as above...almost



### *References*

[Docker Documentation](https://docs.docker.com/)

[Docker — 从入门到实践](https://www.gitbook.com/book/yeasy/docker_practice)