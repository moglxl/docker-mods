Docer image for compiling motorola Mods firmware(Base on Ubuntu 16.04).



## Windows

>1. Get Docker for Windows([Stable](https://download.docker.com/win/stable/InstallDocker.msi) [Edge](https://download.docker.com/win/edge/Docker%20for%20Windows%20Installer.exe)) from [Docker website](https://docs.docker.com/docker-for-windows/install/).
>
>2. Install
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

## Mac

> Just same as above...



### *References*

[Docker Documentation](https://yeasy.gitbooks.io/docker_practice/content/)

[Docker — 从入门到实践](https://www.gitbook.com/book/yeasy/docker_practice)