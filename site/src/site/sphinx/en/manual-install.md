Manually Install Arthas
===================

1. Download the latest version

    **Latest version**: [![Arthas](https://img.shields.io/maven-central/v/com.taobao.arthas/arthas-packaging.svg?style=flat-square "Arthas")](http://search.maven.org/classic/#search%7Cga%7C1%7Cg%3A%22com.taobao.arthas%22%20AND%20a%3A%22arthas-packaging%22)

    If the download speed is slow, try to use [Ali cloud mirror repository](https://maven.aliyun.com/), for example, to download version `3.x.x` (you can replace `3.x.x` in the example URL if you want to download other version), the download URL is: https://maven.aliyun.com/repository/public/com/taobao/arthas/arthas-packaging/3.x.x/arthas-packaging-3.x.x-bin.zip

2. Unzip zip file

    ```bash
    unzip arthas-packaging-bin.zip
    ```

3. Install Arthas

    It is recommended to completely remove all old versions of Arthas before installation.

    ```bash
    sudo su admin
    rm -rf /home/admin/.arthas/lib/* # remove all the leftover of the old outdated Arthas
    cd arthas
    ./install-local.sh # switch the user based on the owner of the target Java process.
    ```

4. Start Arthas

    Make sure `shutdown` the old Arthas server before start.

    ```bash
    ./as.sh
    ```
