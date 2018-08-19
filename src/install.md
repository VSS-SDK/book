# Instalação

## VSS-Core
Inicialmente é necessário instalar o biblioteca VSS-Core. Para isso, abra um terminal e execute os comandos:

```bash
git clone https://github.com/VSS-SDK/VSS-Core
cd VSS-Core
sudo ./configure.sh
```

O script irá atualizar os pacotes do Linux e em seguida irá instalar as dependências necessárias para rodar o SDK. 
Por último, a biblioteca será compilada e instalada na sua distro. 

## Demais projetos
Para instalar os outros projetos não existe ordem. Basta seguir os comandos. 

### VSS-Vision
```bash
git clone https://github.com/VSS-SDK/VSS-Vision
cd VSS-Vision
sudo ./configure.sh
```

### VSS-Simulator
```bash
git clone https://github.com/VSS-SDK/VSS-Simulator
cd VSS-Simulator
sudo ./configure.sh
```

### VSS-Viewer
```bash
git clone https://github.com/VSS-SDK/VSS-Viewer
cd VSS-Viewer
sudo ./configure.sh
```

### VSS-Joystick
```bash
git clone https://github.com/VSS-SDK/VSS-Joystick
cd VSS-Joystick
sudo ./configure.sh
```