# Uma introdução a JavaScript

Vamos ver o que é tão especial sobre JavaScript, o que podemos fazer com essa linguagem e quais outras tecnologias funcionam bem com ela.

## O que é o JavaScript?

*JavaScript* foi inicialmente criado para *"tornar as páginas vivas"*.

Os programas nesta linguagem são chamados de *scripts*. Eles podem ser escritos diretamente no HTML e são executados automaticamente à medida que a página carrega.

Scripts são fornecidos e executados como um texto simples. Eles não precisam de uma preparação especial ou uma compilação para rodar.

Neste aspecto, JavaScript é muito diferente de uma outra linguagem chamada [Java](http://pt.wikipedia.org/wiki/Java_(linguagem_de_programação)).

```smart header="Por que <u>Java</u>Script?"
Quando JavaScript foi criado, inicialmente tinha outro nome: "LiveScript". Mas a linguagem Java era muito popular naquela época, então foi decidido que posicionar essa nova linguagem como um "irmão mais novo" de Java ajudaria.

Mas, à medida que evoluiu, JavaScript tornou-se uma linguagem totalmente independente, com sua própria especificação chamada [ECMAScript](https://pt.wikipedia.org/wiki/ECMAScript), e agora não tem relação alguma com Java.
```

Atualmente, JavaScript pode ser executado não somente no navegador, mas também no servidor, ou mesmo em qualquer dispositivo onde exista um programa especial chamado [Interpretador de JavaScript](https://pt.wikipedia.org/wiki/Interpretador_de_JavaScript).

O navegador possui um interpretador incorporado, que às vezes é chamado de "máquina virtual JavaScript".

Diferentes interpretadores têm diferentes "codinomes", por exemplo:

- [V8](https://pt.wikipedia.org/wiki/V8_(JavaScript)) - no Chrome e no Opera.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) - no Firefox.
- ... Existem outros codinomes como "Trident", "Chakra" para diferentes versões do IE, "ChakraCore" para Microsoft Edge, "Nitro" e "SquirrelFish" para Safari, etc.

É bom lembrar dos termos acima, porque eles são usados ​​em artigos de desenvolvedores na internet. Nós também os usaremos. Por exemplo, se "um recurso X é suportado pelo V8", então provavelmente funciona no Chrome e no Opera.

```smart header="Como funcionam os interpretadores?"

Interpretadores são complicados. Mas o básico é fácil.

1. O interpretador (incorporado, se for um navegador) lê ("analisa") o script.
2. Então ele converte ("compila") o script para a linguagem da máquina.
3. Em seguida, o código da máquina é rapidamente executado.

O interpretador aplica otimizações em todas as etapas do processo. Ele observa o script compilado conforme é executado, analisa os dados que passam por ele e aplica otimizações ao código da máquina com base nesse conhecimento. No final, os scripts são bastante rápidos.
```

## O que o JavaScript do navegador pode fazer?

O JavaScript moderno é uma linguagem de programação "segura". Não fornece acesso de baixo nível à memória ou à CPU, porque foi inicialmente criado para navegadores que não o exigem.

Os recursos dependem muito do ambiente que executa JavaScript. Por exemplo, [Node.JS](https://pt.wikipedia.org/wiki/Node.js) suporta funções que permitem que o JavaScript leia/escreva arquivos arbitrários, execute solicitações de rede, etc.

O JavaScript no navegador pode fazer tudo relacionado à manipulação da página, à interação com o usuário e ao servidor web.

Por exemplo, o JavaScript no navegador é capaz de:

- Adicionar novo HTML à página, alterar o conteúdo existente, modificar estilos.
- Reagir às ações do usuário, executar em cliques do mouse, movimentos de ponteiro, pressionamento de teclas.
- Enviar solicitações através da rede para servidores remotos, baixar e fazer upload de arquivos (as tecnologias chamadas [AJAX](https://pt.wikipedia.org/wiki/AJAX_(programação)) e [COMET](https://pt.wikipedia.org/wiki/Comet_(programação)).
- Obter e definir cookies, fazer perguntas ao visitante, mostrar mensagens.
- Lembrar dos dados no lado do cliente ("armazenamento local").

## O que o JavaScript no navegador NÃO pode fazer?

As habilidades do JavaScript no navegador são limitadas por causa da segurança do usuário. O objetivo é evitar que uma página mal-intencionada acesse informações privadas ou prejudique os dados do usuário.

Os exemplos de tais restrições são:

- O JavaScript em uma página da Web não pode ler/escrever arquivos arbitrários no disco rígido, copiá-los ou executar programas. Não possui acesso direto às funções do sistema operacional.

Os navegadores modernos permitem que ele funcione com arquivos, mas o acesso é limitado e apenas fornecido se o usuário fizer determinadas ações, como "soltar" um arquivo em uma janela do navegador ou selecioná-lo através de uma tag `<input>`.

Existem maneiras de interagir com câmera/microfone e outros dispositivos, mas eles exigem permissão explícita do usuário. Portanto, uma página habilitada para JavaScript não pode sorrateiramente ativar uma câmera web, observar o ambiente e enviar as informações para a [NSA](https://pt.wikipedia.org/wiki/Agência_de_Segurança_Nacional).
- Diferentes abas/janelas geralmente não sabem uma sobre a outra. Às vezes elas sabem, por exemplo quando uma janela usa o JavaScript para abrir a outra. Mas, mesmo neste caso, o JavaScript de uma página não pode acessar o outro se eles vierem de sites diferentes (de um domínio, protocolo ou porta diferente).

Isso é chamado de "Política de mesma origem". Para contornar isso, *ambas as páginas* devem conter um código JavaScript especial que lida com a troca de dados.

A limitação é novamente para a segurança do usuário. Uma página de `http://umsitequalquer.com.br` que um usuário abriu não deve poder acessar outra guia do navegador com a URL `http://gmail.com` e roubar informações a partir daí.

- O JavaScript pode se comunicar facilmente pela rede com o servidor do qual a página atual veio. Mas a capacidade de receber dados de outros sites/domínios é prejudicada. Embora possivel, requer um acordo explícito (expresso em cabeçalhos HTTP) do lado remoto. Mais uma vez, são limitações de segurança.

![](limitations.png)

Esses limites não existem se o JavaScript for usado fora do navegador, como por exemplo em um servidor. Os navegadores modernos também permitem instalar plugins/extensões que podem obter permissões estendidas.

## O que torna JavaScript único?

Existem pelo menos *três* coisas excelentes sobre JavaScript:

```comparar
+ Integração completa com HTML/CSS.
+ Coisas simples feitas de maneira simples.
+ Suportado por todos os navegadores principais e habilitado por padrão.
```

Combinadas, estas três coisas existem apenas em JavaScript e nenhuma outra tecnologia de navegador.

Isso é o que torna JavaScript único. É por isso que é a ferramenta mais difundida para criar interfaces de navegador.

Enquanto se planeja aprender uma nova tecnologia, é benéfico verificar suas perspectivas. Então, vamos partir para as tendências modernas que incluem novas linguagens e habilidades do navegador.


## Linguagens "em cima" de JavaScript

A sintaxe do JavaScript não se adequa às necessidades de todos. Pessoas diferentes querem características diferentes.

Isso é de se esperar, porque projetos e requisitos são diferentes para todos.

Recentemente, surgiu uma infinidade de novas linguagens, que são *transpiladas* (convertidas) para JavaScript antes de serem executadas no navegador.

As ferramentas modernas tornam a transpilação muito rápida e transparente, permitindo que os desenvolvedores programem em outra linguagem e convertendo automaticamente "debaixo dos panos".

Exemplos de tais linguagens:

- [CoffeeScript](http://coffeescript.org/) é um "açúcar sintático" para JavaScript, ele apresenta uma sintaxe mais curta, permitindo escrever código mais preciso e claro. Geralmente, os desenvovedores Ruby gostam dele.
- [TypeScript](http://www.typescriptlang.org/) concentra-se na adição de "dados fortemente tipados", para simplificar o desenvolvimento e suporte a sistemas complexos. É desenvolvido pela Microsoft.
- [Dart](https://www.dartlang.org/) é uma linguagem autônoma que possui seu próprio interpretador que é executado em ambientes que não são navegadores (como aplicativos para dispositivos móveis). Inicialmente foi oferecido pelo Google como um substituto para JavaScript, mas, a partir de agora, os navegadores exigem que ele seja transpilado para o JavaScript, assim como os acima.

E existem mais. Claro que, mesmo que usemos uma dessas linguagens, também devemos saber JavaScript para realmente entender o que estamos fazendo.

## Resumo

- JavaScript foi inicialmente criado como uma linguagem restrita ao navegador, mas agora também é usado em muitos outros ambientes.
- Neste momento, JavaScript está na posição única de linguagem de navegador mais amplamente adotada com integração total com HTML/CSS.
- Existem muitas linguagens que são "transpiladas" para JavaScript e fornecem certos recursos. Recomenda-se dar uma olhada nelas, pelo menos brevemente, depois de dominar o JavaScript.
