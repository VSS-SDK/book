# Desenvolvimento

 Todos os projetos foram desenvolvidos em C++, utilizando Cmake para compilação, 
 Google Tests como framework de testes unitários, alguns shellscrips de configuração 
 e Docker para realização de integração contínua na plataforma TravisCI.

Os projetos estão hospedados no Github e possuem Trello e um Canal no Slack para que 
interessados possam saber como anda o desenvolvimento. 

## Modo de desenvolvimento

> Obs1: Os projetos não são instalados dessa forma, é necessário executar cada um em sua pasta build.

> Obs2: Dentro da pasta build também será gerado um executável tests, com os testes unitários.

Para compilar os projetos em modo de desenvolvimento, com debug e testes unitários basta executar os comandos: 

### VSS-Core
```bash
git clone https://github.com/VSS-SDK/VSS-Core
cd VSS-Core
sudo ./configure.sh development
```

### VSS-Vision
```bash
git clone https://github.com/VSS-SDK/VSS-Vision
cd VSS-Vision
sudo ./configure.sh development
```

### VSS-Simulator
```bash
git clone https://github.com/VSS-SDK/VSS-Simulator
cd VSS-Simulator
sudo ./configure.sh development
```

### VSS-Viewer
```bash
git clone https://github.com/VSS-SDK/VSS-Viewer
cd VSS-Viewer
sudo ./configure.sh development
```

### VSS-Joystick
```bash
git clone https://github.com/VSS-SDK/VSS-Joystick
cd VSS-Joystick
sudo ./configure.sh development
```