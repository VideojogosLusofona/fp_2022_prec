# Projeto de Recurso de Fundamentos de Programação 2022/2023

## Introdução 
Todos os grupos devem implementar em Python um jogo chamado *Don't Look Down*. Este jogo necessita **obrigatóriamente** interface gráfica em PyGame.

## Contexto do Jogo

*Don't look down* é um *roguelike* inspirado no jogo [Downwell](https://store.steampowered.com/app/360740/Downwell/), onde o objetivo é obter a maior pontuação possível. O jogador controla um boneco chamado *fallguy* que está em queda livre, onde o objetivo é evitar inimigos e armadilhas que aparecem pelo caminho, e *aguentar* o mais tempo possível. 

![Game Screen](figures/GameScreen.png)

### Objectivo do Jogo

O objectivo deste jogo é simplesmente sobreviver o maior tempo possível, evitando os obstaculos que vão aparecendo pelo caminho do jogador. 

### Descrição Técnica

Esta secção descreve as funcionalidades **core** do jogo. 

#### Gameplay

O jogo joga-se com o teclado usando as setas (exclusivamente esquerda e direita). É importante realçar que **o jogador está constantemente em queda livre**, com a excepção de plataformas sem armadilha.

![Player Movement](figures/GameMov.png)

##### Death

Se o jogador cair em cima ou tocar numa armadilha, o jogador *morre* perdendo uma vida. Quando o numero total de vidas chegar a 0 o jogo deve mostrar o ecrã de *Game Over*. O jogador começa com 3 vidas.

##### Point Scoring

Os pontos do jogo estão interligados diretamente ao tempo de jogo total. A cada segundo de jogo é adicionado 1 ponto ao score total do jogador. 

##### Bullets

O jogador tem acesso a um total de 3 *bullets* que permite "destruir" uma plataforma inteira ajudando o jogador a passar através desta sem dano. O bullet também permite reduzir a velocidade de queda do jogador permitindo fazer manobras mais precisas se necessario.

Para usar bullets o jogador usa o *spacebar* (tecla espaço), no qual dispara uma esfera diretamente abaixo do *fallguy* a uma velocidade elevada comparativamente ao do jogador, e diminui a velocidade de queda do jogador durante 1.5 segundos. Se a esfera collidir com uma armadilha este é distruida por completo, deixando o jogador atravesá-la.

O jogador tem um total de 3 balas, cada bala tem um tempo de regeneração de 2.5 segundos. Se não houver balas, o jogador não pode disparar. 

#### Interface

O User Interface deverá apresentar o numero de vidas do jogador (3 no total), o total de pontos acumulado e o número de balas corrente. 

![Game UI](figures/GameUI.png)

##### Start Screen


##### Game Over & Leaderboard


#### Início do Jogo

#### Controlar a Nave

#### Mecânicas dos Cometas

#### Detecção de Colisões


#### Limites do Mundo (Wrap-Around)


#### Leaderboard

O leaderboard deverá ser permanente (mesmo quando se desliga o jogo), e para isso é necessário escrever para um ficheiro os valores destes. Para tal é necessario usar funções de read e write para um ficheiro de texto que irá ser guardado na pasta local do jogo. Funções uteis para ver:

