# VSS-Vision em construção...

É o responsável por capturar posições cartesianas dos robôs a partir da imagem da câmera. Utiliza a biblioteca de processamento de imagem opensource OpenCV. O VSS-Vision está dividido em dois módulos, um de calibragem, onde é possível calibrar cores, cortar e rotacionar a imagem. E um módulo de jogo, onde seta-se o padrão de cada robô, assim como a cor do time. A definição das posições dos robôs são realizadas a partir do rastreamento das cores calibradas.

#### Calibration
- Pressionando F1 você navega entre a imagem original e a imagem auxiliar de calibragem. A imagem auxiliar é uma binarização da imagem orinal a partir dos valores dos sliders do HSV. Esta imagem facilita a configuração das cores.

- Para calibrar as cores dos jogadores e da bola utiliza-se os sliders do HSV. Uma dica para facilitar é, deixe todos os máximos no máximo e todos os mínimos no mínimo desta forma estará pegando o range máximo do HSV e a imagem auxiliar ficara branca. Com isso comece mexendo no slider dos minimos na seguinte ordem, V min, S min, H min. Após mexe-se nos máximos para que apenas a cor desejada fique branca. Quando a cor já estiver quase calibrada faça pequenos ajustes em todos os sliders. 

- Para realizar o corte da imagem deve-se clicar no botão de corte de modo que ele fique pressionado, após clica-se apenas nos cantos do campo na seguinte ordem, canto superior esquerdo, canto superior direito, canto inferior esquerdo e canto inferior direito. Esses cantos estão relacionados com o que você está vendo na tela. Totalizando 4 pontos, que aparecerão vermelhos na tela, esta função ja irá cortar e rotacionar a imagem, através de uma transformação de perspectiva.


#### Vision

- Deve-se carregar a calibragem préviamente feita. Após seleciona-se a cor do time e o padrão dos robôs. feito isso as posições dos jogadores, bola e adversários estarâo aparacendo no canto direito da tela.
