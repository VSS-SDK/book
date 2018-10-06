# VSS-Viewer [![GitHub stars](https://img.shields.io/github/contributors/VSS-SDK/VSS-Viewer.svg?style=social&label=Contributors)](https://github.com/VSS-SDK/VSS-Viewer)

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)][gpl3]
[![Build Status](https://api.travis-ci.com/VSS-SDK/VSS-Viewer.svg?branch=master)][travis]

O VSS-Viewer é um visualizador de [estados de jogo](communication.md#estado), que também mostra
[informações de debug](communication.md#depuração). O projeto permite que o usuário pause uma partida
no [VSS-Simulator](vsssimulator.md) e arraste os robôs e a bola.

## Relação com o VSS-Simulator
O VSS-Viewer está fortemente relacionado com o [VSS-Simulator](vsssimulator.md). Por padrão, uma partida
não começa no [VSS-Simulator](vsssimulator.md) até que o VSS-Viewer mande um [pacote de controle](communication.md#controle).
Para enviar esse pacote, basta teclar espaço no VSS-Viewer. Essa tecla pausa e retoma o jogo, sempre que necessário.

## Recebimento de estados
O VSS-Viewer recebe os pacotes de [estado de jogo](communication.md#estado), ouvindo as mensagens do
[VSS-Simulator](vsssimulator.md) e do [VSS-Vision](vssvision.md).

## Manipulando objetos em campo
Para manipular objetos em campo, antes é necessário pausar a partida (apertando a tecla espaço). Após isso,
basta clicar com o botão esquerdo e arrastar os objetos. Para alterar a orientação de um robô, clique com
o botão esquerdo em um, mantenha pressionado o clique, e utilize as setas (direita e esquerda) do teclado.

![viewer](https://raw.githubusercontent.com/VSS-SDK/assets/master/images/changing.png)

Robô (com padrão de cor azul e roxo) sendo manipulado.

## Câmeras
Existem dois tipos de câmeras implementadas, uma que mostra o jogo pelo topo do campo e outra que mostra
o jogo como se fosse uma transmissão de futebol. Para alterar a câmera basta teclar C, porém, apenas
é possível realizar essa operação com o jogo não pausado.

![viewer](https://raw.githubusercontent.com/VSS-SDK/assets/master/images/cameras.png)
Câmera de TV e câmera do topo.

[gpl3]: http://www.gnu.org/licenses/gpl-3.0/
[travis]: https://travis-ci.com/VSS-SDK/VSS-Viewer