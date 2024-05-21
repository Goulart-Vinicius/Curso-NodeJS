### Módulos em JavaScript

**Módulos** são arquivos que contêm funcionalidades próprias e isoladas. Usamos módulos para organizar e dividir o código em partes menores, tornando-o mais gerenciável, reutilizável e de fácil manutenção.

#### Exemplo de Modularização
Imagine que você precisa criar uma calculadora. Colocar todas as funções (adição, subtração, multiplicação, divisão) em um único arquivo pode tornar o código longo, lento e confuso. Com a modularização, você pode criar um arquivo separado para cada operação e, em seguida, chamá-los de um arquivo principal.

#### Tipos de Modularização
Em JavaScript, existem basicamente dois tipos de modularização:
1. **CommonJS**: Usado principalmente com Node.js.
2. **ESM (ECMAScript Modules)**: Usado em navegadores e está ganhando popularidade no Node.js também.

#### Exportação e Importação
- **Exportação**: Disponibiliza variáveis, funções, classes, etc., para fora de um módulo.
- **Importação**: Usa variáveis, funções, classes, etc., exportados de um módulo.

#### Exportação com CommonJS
Para exportar algo usando CommonJS, utilizamos `module.exports`.

**Exemplos:**
1. Exportar uma variável:
    ```javascript
    const numero = 3;
    module.exports = numero;
    ```

2. Exportar um array:
    ```javascript
    const nome = "Vinicius";
    const idade = 27;
    const sexo = "Masculino";
    module.exports = [nome, idade, sexo];
    ```

3. Exportar uma função:
    ```javascript
    const soma = function (a, b) {
        return a + b;
    };
    module.exports = soma;
    ```

4. Exportar uma função anônima:
    ```javascript
    module.exports = (nome) => {
        console.log(nome);
    };
    ```

Estes são apenas alguns exemplos. Existem outras formas de exportação que você poderá explorar com o tempo.

#### Importação com CommonJS
Para importar algo em CommonJS, utilizamos `require`.

**Exemplo:**
```javascript
const soma = require("./soma.js");
```
A função require recebe como parâmetro o caminho para o arquivo que será importado.