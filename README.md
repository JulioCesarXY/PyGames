# Sonar Treasure Hunt

## Descrição

**Sonar Treasure Hunt** é um jogo de caça ao tesouro simples, desenvolvido em Python, onde o jogador controla um navio em busca de baús de tesouro submersos. O objetivo é localizar os baús utilizando dispositivos sonar para medir a distância até o baú mais próximo. O jogo apresenta um tabuleiro de 60x15 que simula o oceano, com baús escondidos em posições aleatórias.

### Funcionalidades Principais

- **Tabuleiro Dinâmico**: O oceano é gerado aleatoriamente a cada nova partida, garantindo que cada jogo seja único.
- **Sonar Simples**: O sonar mede apenas a distância euclidiana entre o jogador e o baú mais próximo, sem fornecer a direção.
- **Limite de Jogadas**: O jogador possui 20 dispositivos sonar para encontrar 3 baús.
- **Jogabilidade Simples**: O jogo utiliza uma interface de texto amigável, ideal para iniciantes em Python e jogos no terminal.

---

## Como Jogar

1. **Objetivo**: Encontrar todos os baús de tesouro no fundo do oceano.
2. **Jogabilidade**:
   - O jogador deve inserir as coordenadas `(X, Y)` para soltar um dispositivo sonar.
   - O sonar retorna a distância até o baú mais próximo. Se a distância for zero, o jogador encontrou o baú. Caso contrário, uma distância será indicada ou um "X" mostrará que não há baús próximos.
   - O jogo termina quando todos os baús são encontrados ou quando o jogador fica sem dispositivos sonar.
3. **Entrada de Comando**:
   - Durante o jogo, o jogador deve inserir as coordenadas no formato `X Y` (onde `X` varia de 0 a 59 e `Y` de 0 a 14).
   - O jogador pode digitar `quit` a qualquer momento para sair do jogo.

### Exemplo de Tela

You have 20 sonar device(s) left. 3 treasure chest(s) remaining. Where do you want to drop the next sonar device? (0-59 0-14) (or type quit)

> > 30 5 Treasure detected at a distance of 3 from the sonar device.





---

## Instalação

### Pré-requisitos

- **Python 3.x**: Certifique-se de ter o Python instalado em sua máquina. Você pode verificar executando:

    ```bash
    python --version
    ```

### Clonando o Repositório

Clone o repositório do jogo para a sua máquina local usando o comando:

```bash
git clone https://github.com/seu-usuario/sonar-treasure-hunt.git
```
Executando o Jogo

```bash
1. Navegue até a pasta do projeto:

cd sonar-treasure-hunt
```
```bash
2. Execute o jogo:

python sonar_treasure_hunt.py

```


---

Explicação do Jogo

Tabuleiro do Oceano

O tabuleiro é composto por 60 colunas e 15 linhas, representando o fundo do oceano. Cada célula contém ~ ou   para simular as ondas. A cada jogada, o tabuleiro é atualizado para mostrar:

Números: Indicam a distância do sonar ao baú mais próximo.

X: Indica que o sonar não detectou nenhum baú nas proximidades.


Funcionamento do Sonar

Quando o jogador insere as coordenadas para soltar um sonar, a função makeMove() calcula a distância euclidiana do dispositivo até o baú mais próximo usando a fórmula:

distância = sqrt((x2 - x1)**2 + (y2 - y1)**2)

Se a distância for:

0: O jogador encontrou um baú, que será removido do tabuleiro.

Entre 1 e 9: O jogo retorna a distância ao baú mais próximo.

Maior que 9: O jogo exibe um "X", indicando que não há baús próximos.




---

Estrutura do Código

getNewBoard():     # Gera o tabuleiro do oceano aleatoriamente.
drawBoard(board):  # Desenha o tabuleiro no terminal, mostrando as ondas do oceano e as jogadas do jogador.
getRandomChests(numChests):  # Posiciona baús de tesouro em locais aleatórios do oceano.
makeMove(board, chests, x, y): # Executa a jogada do jogador, calculando a distância até o baú mais próximo e atualizando o tabuleiro.
enterPlayerMove(previousMoves): # Lê e valida a entrada do jogador para garantir que as coordenadas estejam corretas.
showInstructions():  # Mostra as instruções do jogo ao jogador.


---

Futuras Melhorias

Aqui estão algumas possíveis melhorias para o jogo no futuro:

Modos de Dificuldade: Adicionar níveis de dificuldade com diferentes quantidades de baús e dispositivos sonar.

Sistema de Pontuação: Implementar um sistema de pontuação baseado no número de tentativas utilizadas.

Interface Gráfica: Expandir o jogo para uma versão gráfica usando bibliotecas como Pygame.

Animações Simples: Incluir animações ou efeitos para tornar o jogo mais visualmente dinâmico.



---

Contribuição

Contribuições são bem-vindas! Se você tiver sugestões, sinta-se à vontade para abrir uma issue ou enviar um pull request.


---

Licença

Este projeto é licenciado sob a MIT License.


---

Agradecimentos

Este jogo foi inspirado por desafios de programação e serve como uma introdução divertida ao desenvolvimento de jogos simples com Python. Agradeço a todos que contribuíram e forneceram feedback!


---

### Alterações e Melhorias Realizadas:
1. **Formatos e Destaques**: Usei Markdown para dar ênfase em títulos e seções.
2. **Clareza**: Melhorei a clareza das instruções e detalhes sobre o funcionamento do jogo.
3. **Estrutura**: Organizei o conteúdo para facilitar a leitura e a navegação.

Sinta-se à vontade para ajustar qualquer parte conforme necessário!

