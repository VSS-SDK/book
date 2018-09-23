# VSS-Simulator [![GitHub stars](https://img.shields.io/github/contributors/VSS-SDK/VSS-Simulator.svg?style=social&label=Contributors)](https://github.com/VSS-SDK/VSS-Simulator)

[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)][mit]
[![Build Status](https://api.travis-ci.com/VSS-SDK/VSS-Simulator.svg?branch=master)][travis]

O VSS-Simulator é o simulador de partidas de futebol para a categoria IEEE Very Small Size Soccer. O projeto
fornece um mundo 3D feito utilizando a biblioteca [Bullet Physics](http://bulletphysics.org/wordpress/), 
onde os objetos colidem e possuem restrições cinemáticas e dinâmicas. Há também um árbitro que detecta gols
e reposiciona os objetos em campo, fazendo o jogo prosseguir.
 
## Relação com o VSS-Vision

O VSS-Simulator e o [VSS-Vision](vssvision.md) possuem o mesmo papel de enviar pacotes de estados em broadcast,
que podem ser obtidos pelo [VSS-Viewer](vssviewer.md) e por estratégias.

## Integração com o VSS-Viewer
Quando executado em conjunto com o [VSS-Viewer](vssviewer.md), é possível pausar partidas e alterar a posição
e orientação dos robôs e da bola em campo.

## Modos de finalização de partida
É possível configurar uma partida para nunca terminar, terminar quando passar 10 minutos de jogo ou terminar
quando a diferença de gols entre dois times extrapolar uma certa quantidade. Tudo isso pode ser configuração
com as [flags de execução](simulatorexeflag.md).
 
[travis]: https://travis-ci.com/VSS-SDK/VSS-Simulator
[mit]: https://raw.githubusercontent.com/SIRLab/VSS-Simulator/master/LICENSE.txt