- [Read File](https://www.w3schools.com/python/python_file_open.asp)
- [Write File](https://www.w3schools.com/python/python_file_write.asp)

### Referências


## Objetivos e Critério de Avaliação

Este projeto tem os seguintes objetivos:

-   **O1** - Programa deve funcionar como especificado. Atenção aos detalhes, pois é fácil desviarem-se das especificações caso não **leiam o enunciado com atenção**.
-   **O2** - Projeto e código bem organizados, nomeadamente:
    -   Código devidamente comentado e indentado.
    -   Inexistência de código "morto", que não faz nada, como por exemplo variáveis, propriedades ou métodos nunca usados.
    -   Projeto compila e executa sem erros e/ou _warnings_.
-   **O3** - Projeto adequadamente documentado com *comentários* descrevendo a funcionalidade de várias secções do código.
-   **O4** - Repositório Git deve refletir boa utilização do mesmo, nomeadamente:
    -   Devem existir _commits_ de todos os elementos do grupo, _commits_ esses com mensagens que sigam as melhores práticas para o efeito (como indicado [aqui](https://chris.beams.io/posts/git-commit/), [aqui](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53), [aqui](https://github.com/erlang/otp/wiki/writing-good-commit-messages) e [aqui](https://stackoverflow.com/questions/2290016/git-commit-messages-50-72-formatting)).
    -   Ficheiros binários não necessários, não devem estar no repositório. Ou seja, devem ser ignorados ao nível do ficheiro `.gitignore`.
-   **O5** - Relatório em formato [Markdown](https://guides.github.com/features/mastering-markdown/) (ficheiro `README.md`), organizado da seguinte forma:
    -   Título do projeto.
    -   Autoria:
        -   Nome dos autores (primeiro e último) e respetivos números de aluno.
        -   Informação de quem fez o quê no projeto. Esta informação é **obrigatória** e deve refletir os _commits_ feitos no Git.
        -   Indicação do repositório Git utilizado. Esta indicação é opcional, pois podem preferir manter o repositório privado após a entrega.
    -   Arquitetura da solução:
        -   Descrição da solução, com breve explicação de como o código foi organizado, bem como dos algoritmos não triviais que tenham sido implementados.
    -   Referências, incluindo trocas de ideias com colegas, código aberto reutilizado (e.g., do StackOverflow) e bibliotecas de terceiros utilizadas. Devem ser o mais detalhados possível.
    -   **Nota:** o relatório deve ser simples e breve, com informação mínima e suficiente para que seja possível ter uma boa ideia do que foi feito. Atenção aos erros ortográficos e à correta formatação [Markdown](https://guides.github.com/features/mastering-markdown/), pois ambos serão tidos em conta na nota final.

O projeto tem um peso de 5 valores na nota final da disciplina e será avaliado de forma qualitativa. Isto significa que todos os objetivos têm de ser parcialmente ou totalmente cumpridos. A cada objetivo, O1 a O5, será atribuída uma nota entre 0 e 1. A nota do projeto será dada pela seguinte fórmula:

_N = 5 x O1 x O2 x O3 x O4 x O5_

Isto significa que se os alunos ignorarem completamente um dos objetivos, não tenham feito nada no projeto ou não comparecerem na discussão, a nota final será zero.

### Requisito Mínimo do Projeto

### Pontuação Extra

**Importante**: Façam o minimo requerido primeiro antes de tentarem fazer mais funcionalidades!

## Entrega
O projeto deve ser entregue pelo aluno via Moodle até às **23:59** do dia **3 de Fevereiro 2023**. O aluno deve submeter um ficheiro `zip` com a solução completa, nomeadamente:

-   Pasta escondida `.git` com o repositório Git local do projeto.
-   Pasta do projeto, contendo os ficheiros todos deste.
-   Ficheiro `README.md` contendo o relatório do projeto em formato [Markdown](https://guides.github.com/features/mastering-markdown/).
-   Ficheiro de imagem contendo o Fluxograma. Este ficheiro deve ser incluído no repositório em modo Git LFS.
-   Outros ficheiros de configuração, como por exemplo `.gitignore` e `.gitattributes`.

**Não serão avaliados projetos sem estes elementos e que não sejam entregues através do Moodle.**

## Honestidade académica
Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de honestidade académica. Isto significa que cada ideia que não seja do aluno deve ser claramente indicada, com devida referência ao respectivo autor. O não cumprimento desta regra constitui plágio.

O plágio inclui a utilização de ideias, código ou conjuntos de soluções de outros alunos ou indivíduos, ou quaisquer outras fontes para além dos textos de apoio à disciplina, sem dar o respectivo crédito a essas fontes. Os alunos são encorajados a discutir os problemas com outros alunos e devem mencionar essa discussão quando submetem os projetos. Essa menção **não** influenciará a nota. Os alunos não deverão, no entanto, copiar códigos, documentação e relatórios de outros alunos, ou dar os seus próprios códigos, documentação e relatórios a outros em qualquer circunstância. De facto, não devem sequer deixar códigos, documentação e relatórios em computadores de uso partilhado, e muito menos usar repositórios Git públicos (embora os mesmos possam ser tornados públicos 12h após a data limite de submissão).

Nesta disciplina, a desonestidade académica é considerada fraude, com todas as consequências legais que daí advêm. Qualquer fraude terá como consequência imediata a anulação dos projetos de todos os alunos envolvidos (incluindo os que possibilitaram a ocorrência). Qualquer suspeita de desonestidade académica será relatada aos órgãos superiores da escola para possível instauração de um processo disciplinar. Este poderá resultar em reprovação à disciplina, reprovação de ano ou mesmo suspensão temporária ou definitiva da ULHT.

_Texto adaptado da disciplina de [Algoritmos e Estruturas de Dados](https://fenix.tecnico.ulisboa.pt/disciplinas/AED-2/2009-2010/2-semestre/honestidade-academica) do [Instituto Superior Técnico](https://tecnico.ulisboa.pt/pt/)_

## Licenças
Este enunciado é disponibilizado através da licença [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Metadados
-   Autores: [Phil Lopes](https://github.com/worshipcookies) e [Diogo Andrade](https://github.com/DiogoDeAndrade)
-   Curso: [Licenciatura em Videojogos](https://www.ulusofona.pt/licenciatura/videojogos)
-   Instituição: [Universidade Lusófona de Humanidades e Tecnologias](https://www.ulusofona.pt/)
