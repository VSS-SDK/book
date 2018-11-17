# Visão Geral [![GitHub stars](https://img.shields.io/github/stars/VSS-SDK/VSS-SDK.svg?style=social&label=Stars)](https://github.com/VSS-SDK/VSS-SDK)

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)][gpl3]

O VSS-SDK é um projeto opensource que auxilia equipes na construção de times de futebol de robôs. 
O SDK possui foco na categoria IEEE Very Small Size Soccer, presente na Competição Brasileira de Robótica (CBR) 
e na Competição Latino-Americana de Robótica (LARC). 

Os projetos estão hospedados no Github e possuem um [Grupo de WhatsApp](https://chat.whatsapp.com/ESqglT350Jd4GUi5BQLxEp), 
um Kanban no [Trello](https://trello.com/b/b4dVV6ug/vss-sdk) e um Canal no [Slack](https://vss-sdk.slack.com) para que
interessados possam trocar ideias sobre a categoria IEEE-VSS e discutir questões sobre o SDK. 

* [Instalação](install.md)
* [Utilização](use.md)
* [Desenvolvimento](dev.md)
* [Arquivos Protos](protofiles.md)

![viewer](https://raw.githubusercontent.com/VSS-SDK/assets/master/images/sdk.png)
VSS-Viewer plotando estados do VSS-Simulator e informaçoes de debug de uma estratégia.

O SDK é formado por 4 projetos e alguns exemplos. São esses: 

* [VSS-Vision](vssvision.md) - Sistema de visão computacional.
* [VSS-Simulator](vsssimulator.md) - Simulador de partidas de futebol.
* [VSS-Viewer](vssviewer.md) - Visualizador de estados e debug.
* [VSS-Joystick](vssjoystick.md) - Programa de controle de robôs via joysticks usb/bluetooth.
* [VSS-Samples](samples.md) - Exemplos de estratégias.

Atualmente são suportados somente distribuições Linux, como: Ubuntu 14, Ubuntu 16, Ubuntu 18, Linux Mint 18
e Debian 9.

[gpl3]: http://www.gnu.org/licenses/gpl-3.0/
[travis]: https://travis-ci.com/VSS-SDK/VSS-SDK