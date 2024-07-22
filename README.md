## README

### Jogo da Velha - Oficial

Este projeto é uma implementação do clássico jogo da velha (ou "tic-tac-toe") com diversas funcionalidades, incluindo modos de jogo entre humanos e entre computador e humano. O código utiliza a biblioteca `tensorflow` e outras bibliotecas comuns para simulação e aprendizado de máquina, embora a implementação principal não utilize diretamente essas funcionalidades. O jogo pode ser jogado em três modos:

1. Humano vs. Computador
2. Humano vs. Humano
3. Computador vs. Computador

### Requisitos

- Python 3.x
- Bibliotecas Python: `numpy`, `pickle`, `tensorflow`, `keras`, `pandas`, `matplotlib`, `scipy`

### Instalação

1. **Clone o repositório:**
    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <DIRETORIO_DO_REPOSITORIO>
    ```

2. **Instale as dependências:**
    ```bash
    pip install numpy tensorflow keras pandas matplotlib scipy
    ```

### Estrutura do Código

O código está estruturado em classes que representam diferentes componentes do jogo:

- **`Board`**: Representa o tabuleiro do jogo, incluindo métodos para imprimir o tabuleiro, fazer movimentos, verificar vencedores e obter quadrados vazios.

- **`Node`**: Representa um nó na árvore de jogo, usado para determinar o melhor movimento.

- **`AlphaBeta`**: Implementa o algoritmo minimax com poda alpha-beta para otimizar a tomada de decisão dos computadores.

- **`JogoDaVelha`**: Gerencia a lógica do jogo, incluindo modos de jogo e interação com o usuário.

### Como Executar

Para iniciar o jogo, execute o script principal:

```bash
python jogo_da_velha.py
```

### Modos de Jogo

1. **Humano vs. Computador**: O jogador humano joga contra o computador. O computador faz movimentos aleatórios.

2. **Humano vs. Humano**: Dois jogadores humanos alternam movimentos.

3. **Computador vs. Computador**: Dois computadores jogam entre si com base em movimentos aleatórios.

### Detalhes do Código

- **Classe `Board`:**
  - `__init__`: Inicializa o tabuleiro e o jogador atual.
  - `print_board`: Imprime o estado atual do tabuleiro.
  - `make_move`: Faz um movimento no tabuleiro.
  - `is_winner`: Verifica se há um vencedor.
  - `is_full`: Verifica se o tabuleiro está cheio.
  - `get_empty_squares`: Retorna uma lista de posições vazias no tabuleiro.

- **Classe `Node`:**
  - `__init__`: Inicializa um nó com um tabuleiro e um jogador.
  - `is_terminal_node`: Verifica se o nó é terminal (jogo terminado ou tabuleiro cheio).
  - `get_best_move`: Obtém o melhor movimento baseado nos nós filhos.

- **Classe `AlphaBeta`:**
  - `__init__`: Inicializa a profundidade da busca.
  - `minimax`: Implementa o algoritmo minimax com poda alpha-beta.

- **Classe `JogoDaVelha`:**
  - `__init__`: Inicializa o jogo e define o primeiro jogador.
  - `play_human_vs_computer`: Jogo entre humano e computador.
  - `play_human_vs_human`: Jogo entre dois humanos.
  - `play_computer_vs_computer`: Jogo entre dois computadores.
  - `start_game`: Inicia o jogo e permite ao usuário escolher o modo de jogo.

### Exemplo de Execução

```plaintext
Bem-vindo ao Jogo da Velha!
Escolha um modo de jogo:
1. Humano x Computador
2. Humano x Humano
3. Computador x Computador
Digite sua escolha (1-3): 1
```

### Contribuição

Se desejar contribuir para o projeto, faça um fork do repositório e envie suas alterações via pull requests. Para relatar bugs ou solicitar novas funcionalidades, abra uma issue no repositório.

### Licença

Este projeto está licenciado sob a [Licença MIT](https://opensource.org/licenses/MIT). Veja o arquivo LICENSE para mais detalhes.
