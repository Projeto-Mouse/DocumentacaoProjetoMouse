# Documentação Cena Debug

A cena debug é uma cena específica do nosso jogo para testes de futuras implementações ou de mudanças.

## Como ativar:

Para ativar o modo debug, temos que segurar a tecla **F12** do teclado por alguns segundos (aproximadamente 2).

Após o tempo passado, escreveremos a palavra-chave: *uniaoflasco*.

Tudo junto e sem acento.

Também não devemos apertar **Enter**.

Depois de apertar o F12 e escrever, podemos apertar *play* e a cena debug será carregada.

## A cena em si:

O mapa da cena debug, no momento, se encontra vazio, apenas com um bloco grande ao lado do spawn.

Mas, conforme formos precisando de coisas, vamos adicionando para fazer testes.

Ou seja, se precisarmos testar algo de escalada, vamos colocar algo relacionado à escalada.

Se quisermos testar *stealth*, vamos colocar algo para testar *stealth*.

E assim por diante.

## A UI da cena e cada botão

Ao abrirmos a cena, podemos ver no canto superior direito que temos três coisas:

- FPS  
- Trocar música  
- Abrir menu debug  

O FPS é o próprio número de quadros por segundo em que o jogo está rodando naquele momento.

O botão de trocar música serve para mudar a música de fundo da cena debug. Essas músicas são uma brincadeira feita para tocar Sabrina Carpenter e outras músicas pop.

E o botão de abrir menu debug, que, obviamente, abre o menu debug com os botões para testar coisas.

## O menu debug

Ao abrir o menu debug, podemos ver vários botões e até mesmo um *slider*.

### Debug Iluminação

O debug de iluminação trabalha com a iluminação dinâmica que existe dentro da cena debug, a mesma que existe no mundo do jogo (com dia, noite, amanhecer etc.).

Temos nele três coisas:

- Um *slider* que altera o tempo, formando um ciclo completo: dia, anoitecer, noite e amanhecer  
- Um *Label* dizendo em qual parte da iluminação estamos  
- Um botão para alternar entre dia e noite, para não precisarmos usar o *slider*  

### Debug Spawn

O debug de spawn é responsável por gerar itens, inimigos e aliados no mapa.

Por enquanto, de entidades, só spawnamos:

- Um tipo de inimigo terrestre  
- Um inimigo voador  
- Um aliado  

Mais para frente, vamos fazer esses botões funcionarem como o de itens.

Teremos cenas de inimigos organizadas em pastas, por exemplo:

Inimigos/Voadores/


Dentro dessa pasta, teremos cenas de todos os inimigos voadores. Ao selecionar um, poderemos clicar na tela para spawnar aquele inimigo.

Mas isso é para o futuro. Por agora, só spawnamos os padrões.

Para aliados é a mesma coisa: por enquanto spawnamos apenas o padrão, mas futuramente poderemos escolher qual aliado spawnar, inclusive para testar diálogo, loja e outras interações.

Também temos o spawn de itens, que já está completo e funcional.

Ao clicar no botão de spawnar item, abrimos um mini explorador de arquivos, que já inicia na pasta de cenas de itens.

Assim, podemos escolher qual item queremos spawnar e, ao clicar em alguma parte do mundo, ele será criado.

Esse item pode ser pego e equipado normalmente, como os itens do mundo principal.

Além disso, temos uma contagem de quantas entidades estão spawnadas.

São consideradas entidades:

- Inimigos  
- Aliados  

Itens não são considerados.

### God Mode

O *God Mode*, como o próprio nome diz, permite que o jogador não tome dano.

Futuramente, podemos adicionar outras funcionalidades, como voar, conforme o mapa for crescendo.

Por enquanto, isso não é necessário.

### Teleporte

O debug de teleporte, ao clicar no botão, espera um clique do mouse em alguma parte da tela.

Quando o clique acontece, o jogador é teletransportado para aquela posição.

### Console

O console é talvez a parte mais complexa.

Com ele, além de printarmos no console da Godot, também podemos exibir mensagens diretamente na tela debug.

Isso pode ser feito de qualquer parte do código, já que ele é um *autoload*.

Sendo assim, sempre que quisermos exibir algo na tela debug (como o dano que o jogador recebe), basta chamar:

- `ConsoleDebug.add_text_console_sem_cor(texto)` para texto sem cor  
- `ConsoleDebug.add_text_console_com_cor(texto, Color.COR)` para texto com cor  

Lembrando que o texto deve estar entre aspas (`""`), como em um `print` normal.

Também temos:

- Um botão para rolar o console até o final (caso estejamos vendo mensagens antigas)  
- Um botão para limpar o console, útil para testar novos prints sem poluição de mensagens anteriores  

## Final

Isso é tudo que temos nessa cena debug por enquanto.

Vale lembrar que ela provavelmente vai crescer e mudar bastante com o tempo, conforme surgirem novas necessidades de teste.