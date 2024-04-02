# Módulo 3: Web Blazor

[Criar uma lista de tarefas pendentes com o Blazor](https://learn.microsoft.com/pt-br/training/modules/build-blazor-todo-list/)


## 1 Objetivos de aprendizagem

- Aprender a lidar com eventos de componentes e configurar associações de dados bidirecionais;
- Criar uma página de lista de tarefas pendentes.

## 2 Renderização de valores de expressão C#

Assim como exibimos (renderizamos) o valor de uma variável do JavaScript no código HTML, podemos fazer o mesmo com a sintaxe **razor** para reonhecer código **C#** de uma forma muito fácil, para isso, basta concatenar antes da variável o símbolo "@", conforme abaixo:

```razor
<span> o valor resultante é: @variavel </span>
```

Mesmo que não deixemos explicitado que finalizou o código em C# o **razor** consegue fazêe-lo,contudo, podemos colocar a variável em questão entre parênteses após o "@":

```razor
<span> o valor resultante é: @(variavel) </span>
```

## 3 Adição de fluxo de controle

Também é possível 

```js
<p id="demo"></p>

<script>
    if(valorCorrente > 3){
        document.getElementById("demo").innerHTML = "Hello World!";
    }
</script>
```

```razor
@if(valorCorrente > 3)
{
    <p> Hello World! </p>
}
<>
```

## 4 Tratamento de eventos


## 5 Vinculação de dados

## 6 Criação da Lista


## 7 Material de suporte

## 8 Agradecimento

## 9 Data

2 de abril de 2024.