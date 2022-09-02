# Curso-de-AngularJS
AngularJS📚🅰️-Repositório criado para estudar o framework AngularJS
Clique aqui para acessar o código fonte da aula desejada
- [Aula 1](https://github.com/lramon2001/Curso-de-AngularJS/blob/main/aula1.html)
- [Aula 3](https://github.com/lramon2001/Curso-de-AngularJS/blob/main/aula3.html)

## Aula 1-Como iniciar uma aplicação Angular e criar módulos

Para iniciar uma aplicação Angular Js basta adicionar a biblioteca no template usando uma tag script 

```html
  <script src="http://cdnjs.cloudflare.com/ajax/libs/angular.js/1.6.4/angular.min.js"></script>
```

Para criar um módulo basta utilizar a função module passando o nome que deseja para o módulo e as dependências do modulo no array

```html
<script>
    angular.module('myApp',[]);
</script>

```

## Aula 2- Iniciando o projeto

Neste curso desenvolveremos uma aplicação angular. A aula 2 foi destinada a configuração do ambiente e estruturação do projeto.

## Aula 3- Como usar o ng-init, ng-if,  ng-show e ng-hide

Para usar o ng-init basta usar esta sintaxe. O navegador exibirá "o valor de a é 5"
```html
  <div ng-init="a=5"> 
  
    O valor de a é {{a}}
  
  </div>
  
```
Para usar o ng-if basta usar esta sintaxe. O navegador exibirá "FACE UP, MAKE YOUR STAND. REALIZE, YOU ARE LIVING ON THE GOLDEN YEARS" pois o valor da varievel visivel é true. Outras diretivas similares são ng-show e ng-hide. Mas por questões de segurança é fortemente aconselhável utilizar o ng-if
```html
  <div ng-init="visivel=true">
    <div ng-if="visivel">
      <span>
        FACE UP, MAKE YOUR STAND. REALIZE, YOU ARE LIVING ON THE GOLDEN YEARS
      </span>
    </div>
  </div>
```
Outro recurso muito útil é o ng-repeat que consegue apresentar uma lista, na sintaxe que apresentarei vou utilizar a clásula track by para poder repetir itens
```html
<ul ng-init="lista = [1,2,3,4,5,6,6,7,8]">
  <li ng-repeat="item in lista track by $index">
          indice:{{$index}}- item:{{item}}
  </li>
</ul>
```

## Aula 4 - Como usar o ng-style e o ng-click

Para usar o ng-style primeiro devemos criar uma variavel json com o estilo que desejamos adotar. Depois atribuimos esta variavel ao ng-style. Já o ng-click devemos declarar o evento que esperamos. Fica mais fácil com a demonstração em código. Se julgar necessário, repita ai no seu navegador
```html
<div ng-init= "meuEstilo = {'color': 'green'}">
  <span ng-style = "meuEstilo"> O Hexa vem </span>
  <button ng-click="meuEstilo = {'color':'yellow'}">Clique aqui </button>
</div>
```

## Aula 5 - Como utilizar controllers

- Controller é a camada da arquitetura que deve conter a implementação da lógica e o envio de dados para os nossos templates;
- Para o Angular, um controller basicamente é uma função construtora com um objeto chamado $scope;
- $scope representa o meio campo entre um controller e uma view;
- $scope é capaz de passar variáveis e até mesmo funções do controller para a view. O inverso também é válido: é possível repassar informações da view para o controller utilizando o $scope.

Exemplo de controller:

```js
var app = angular.module('App',[]);

app.controller('ExemploController', ['$scope', function($scope) {
  $scope.greeting = 'Ola!';
}]);

```
A aula 5 foi longa e cheia de informações. Por isso optei por listar explicando as etapas

- Criar o arquivo app.js com o seguinte código criando o módulo

```js
  angular.module('myApp',[]);
```

- 
