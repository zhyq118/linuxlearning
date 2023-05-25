# ubuntu安装docker和portainer

## ubuntu安装docker

官方文档[在此]([Install Docker Engine on Ubuntu | Docker Documentation](https://docs.docker.com/engine/install/ubuntu/))

### Set up the repository

1. Update the `apt` package index and install packages to allow `apt` to use a repository over HTTPS:
   
   ```
   $ sudo apt-get update
   $ sudo apt-get install ca-certificates curl gnupg
   ```

2. Add Docker’s official GPG key:
   
   ```
   $ sudo install -m 0755 -d /etc/apt/keyrings
   $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
   $ sudo chmod a+r /etc/apt/keyrings/docker.gpg
   ```

3. Use the following command to set up the repository:
   
   ```
   $ echo \
    "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```
   
   > **Note**
   > 
   > If you use an Ubuntu derivative distro, such as Linux Mint, you may need to use `UBUNTU_CODENAME` instead of `VERSION_CODENAME`.

### Install Docker Engine

1. Update the `apt` package index:
   
   ```
   $ sudo apt-get update
   ```

2. Install Docker Engine, containerd, and Docker Compose.
   
   - Latest
   - Specific version

  To install the latest version, run:

```
 $ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

  ---

3. Verify that the Docker Engine installation is successful by running the `hello-world` image.
   
   ```
   $ sudo docker run hello-world
   ```
   
   This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.

You have now successfully installed and started Docker Engine.



### ## 解决“Got permission denied while trying to connect to the Docker daemon socket at unix“问题

出现此问题说明当前用户没有权限，官方解决方案[在此]([Linux post-installation steps for Docker Engine | Docker Documentation](https://docs.docker.com/engine/install/linux-postinstall/))



To create the `docker` group and add your user:

1. Create the `docker` group.
   
   ```
   $ sudo groupadd docker
   ```

2. Add your user to the `docker` group.
   
   ```
   $ sudo usermod -aG docker $USER
   ```

3. Log out and log back in so that your group membership is re-evaluated.
   
   > If you’re running Linux in a virtual machine, it may be necessary to restart the virtual machine for changes to take effect.
   
   You can also run the following command to activate the changes to groups:
   
   ```
   $ newgrp docker
   ```

4. restart docker service
   
   ```
   $ sudo systemctl restart docker
   ```
   
   

## 安装运行Portainer



```shell
docker run -d -p 9000:9000 -p 8000:8000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /home/username/portainer/data:/data portainer/portainer
```

以上面的配置为例，直接打开本地的`9000`端口地址就可以进入管理后台。

- [http://localhost:9000](http://localhost:9000/)




