# VSS-Vision

É o responsável por capturar posições cartesianas dos robôs a partir da imagem da câmera. Utiliza a biblioteca de processamento de imagem opensource OpenCV. O VSS-Vision está dividido em dois módulos, um de calibragem, onde é possível calibrar cores, cortar e rotacionar a imagem. E um módulo de jogo, onde seta-se o padrão de cada robô, assim como a cor do time. A definição das posições dos robôs são realizadas a partir do rastreamento das cores calibradas. Ambos os módulos possuem a opção de trabalhar com imagens ou com uma câmera.

#### Calibration

- Para calibrar as cores dos jogadores e da bola utiliza-se os sliders do HSV. Uma dica para facilitar é, deixe todos os máximos no máximo e todos os mínimos no mínimo desta forma estará pegando o range máximo do HSV e a imagem auxiliar ficara branca. Com isso comece mexendo no slider dos minimos na seguinte ordem, V min, S min, H min. Após mexe-se nos máximos para que apenas a cor desejada fique selecionada. Quando a cor estiver selecionada, ela ficará contornada por uma borda branca. Quando a cor já estiver quase calibrada faça pequenos ajustes em todos os sliders. 

![Calibration F1 off](https://user-images.githubusercontent.com/45695730/58657313-6040c780-82f4-11e9-83a9-100626186987.png)

- Pressionando F1 você navega entre a imagem original e a imagem auxiliar de calibragem. A imagem auxiliar é uma binarização da imagem orinal a partir dos valores dos sliders do HSV. Esta imagem facilita a configuração das cores, pois nela, as cores na faixa desejada ficam completamente brancas, e as fora da faixa pretas.

![Calibration F1 on](https://user-images.githubusercontent.com/45695730/58657315-620a8b00-82f4-11e9-8ea6-6d6fdba2f489.png)

- Para realizar o corte da imagem deve-se clicar no botão de corte de modo que ele fique pressionado, após clica-se apenas nos cantos do campo na seguinte ordem, canto superior esquerdo, canto superior direito, canto inferior esquerdo e canto inferior direito. Esses cantos estão relacionados com o que você está vendo na tela. Totalizando 4 pontos, que aparecerão vermelhos na tela, esta função ja irá cortar e rotacionar a imagem, através de uma transformação de perspectiva.

- A calibração gera um arquivo .txt, que pode ser acessado de qualquer lugar, ou seja, não necessita ficar armazenado em algum diretório específico (porém recomenda-se utilizar um de fácil acesso). Ele pode ser aberto novamente na calibração para editar o que foi feito, e é necessário para o funcionamento do Vision.

#### Vision

- A maior função do Vision é verificar se a leitura e captura de cores estão sendo feitas de maneira correta, para que as estratégias funcionem com os robôs corretos e suas devidas posições.

- Deve-se carregar a calibragem préviamente feita. Após seleciona-se a cor do time e o padrão dos robôs. Feito isso, as posições dos jogadores, bola e adversários estarâo aparacendo no canto direito da tela. As cores dos times ficam, assim como no Calibration, contornadas de branco, com a adição de um pequeno texto indicando a cor em questão (amarelo ou azul).

![Vision](https://user-images.githubusercontent.com/45695730/58657303-58812300-82f4-11e9-8e01-d5d652783070.png)



