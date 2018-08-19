# Visão Geral

O VSS-SDK é um projeto opensource que auxilia equipes na construção de times de futebol de robôs. 
O SDK possui foco na categoria IEEE Very Small Size Soccer, presente na Competição Brasileira de Robótica (CBR) 
e na Competição Latino-Americana de Robótica (LARC). 

![viewer](http://localhost:3000/imgs/viewer.png)
VSS-Viewer plotando estados do VSS-Simulator e informaçoes de debug de uma estratégia.

O SDK é formado por 5 projetos. São esses: 

* VSS-Vision - Sistema de visão computacional.
* VSS-Simulator - Simulador de partidas de futebol.
* VSS-Viewer - Visualizador de estados e debug.
* VSS-Joystick - Programa de controle de robôs via joysticks usb/bluetooth.
* VSS-Core - Interface de comunicação, domínio, métodos úteis. 

São utilizados tecnologias que possibilitam a construção de estratégias em várias linguagens. Atualmente, 
existem dois exemplos de como realizar a comunicação com os projetos, um em C++ e outro em Rust. 
No futuro serão adicionados mais exemplos. 

* VSS-SampleCpp - Exemplos de como utilizar o SDK.
* VSS-SampleRust - Exemplos de como utilizar o SDK. 