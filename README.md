# Sistema Solar com OpenGl, GLEW e GLUT
## Projeto com iluminação

### Autores

- Isaias do Carmo
- Ingrynd
- Ionara
- Jean
- Jose Anahelton
- Felipe Barros

## Demonstração

## Características

- Ao iniciar o programa no vistual studio, já é iniciado a simulação do sistema solar
- Planetas e estrelas foram feitos usando classes que recebem como construtuor paramentros que definem sua posição
- Para trabalhar e construir as textura foi usado as funções glGenTextures, glBindTexture, glTexImage2D
- Nesta fase do processo foi adicionado a iluminação, foi usado:
    -  glEnable(GL_LIGHTING) -  ativar iluminação
    -  Definir os arrays da luz ambiente e ativa-la com a função glLightModelfv()
    -  configuração da luz difusa: responsável pelo efeito de "degradé" nos objetos, há um ponto a partir do qual a luz é emitida e seu brilho é emitido indistintamente em todas as direções.
        - Definir e ativar uma luz Difusa usando glLightfv()
        - Definir e ativar uma luz Especular: é a responsável pela geração de pontos de brilho no objeto
- Função para configurar as texturas e chamar a função responsável pela iluminação
- Trabalhando com tranformações de translação, rotação e escala
    - glPushMatrix() e glPopMatrix() para permitir que uma transformação valha somente em um certo trecho de prograam
    - glTranslatef() para trabalhar com a translação 
    - glRotatef() - para rotação
    - glutWireTorus() para desenhar wireframe de um torus
- Para desenhar as cenas foram usadas várais funções da Gl, afim de construir o sistema de acordo com as posiões, rotação e translações adequadas. 
- Há um método animate que é responsábel pela animação do sistema, incrementando o valor da orbita dos planetas e astros e jogando na função glutTimerFunc() que redesenha o quadrado com as novas coordenadas


[Link da demonstração sem ilumincação](https://youtu.be/778saKiBlTo) - sem iluminação

[Video com iluminação](https://youtu.be/eCrHfMTC09c) - com iluminação
## Melhorias

- Ajustar melhor a iluminação ao ir mudando o ângulo de visão da camera
- adicionar mais cameras ao projeto, para uma melhor visualização do sistema
- Resolver problemas como: velocidade, iluminação do sol e luz refletida nos planetas
- Permitir rodar em outros sistemas

## Problemas
- O grande problema foi a dificuldade técnica
    - Alguns membros tinham pouco conhecimento com versionamento de código o que atrasou o andar do projeto
    - Alguns membros usavam Linux outros windows, foi necessário focar em um sistema e até mesmo o uso de maquinas em cloud teve para ajudar no andar do projeto
    - Bugs que níguem sabe explicar: mesmo código rodando em um sitema windows de um dos membros, mas não rodava em um computador com windows de outro membro.
    - Foi usados diferentes fontes para construir o projeto, o que pode ser, mas não sabemos, o responsável por alguns bugs de compatiblidade.
    - Um problema mais simples que houve foi o uso do github, ao tentar comitar as alterações, houve um erro não resolvido pelos membros, foi necessário criar outro repositório e subir pelo github os arquivos.

## Referências
[Creating the Solar System — OpenGL and C++](https://medium.com/@keynekassapa13/creating-the-solar-system-opengl-and-c-9d4e4798d759)

https://github.com/1kar/OpenGL-SolarSystem
