# Desenvolvimento

Todos os projetos foram desenvolvidos em C++, utilizando [Cmake](https://cmake.org/) para compilação, 
[Google Tests](https://github.com/google/googletest) como framework de testes unitários, 
alguns shellscrips de configuração  e [Docker](https://www.docker.com/) para realização de integração
contínua na plataforma [TravisCI](https://travis-ci.com/VSS-SDK).

## Modo de desenvolvimento

> Obs1: Os projetos não são instalados dessa forma, é necessário executar cada um em sua pasta build.

> Obs2: Dentro da pasta build também será gerado um executável tests, com os testes unitários.

Para compilar os projetos em modo de desenvolvimento, com debug e testes unitários basta executar os comandos: 

### VSS-Core
```
git clone https://github.com/VSS-SDK/VSS-Core
cd VSS-Core
sudo ./configure.sh development
```

### VSS-Vision
```
git clone https://github.com/VSS-SDK/VSS-Vision
cd VSS-Vision
sudo ./configure.sh development
```

### VSS-Simulator
```
git clone https://github.com/VSS-SDK/VSS-Simulator
cd VSS-Simulator
sudo ./configure.sh development
```

### VSS-Viewer
```
git clone https://github.com/VSS-SDK/VSS-Viewer
cd VSS-Viewer
sudo ./configure.sh development
```

### VSS-Joystick
```
git clone https://github.com/VSS-SDK/VSS-Joystick
cd VSS-Joystick
sudo ./configure.sh development
```