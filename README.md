# Sistema para Gestão de Campeonatos
> Projeto desenvolvido para a disciplina de Programação Orientada a Objetos.

#### A aplicação tem importância para organização de campeonatos sejam eles amadores ou não, assim formando os duelos de forma automática pelo sistema, facilitando os cálculos para saber os vencedores por meio do sistema de pontos.
**O tema definido por meio de sorteio que deve cumprir alguns requisitos, sendo eles:**
- Permitir o cadastro de equipes (inclusão, exclusão e edição);
- Exibir relação de equipes;
- Gerar tabela de jogos, com as equipes e data/hora do jogo;
- Permitir a inserção dos placares dos jogos;
- Exibir ranking das equipes conforme o registro dos placares dos jogos:
  - Vitória equivale a 3 pontos
  - Empate equivale a 1 ponto.
  
 **Para desenvolvimento da mesma, se fez necessária algumas ferramentas, sendo elas:**
 - QT designer, para desenvolvimento da interface;
 - VSCode, utilizando o python para desenvolvimento do código para funcionamento da interface e interação entre as telas;
 - Necessário implementação do pyside6 para conversão do arquivo .UI para .PY ;
 - Site lucid.app para criação do diagrama de classes UML e diagrama de caso de uso;
 - Site github.com para documentação do projeto.
 
**O sistema em questão teve seu início no dia 24 de janeiro de 2023 e sua finalização no dia 06 de fevereiro de 2023. Inicialmente, de forma manual, utilizando papel e caneta realizamos a criação das telas que seriam apresentadas, por conseguinte iniciamos a criação das telas no QT designer e realizamos a divisão de tarefas para os componentes do grupo, ao longo das semanas foram realizadas melhorias, tanto no código python, quanto na interface juntamente com a criação dos diagramas (de caso de uso e  de classes UML)para melhor entendimento da aplicação.**

Abaixo se tem o diagrama de casos de uso UML que foi utilizado para desenvolvimento do código em python:
![image](https://user-images.githubusercontent.com/115077376/217119249-087b2dc3-97be-4f2a-8011-28bfdd22e998.png)
Dentro do diagrama temos as seguintes classes:
- Equipe:
  - #nomeEquipe: string (atributo), que tem o papel de registro do nome da equipe;
  - #Equipe: int (atributo), que serve para identificação da equipe, como um ID;
  - +alterarNome() (método), utilizado para mudança do nome da equipe (caso usuário deseje);
  - +excluirEquipe() (método), utilizada para exclusão de equipe (caso usuário deseje).
  
- Nome das Equipes:
  - Essa é uma classe secundária que tem como sua primária a classe Equipe;
  - +exibirEquipes() (método), mostrar as equipes na tela.
  
- Jogos:
  - -equipes: equipe[] (atributo), gerar jogos entre duas equipes;
  - -dataJogo: date (atributo), data em que jogo ocorrerá;
  - -horarioJogo: time (atributo), hora em que irá acontecer;
  - -placar: string (atributo), colocar o placar final;
  - +equipevencedora(): string (método), registrar equipe vencedora;
  - +empate(): boolean (método), registrar se foi empate ou não.
  
- Ranking:
  - -colocação Equipe:int (atributo), mostrar qual foi a colocação das equipes;
  - -nomeEquipe: string (atributo), exibir as equipes;
  - +somarPontos() (método), somar os pontos dos vencedores e dos empates para saber o total de pontos. 
 
Além do diagrama de classes, temos o diagrama de casos de uso, que é apresentado logo abaixo:
![image](https://user-images.githubusercontent.com/115077376/217124006-52bdccf7-d4de-411a-b4f0-a72583e90f1a.png)

O diagram em questão demonstra a funcionalidade do sistema, os atores são o usuário que irá registrar as equipes, as datas, os horários e os placares do duelo. Já o sistema de jogos irá guardar as informações, os nomes das equipes, os vencedores(ou empate) assim somando os pontos. Também realizará a geração dos duelos com as equipes que foram registradas.  






__Discentes envolvidos: Graciele Pontes; Guilherme Florêncio; Jonathan Leoncio; Mateus Eider; Moises Nascimento.__
