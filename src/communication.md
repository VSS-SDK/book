# Comunicação entre projetos

Foram idealizados quatro pacotes de comunicação entre os projetos que possuem responsabilidades diferentes. 
Suas definições podem ser encontradas nos [arquivos protos](protofiles.md) e exemplos de utilização podem
ser encontrados nos [VSS-Samples](samples.mdssssssssssssssssssssssssssssssssssssssssssssssssssssssssss).

## Estado
O pacote de estado carrega informações das posições e orientações de todos os objetos em campo, ele pode ser
enviado pelo [VSS-Vision](vssvision.md) e pelo [VSS-Simulator](vsssimulator.md), e o projeto [VSS-Viewer](vssviewer.md)
está configurado para automáticamente interpretar mensagem de ambos os projetos. O conteúdo do pacote pode ser
visto na [seção de state](protofiles.md#state) nos arquivos protos e o mesmo por padrão trafega na porta 5555.

## Comando
O pacote de comando carrega informações das velocidades das rodas dos robôs de um time. Cada time envia um pacote
desse para o [VSS-Simulator](vsssimulator.md), por padrão o time amarelo utiliza a porta 5556 e o time azul utiliza
a porta 5557. O projeto [VSS-Joystick](vssjoystick.md) utiliza o mesmo pacote nas mesmas portas para controlar
robôs. O conteúdo do pacote pode ser visto na [seção de command](protofiles.md#command).

## Depuração
O pacote de depuração carrega informações que podem ser plotadas no [VSS-Viewer](vssviewer.md), como, pose objetivo,
vetor de movimento e caminhos. Por padrão é utilizado a porta 5558 para envio de debug pelo time amarelo e a porta
5559 é utilizada pelo time azul. O conteúdo do pacote pode ser visto na [seção de debug](protofiles.md#debug).

## Controle
O pacote de controle é exclusivamente enviado pelo [VSS-Viewer](vssviewer.md) para o [VSS-Simulator](vsssimulator.md)
e serve para iniciar e pausar a simulação. O conteúdo do pacote pode ser visto na [seção de control](protofiles.md#control).