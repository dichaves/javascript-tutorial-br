# Console do desenvolvedor

Códigos são propensos a erros. É provável que você cometa erros... Ah, do que estou falando? Você *absolutamente* vai cometer erros, pelo menos se você é humano, não um [robô](https://en.wikipedia.org/wiki/Bender_(Futurama)).

Mas no navegador, um usuário não vê os erros por padrão. Então, se algo der errado no script, não veremos o que está quebrado e não conseguiremos corrigi-lo.

Para ver erros e obter muitas outras informações úteis sobre scripts, os navegadores têm "ferramentas de desenvolvedor" incorporadas.

Na maioria das vezes, os desenvolvedores tendem a usar o Chrome ou o Firefox para desenvolvimento, porque esses navegadores possuem as melhores ferramentas. Outros navegadores também fornecem ferramentas para desenvolvedores, às vezes com recursos especiais, mas geralmente estão ainda tentando alcançar o Chrome ou o Firefox. Então, a maioria das pessoas tem um navegador "favorito" e muda para outros se um problema for específico do navegador.

As ferramentas do desenvolvedor são realmente poderosas, existem muitos recursos. Para começar, aprenderemos como abri-los, ver erros e executar comandos JavaScript.


## Google Chrome

Abra a página [bug.html](bug.html).

Há um erro no código JavaScript dela. Está escondido dos olhos de um visitante regular, então vamos abrir as ferramentas do desenvolvedor para vê-lo.

Pressione a tecla `key:F12` ou, se você estiver no Mac, pressione `key:Cmd+Opt+J`.

As ferramentas do desenvolvedor serão abertas na guia Console por padrão.

Parece um pouco com isso:

![cromo](chrome.png)

O aspecto exato das ferramentas do desenvolvedor depende da sua versão do Chrome. Ele muda de tempos em tempos, mas deve ser similar.

- Aqui podemos ver a mensagem de erro de cor vermelha. Neste caso, o script contém um comando desconhecido chamado "lalala".
- À direita, existe um link clicável na fonte `bug.html:12` com o número da linha onde o erro ocorreu.

Abaixo da mensagem de erro, há um símbolo `>` azul. Ele marca uma "linha de comando" onde podemos digitar comandos de JavaScript e pressionar a tecla `key:Enter` para executá-los (`key:Shift+Enter` para inserir comandos de múltiplas linhas).

Agora podemos ver erros e isso é o suficiente para o início. Voltaremos às ferramentas do desenvolvedor mais tarde e cobriremos uma depuração mais aprofundada no capítulo <info:debugging-chrome>.


## Firefox, Edge e outros

A maioria dos outros navegadores usa `key:F12` para abrir as ferramentas do desenvolvedor.

A aparência deles é bem parecida. Uma vez que você sabe como usar um deles (você pode começar com o Chrome), pode mudar facilmente para outro.

## Safari

O Safari (navegador Mac, não suportado pelo Windows/Linux) é um pouco especial aqui. Precisamos primeiro habilitar o "menu Desenvolvedor".

Abra Preferências e vá para o painel "Avançado". Há uma caixa de seleção na parte inferior:

![safari](safari.png)

Agora `key:Cmd+Opt+C` pode alternar o console. Observe também que o novo item do menu superior, chamado "Desenvolvedor", apareceu. Ele tem muitos comandos e opções.

## Resumo

- As ferramentas do desenvolvedor nos permitem ver erros, executar comandos, examinar variáveis ​​e muito mais.
- Elas podem ser abertas com `key:F12` para a maioria dos navegadores no Windows. O Chrome para Mac precisa de `key:Cmd+Opt+J`, e o Safari `key:Cmd+Opt+C` (precisa ser ativado antes).

Agora temos o ambiente pronto. Na próxima seção, nos concentraremos em JavaScript.
