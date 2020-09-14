# Teste de frontend da Gblix

**Por favor, leia esse documento com atenção.**

## Introdução

Esse é o teste de frontend da Gblix. Recomendamos que você faça um _fork_ dele
para seu perfil para continuar.

Nesse teste utilizaremos o [Parcel Bundler](https://parceljs.org), pela sua
simplicidade e por não precisar de configuração em vários casos. Você pode
utilizar nativamente JS, JSX, Vue, Sass, dentre outros. Veja no **sidebar**
[dessa página](https://parceljs.org/getting_started.html), na sessão
"Asset types".

## O que **pode** ser utilizado

Para o visual da aplicação:

- Bootstrap (já instalado)
- Sass

Para a lógica de aplicação:

- Vanilla JS
- TypeScript
- Vue
- React
- jQuery (caso queira utilizar algum componente do Bootstrap)

É recomendado consultar [essa página](https://parceljs.org/recipes.html) para
ver como os itens acima podem ser utilizados com o Parcel.

Embora **não** seja critério de classificação, recomendamos o
[BEM](http://getbem.com/) como metodologia de nomeação.

## Sobre teste de aplicação

Os testes são **opcionais**, porém desejáveis. Recomendamos utilizar o Jest,
mas outras ferramentas também serão aceitas. Essa aplicação **não** entrega
estrutura de testes pronta devido ao grande número de cenários e ferramentas
diferentes.

## Instruções para rodar o projeto

### Como iniciar o servidor de desenvolvimento

Antes de começar, é necessário ter o Node e o NPM instalados na sua máquina.
Abra o terminal e, na pasta do projeto rode:

1. `npm install` - para instalar as dependências (só precisa rodar uma vez)
1. `npm run dev` - para iniciar o servidor em
   [http://localhost:1234](http://localhost:1234)

Ao alterar um _asset_, sua página irá atualizar automaticamente ✨.

# O projeto

Você será responsável por fazer uma pequena aplicação web para montar refeições baseado em ingredientes previamente informados.

## Layout

Você recebeu um arquivo de layout por e-mail. É recomendado abrí-lo antes de prosseguir.
Baixe o Adobe XD [aqui](https://www.adobe.com/br/products/xd.html).

Esse arquivo contém apenas a versão mobile da aplicação, isso é proposital. Fique à vontade para adaptar a aplicação para _desktop_, caso queira, contudo, não será critério de avaliação.

Para ver as interações propostas, abra o arquivo no XD e pressione Ctrl + Enter (ou Cmd + Enter no Mac).

### Sobre a tela principal de montagem

1. Uma refeição tem três divisórias disponíveis para você inserir ingredientes nelas;
1. Ingredientes possuem uma tabela nutricional;
1. Ingredientes podem ser incrementados/decrementados de 50 em 50g;
1. É possível pedir mais de uma refeição igual através do widget "Quantidade de refeições";
1. O resumo da refeição, na sessão de "Valores totais" deve conter a soma dos valores nutricionais dos ingredientes escolhidos nos pratos.

### Sobre o modal de adição de ingredientes

1. Cada ingrediente _pertence_ a uma categoria, como: gorduras, proteínas, carboidratos, etc, que são listadas em forma de accordion no modal;
1. Ao clicar no botão "+", à direita do ingrediente, o mesmo será adicionado à divisória escolhida. Esse botão age como um checkbox, logo, terá dois estados: checked e unchecked, como proposto no layout;
1. O botão vermelho abaixo do modal serve para fechá-lo.

### Estrutura de dados de exemplo:

Recomendamos que você faça um JSON mock desses dados para alimentar a aplicação.
_Não_ se apegue a fatos nos dados, não avaliaremos isso. Você poderá utilizar a
seguinte estrutura de dados como exemplo para preencher as categorias de
ingredientes e os ingredientes em si:

```javascript
{
  categories: [
    {
      name: "Proteínas",
      slug: "proteinas",
      ingredients: [
        {
          id: 1,
          name: "File Mignón Grelhado",
          // Não se preocupe com a foto, todas podem ser placeholders
          photo: "//placehold.it/256x256",
          nutritionFacts: [
            {
              name: "Carboidratos",
              value: 20,
              // Valor diário, em %
              dv: 12,
            },
            {
              name: "Calories",
              value: 1660,
              dv: 8,
            },
            // Outras informações nutricionais
          ],
        },
      ],
    },
  ];
}
```

## Dúvidas

Caso tenha alguma dúvida, entre em contato com o e-mail que te enviou o teste que nós responderemos o mais rápido possível.
