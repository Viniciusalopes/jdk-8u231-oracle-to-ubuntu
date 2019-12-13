# AutomaGizar com ShellScrip (Shell-Base)

# Install Oracle JDK 8 on Linux
## Instalar Oracle JDK 8 no Linux/Ubuntu 19.10

__FONTE:__ [Install Oracle JDK 8 on Linux](https://www.javahelps.com/2015/03/install-oracle-jdk-in-ubuntu.html)

__Download:__ [Java SE Development Kit 8 Downloads](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

### Comandos no terminal

__Criar o diretório__ 
```
sudo mkdir /usr/lib/jvm
```

__Extrair para o diretório criado__
```
$ sudo tar -xvzf ~/Downloads/jdk-8u231-linux-x64.tar.gz -C /usr/lib/jvm
```

__Editar o PATH de environment
sudo nano /etc/environment
    ## CONTEÚDO DE '/etc/environment' após a edição
    PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/jvm/jdk1.8.0_231/bin:/usr/lib/jvm/jdk1.8.0_231/db/bin:/usr/lib/jvm/jdk1.8.0_231/jre/bin"
    J2SDKDIR="/usr/lib/jvm/jdk1.8.0_231"
    J2REDIR="/usr/lib/jvm/jdk1.8.0_231/jre"
    JAVA_HOME="/usr/lib/jvm/jdk1.8.0_231"
    DERBY_HOME="/usr/lib/jvm/jdk1.8.0_231/db"
    ## CONTEÚDO DE '/etc/environment' após a edição

# Comandos no terminal:
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_231/bin/java" 0
sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/jdk1.8.0_231/bin/javac" 0
sudo update-alternatives --set java /usr/lib/jvm/jdk1.8.0_231/bin/java
sudo update-alternatives --set javac /usr/lib/jvm/jdk1.8.0_231/bin/javac
update-alternatives --list java
update-alternatives --list javac
java -version
# A saída do comando java -version deve ser:
# java version "1.8.0_231"
# Java(TM) SE Runtime Environment (build 1.8.0_231-b11)
# Java HotSpot(TM) 64-Bit Server VM (build 25.231-b11, mixed mode)

nano ~/netbeans-8.2/etc/netbeans.conf
    # setar netbeans_jdkhome

    #netbeans_jdkhome="/lib/jvm/java-8-openjdk-amd64"
    netbeans_jdkhome="/usr/lib/jvm/jdk1.8.0_231"

# UPDATE VOVOLINUX (2019-11-25)
