# **Guía arduino - linux**
***
![Captura de pantalla de Edgar](/portada.png)

## Guía para instalar el IDE de arduino en una máquina con GNU-linux(Distribuciones basadas en debian o ubuntu).
***
Hola como están mi nombre es [Edgar E. Mamani A.](https://www.facebook.com/dEmONeDGEnT) y en esta ocasión voy a mostrarles como instalar el IDE de arduino en **GNU-linux**, para ser más preciso en alguna ***distribución basada en ubuntu o debian***.

1. Bueno lo primero que tenemos q hacer es descargar el software de arduino en nuestra computadora, para ello abrimos nuestro navegador de internet y nos dirigimos a la página oficial de arduino([https://www.arduino.cc/](https://www.arduino.cc/)).

2. Una vez descargado el archivo lo que hacemos es descomprimirlo y borrar el archivo comprimido para posteriormente abrir la terminal:
```edgar@teamOSH:~$```

3. El IDE de arduino necesita java para poder ejecutarse, para ello verificamos si tenemos java instalado con el comando:
```java -version```

4. Si nos muestra la versión de java entonces lo tenemos instalado y podemos continuar con el siguiente paso, caso contrario tenemos que instalarlo:
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

5. Después de instalar java vamos a proceder a la instalación de la última versión de arduino, en mi caso es la versión 1.8.5 ósea la que acabamos de descargar. Cabe recalcar que debemos cambiar las siguientes instrucciones dependiendo de la versión que estemos instalando:
```
sudo mv arduino-1.8.5 /opt
sudo ln -s /opt/arduino-1.8.5 /opt/arduino
cd /opt/arduino
sudo ./install.sh
```

6. Una vez terminado el proceso de instalación es necesario que nuestro usuario tenga permisos para conectarse a la paca arduino a través del puerto USB, para ello tendremos que añadirlo al grupo dialout:
```
sudo adduser USUARIO dialout
```
***
### Y con estas simples instrucciones ya podemos utilizar nuestro arduino para poder programarlo desde nuestro sistema operativo GNU-linux.
