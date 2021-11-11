## deepin 代理

### 安装electron-ssr

- [github地址](https://github.com/shadowsocksrr/electron-ssr)，下载deb包（deepin基于Debian）

- 操作步骤

  - 系统需要安装Python，建议使用[pyenv](https://github.com/pyenv/pyenv)管理多版本

  - 安装依赖

    ```shell
    sudo apt install libcanberra-gtk-module libcanberra-gtk3-module gconf2 gconf-service libappindicator1
    sudo apt-get install libssl-dev
    sudo apt-get install libsodium-dev
    ```

- 启动，终端输入

  ```shell
  electron-ssr
  ```

- 出现小飞机，设置订阅地址，确认订阅地址是否更新

### 设置命令行代理

- 查看端口情况

  ![image-20211110171225764](/home/houxl/.config/Typora/typora-user-images/image-20211110171225764.png)

- 设置环境变量

  ```shell
  echo 'alias setproxy="export ALL_PROXY=socks5://127.0.0.1:1080"' >> ~/.bashrc
  echo 'alias unsetproxy="unset ALL_PROXY"' >> ~/.bashrc
  ```

- 启动终端代理
  - setproxy
- 关闭终端代理
  - unsetproxy