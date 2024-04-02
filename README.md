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

Também é possível inserir fluxo de programa no HTML, como questões condicionais, conforme já fazíamos no JavaScript, igual ao exemplo a seguir:

```js
<HTML>
    <BODY>
        <p id="demo"></p>

        <script>
            if(valorCorrente > 3){
                document.getElementById("demo").innerHTML = "Hello World!";
            }
        </script>
    </BODY>
</HTML>
```
No entanto, veja como é muito mais simples fazer a mesma atividade acima utilizando a linguagem **C#** com a sitaxe **razor** no HTML:

```razor
<HTML>
    <BODY>
        @if(valorCorrente > 3)
        {
            <p> Hello World! </p>
        }
    </BODY>
</HTML>
```

## 4 Tratamento de eventos

Eventos clássicos do DOM como *onload*, *onclick*, *onchange*, etc, podem ser executados no HTML através da sintaxe blazor, conforme o exemplo abaixo que ao clicar no mouse uma função de incremento é executada em C#:

```razor
<button @onclick="IncrementaConta"> Clique </button>

@code {
    private int Conta = 0;

    private void IncrementaConta()
    {
       Conta += 1;
    }
}
```
## 5 Vinculação de dados

o atributo `@bind` permite que seja criado um **vínculo bidirecional** do valor que um elemento do DOM tanto recebe quanto exibe par o usuário. Caso o valor desse elemento seja alterado no DOM, ele será atualizado automaticamente no código, e caso seja alterado no código, será também automaticamente atualizado no DOM.[^1]  

```razor
<input @bind="text" />

    <button @onclick="() => text = string.Empty">Clear</button>

<p>@text</p>

@code {
    string text = "";
}
```

[^1]: Recursos de vinculação [Binding features](https://learn.microsoft.com/en-us/aspnet/core/blazor/components/data-binding?view=aspnetcore-8.0)
## 6 Criação da Lista

### 6.1 Adição de um componente

## 7 Material de suporte

## 8 Agradecimento

## 9 Data

2 de abril de 2024.