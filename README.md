# GEANT4-INSTALATION-GUIDE
HOW TO


https://www.youtube.com/watch?v=Lxb4WZyKeCE&t=2s

https://www.youtube.com/watch?v=UyXFBP-dVHI

**Instalation in Windows 11 (WSL2 Ubuntu)** 

Unzip source code

$ tar xzfv geant4-v11.3.0.tar.gz

Libraries (Pre-Requirements)

$ sudo apt install -y cmake cmake-curses-gui gcc g++ libexpat1-dev libxmu-dev libmotif-dev  libqt5opengl5-dev

Install QT5 (User Interface Library - GUI)

$ sudo apt install -y qtcreator qtbase5-dev qt5-qmake cmake

Create for to compile the binaries

$ mkdir build 

$ cd build 

$ sudo ccmake ..

1. **Press key [c] to configure**
    1. add geant4-v11.3.0**-install** to instalation folder (To not all files stay in same root folder)
    
    ADD CMAKE_ISNTALL_PREFIX your folder /home/clayton/Geant4/geant4-v11.3.0-install/
    
2. **Press key [g] to configure**

![image.png](attachment:a344e571-726a-4711-bd33-7059443af78b:image.png)

![image.png](attachment:e5c6b380-c1ae-411a-9f57-42f824fccbcc:image.png)

![image.png](attachment:9ca1e3c3-155d-4684-9298-1e282f8da310:image.png)

### Compile/Download the files (Download the porper files)

Inside /build/

#Install using 8 threads 

$ sudo make -j 8

$ sudo make install 

### Folders Information

![image.png](attachment:6425be34-59e1-4654-9c45-2e9021a5dfbe:image.png)

Folder —> /Geant4/geant4-v11.3.0-install/bin 

### Version

$ ./geant4-config --version
11.3.0

### Setput Environment

Option 1)

$ source geant4-v11.3.0-install/bin/geant4.sh

### Run Project File

Go To Examples Folder

$ cd /Geant4/geant4-v11.3.0/examples/basic/B5/

Create the folder inside example folder build/

$ sudo mkdir build

$ cd build/

$ cmake ..

$ sudo make -j 8

$ ./exampleB5

$ sudo cmake .. ; sudo make -j 8; ./exampleB5
