# Contribuições

:+1: :tada: Antes de começar, gostaríamos de agradecer sua intenção de contribuir para este projeto.

## O que eu devo saber antes de começar?

### Código de Conduta

Este projeto possui um [código de conduta](CODE_OF_CONDUCT.md) e ao participar, você deve segui-lo esse código. Informe
qualquer comportamento inaceitável para [contato@gestaolivre.org](mailto:contato@gestaolivre.org).

### GitHub

> :heart: :octocat: Nós amamos o GitHub

O GitHub é onde estarão armazenados todo o código fonte, documentação e status do projeto. Isso significa que faremos
uso extensivo das ferramentas por ele disponibilizadas, como _issues_, _pull requests_, wiki, etc.

Além disso, o [GitHub Flow](https://guides.github.com/introduction/flow/) é adotado como nosso padrão de projeto, se
pretende contribuir com a codificação do nosso projeto, sugerimos que se tome um tempo para conhece-lo.

### Arquitetura e Design

A arquitetura e design do projeto está incluída com a documentação no repositório ou na wiki do projeto, quaisquer
sugestões devem ser encaminhadas através de _issues_, _pull requests_ ou alterações na wiki.

## Como eu posso contribuir?

### Apontando falhas

Esse é o jeito mais simples de começar, use o projeto e nos diga o que há de errado. Nós controlamos os bugs através
de _issues_ e bem simples de reporta-los.

Faça o possível para ser o mais descritivo possível, quanto mais detalhada for sua descrição do problema mais simples
será sua correção.

Ao criar uma _issue_ você terá um formulário que auxiliará no processo.

### Sugerindo melhorias

O projeto poderia ser melhor, nos diga como.

Crie um _issue_ informando o que temos que melhorar.

### Contribuindo com a documentação

Você já está usando nosso projeto? Que bom! Ajude outras pessoas a se ambientar e usá-lo, você pode contribuir com a
wiki ou com a documentação do projeto.

### Codificando

Mesmo que você seja um desenvolvedor iniciante, pode contribuir com o projeto.

Ambiente-se com os padrões usados e como a aplicação funciona e envie seu _pull request_.

## Contribuindo com o Código

### Preparando seu ambiente

A primeira coisa a fazer é criar seu _fork_ do projeto, a partir dele você poderá enviar suas contribuições.

Crie um clone local do seu projeto:

```bash
git clone git@github.com:contribuidor/gestaolivre-server.git
```

Crie um ambiente virtual e instale as dependências:

```bash
mkvirtualenv `which python3.6` gestaolivre-server
pip install -r requirements.txt
```

### Configure seu projeto

Adicione um arquivo `.env` com o seguinte conteúdo na raiz do projeto:

```bash
DEBUG=on
SECRET_KEY=dev-secret-key
DATABASE_URL=postgres://postgres:postgres@localhost:5432/postgres
CACHE_URL=redis://localhost:6379/0
```

Lembre-se de alterar os dados para refletir sua instalação do PostgreSQL e Redis.

### 

### Atualize sua cópia

Adicione um referência ao nosso repositório para manter sua cópia atualizada:

```
git remote add upstream git@github.com:gestaolivre/gestaolivre-server.git
git fetch upstream
git rebase upstream/master
git push origin master
```

### 


```

```



### Por onde começar?

**1.** Faça o _fork_ do projeto.

**2.** [Entenda nosso fluxo](#fluxo).

**3.** [Leia e pratique as boas práticas](#boas-pr%C3%A1ticas).

### Fluxo

É muito fácil contribuir para o projeto. Qualquer tipo de ajuda (seja ela grande ou pequena) é bem-vinda. Se encontrar qualquer parte do livro que possa ser melhorada, essa é uma grande oportunidade para participar ([aqui](https://github.com/braziljs/eloquente-javascript/issues?q=is%3Aopen+is%3Aissue+label%3Amelhorias) é um ótimo lugar para achar coisas que possam ser melhoradas). Caso não saiba por onde começar:

**1.** Faça referência ao repositório oficial após o _fork_

```
git remote add upstream git@github.com:braziljs/eloquente-javascript.git
```

**2.** Antes de iniciar o processo de contribuição, crie uma nova branch para fazer suas alterações.

Alguns exemplos:

- Para tradução: `git checkout -b traducaoCapX`
- Para revisões: `git checkout -b revisaoCapX`
- Para erros: `git checkout -b correcaoCapX`

> Use qualquer nome que seja coerente com a contribuição que está sendo feita.
> `X` representa o número do capítulo.

**3.** Após realizar as alterações, é hora de fazer um commit com uma mensagem coerente do que foi feito. Exemplo:

```
git add --all
git commit -am ‘Adiciona tradução/revisão/melhoria capítulo X linha/linhas Y’
git push origin traducaoCapX
```

**4.** Envie um _Pull Request_ com as alterações feitas, fazendo referência para o `master` do repositório oficial.

**5.** Sua contribuição será analisada pela comunidade. Em alguns casos pediremos algumas alterações antes de dar merge.

Após o merge:

- Delete a branch utilizada:

```
git checkout master
git push origin :traducaoCapX
git branch -D traducaoCapX
```

- Atualize seu repositório com o repositório oficial:

```
git fetch upstream
git rebase upstream/master
git push -f origin master
```

**6.** Quando iniciar uma nova contribuição, inicie repita o processo pelo passo 2.

### Boas práticas

- **Não traduza termos técnicos e blocos de código**
- Antes de enviar sua contribuição, certifique-se de que está enviando apenas um **único** commit que represente o que foi feito. Caso tenha feito vários commits, [esmague-os](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html) antes de fazer o _Pull Request_.
- Caso tenha qualquer tipo de dúvida, abre uma _Issue_ que faremos o possível para te ajudar.
- Não adicione comentários nas issues de “log”. Elas tem apenas a finalidade de armazenar referências ao trabalho de cada capítulo.
- Contribua com as discussões.
- Delimitação para títulos de obras: Utilizar o travessão (—) para o início da frase, nome do autor e logo após o nome da obra, sem alterar nenhum valor. Exemplo:

> — Master Yuan-Ma, The Book of Programming

- Estrangeirismo: Utilizar o formato itálico. Exemplo: _bug_
- Sentido Figurado: Sempre destacar com aspas duplas.
- Citação: Aspas duplas com o sinal de >. Exemplo:

> “Foo bar”

- Marcação para código: Utilizar um apóstrofe (\`) para indicar um pedaço de código no meio de um texto (`var foo = undefined`). Ou três apóstrofe com o nome da linguagem de programação na frente (\`\`\`js), para indicar um bloco de código:

```js
var foo;
foo = undefined;
```

### Dúvidas em tradução de termos, palavras, expressões etc…

Quando estiver em uma situação em que você não sabe exatamente como traduzir uma palavra, termo ou expressão, nós recomendamos que siga os seguintes passos:

**1.** Abra uma _Issue_ com um título descritivo como por exemplo: “_Como traduzir a palavra/termo “x”?_” e coloque uma descrição fazendo referência à linha e o capítulo que esteja trabalhando.

**2.** Adicione uma tag `[TODO: ref #<número-da-issue-da-discussão>]<palavra/termo não traduzido>[/TODO]` e continue trabalhando no arquivo enquanto não há uma conclusão na _Issue_. Esse processo é importante para facilitar o acesso a itens pendentes e ter uma referência clara onde está ocorrendo a discussão.

**3.** Após a conclusão da discussão na _Issue_, feche a mesma. Em seguida, remova a tag adicionada no passo 2 e atualize a palavra/termo não traduzido.

**4.** Como mantemos um arquivo de [glossário](https://github.com/braziljs/eloquente-javascript/blob/master/glossario.md), faça um _Pull Request_ adicionando o novo termo, colocando a referência `#<número-da-issue>` no termo/palavra em questão para fácil acesso no futuro.

***

Obrigado! :heart: :heart: :heart:

