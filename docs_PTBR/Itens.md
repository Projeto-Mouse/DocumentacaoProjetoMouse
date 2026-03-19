# SISTEMA DE ITENS E COMO CRIAR UM

## 1 - Introdução

A ideia aqui é apresentar a estrutura atual que estamos usando de itens e como criar um item novo, caso você precise, e vai precisar.

## 2 - Estrutura de pastas e o que cada uma faz.

```
📁 Itens/
├── 📁 Cenas/
│   ├── 📁 CenasMapa/

│   └── 📁 CenasMaoJogador/

├── 📁 Equipamentos/
│   ├── 📁 Armas/

│   ├── 📁 Armaduras/
│   │
│   ├── 📁 Ferramentas/
│   │
│   └── 📁 Ferramentas (outros)
│
├── 📁 Equipamentos (outros)

├── 📄 ItemData.gd
└── 📄 ItemMundo.gd
```

Por enquanto a estrutura de pastas está assim, e acho que está em um bom caminho.

### 2.1 - O que cada pasta/arquivo faz

```
📁 Itens/
```

Essa é a pasta principal é, obviamente a pasta que vamos guardar tudo que tem haver com itens.

```
├── 📁 Cenas/
│   ├── 📁 CenasMapa/

│   └── 📁 CenasMaoJogador/
```

Essa estrutura de pasta vão guardar as cenas que temos.

Isso é:

CenasMapa - É a cena do item no mapa. Ela guarda area3d, colisionshape ( se tiver ), o script ItemMundo.

ItemMundo é um script que adiciona o item em Interagiveis e faz o esquema de se entrarmos na area dele ele setar a variavel do jogador item_da_area_atual.

CenasMaoJogador - É onde vamos guardar as cenas do mesmo item, só que a cena que é um Node3D com um Sprite3D e possivelmente algum script do item, que controla algo que o item fassa, por exemplo a tocha que tem a Omnilight3D e o script da luz, para fazer piscar.

Esses nós que fazem parte do item, os scripts deles e que funcionam na mao do jogador, a luz piscar funciona na mao do jogador, ficam na cena que fica nessa pasta.

Resumindo os itens que ficam no mundo vao ter a cena na pasta itens mundo, quando pegarmos o item do mundo vamos instanciar a cena item mao ( que fica na outra pasta ) na mao do jogador.

Sempre que pegarmos o item do inventario e a cena item mão que vamos instanciar na mão.

