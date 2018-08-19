# VSS-Core

O VSS-Core é o núcleo compartilhado entre todos projetos do SDK. Ele é responsável por prover estruturas de dados 
comuns ao problema de futebol de robôs, constantes, enums, métodos úteis e as interfaces de comunicações via rede.
**Atualmente existem dois Cores, um em C++ e outro em Rust**.

O SDK possui um cuidado especial quanto a tempo de execução, pois, o problema de futebol de robôs é muito dinâmico. 
Para diminur ao máximo o overhead causado pela comunicação entre os projetos, são utilizados duas bibliotecas: 
Google Protocol Buffers (Protobuf) e ZeroMQ. 

A biblioteca protobuf é responsável pela serialização dos dados que trafegam entre os projetos. Diferente de outros 
métodos de serialização, como: XML ou JSON. Protobuf gera um código seguro de serialização/deserialização específico 
para cada linguagem, dessa forma facilitando trabalho. Além disso, a biblioteca é conhecida por possuir menores tempo 
de serialização e de deserialização, o que corroborou na sua utilização. 

A biblioteca ZeroMQ é responsável pela comunicação entre os projetos, sendo essa uma fila de mensagens. Cada pacote 
que trafega no projeto possui sua própria fila que pode possuir modelos unicast, multicast ou broadcast. 
Também podem existir comunicações TCP ou UDP. 

Um exemplo de comunicação realizada pelo SDK são os pacotes de estados enviados pelo VSS-Vision e VSS-Simulator. 
Tais pacotes são enviados em broadcast e utilizam o protocolo UDP. O envio desses pacotes em broadcast possibilita que 
estratégias, o VSS-Viewer e outras eventuais aplicações consigam interpretar as mensages, além de não travar a execução 
do Sistema de Visão Computacional e do Simulador. 