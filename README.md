```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>
<body>
    <!-- Título da página -->
    <h2>Calculadora de Fatorial e Verificador de Número Primo</h2>

    <!-- Entrada de número -->
    <label for="numero">Digite um número:</label>
    <input type="number" id="numero">
    
    <!-- Botão para calcular o fatorial e verificar se o número é primo -->
    <button onclick="calcular()">Calcular</button>

    <!-- Resultado da operação -->
    <p id="resultado"></p>

```Javascript
        function calcularFatorial(n) {
            if (n === 0) {
                // Caso base, fatorial de 0 é 1
                return 1;
```
 > Função para calcular o fatorial de um número

```       
            } else {
                // 
                return n * calcularFatorial(n - 1);
            }
        }
```
>Chamada recursiva para calcular o fatorial (n * fatorial de n-1)

        
        function verificarNumeroPrimo(numero) {
            if (numero <= 1) {
                // Números menores ou iguais a 1 não são primos
                return false;
   
         }

>Função para verificar se um número é primo

```
            for (let i = 2; i <= Math.sqrt(numero); i++) {
                 if (numero % i === 0) {
```             
>Verifica se o número é divisível por qualquer número entre 2 e a raiz quadrada de 'numero'

```
                    return false;
                }
            }
```
>Se for divisível, não é primo
```
            return true;
        }
```
>Se passar por todos os testes, é primo

```
        function calcular() {
            
```
> Função principal que chama as funções de fatorial e número primo

```
            let numero = parseInt(document.getElementById("numero").value);
```
> Obtém o número inserido no campo de entrada
```
            
            let fatorial = calcularFatorial(numero);
            let primo = verificarNumeroPrimo(numero);
```
> Calcula o fatorial e verifica se o número é primo
```
            document.getElementById("resultado").innerHTML =
                "O fatorial de " + numero + " é " + fatorial + "<br>" +
                "O número " + numero + (primo ? " é primo." : " não é primo.");
        }
    </script>
</body>
</html>
```      
> // Exibe o resultado no parágrafo de id "resultado"

## Questões para Reflexão

### 1. Após a formatação e adição dos comentários, o código ficou mais organizado, facilitando a compreensão de cada função e seu papel no sistema. Além disso, a indentação correta ajudou a visualizar melhor a estrutura hierárquica das funções e suas interações. A legibilidade foi aprimorada, o que é fundamental para manutenção futura.

### 2. A rastreabilidade no código garante que, no futuro, qualquer desenvolvedor ou programador possa compreender facilmente o propósito de cada parte do código e as interações entre elas. Isso é crucial para a manutenção de sistemas, pois facilita o entendimento do fluxo de trabalho, permite identificar rapidamente problemas e possibilita a implementação de novas funcionalidades sem comprometer o funcionamento existente.

### 3. Algumas práticas essenciais para garantir um código bem documentado incluem:

- **Uso de comentários claros e objetivos:** Sempre que necessário, explique o que uma parte do código faz e por que foi implementada de determinada forma.
- **Nomenclatura adequada:** Usar nomes de variáveis e funções que sejam autoexplicativos e reflitam claramente o que elas representam.
- **Estruturação de código com boas práticas de indentação:** Utilizar uma indentação consistente e organizada ajuda a visualizar a hierarquia do código.
- **Documentação externa:** Usar ferramentas como Markdown para gerar documentação completa, descrevendo como o código funciona e o raciocínio por trás das escolhas feitas.

### 4.O uso do Markdown facilita a criação de documentos legíveis e bem formatados, sem a necessidade de ferramentas complexas. Ele permite que a documentação seja organizada, com suporte para títulos, listas, links e outros recursos de formatação. Além disso, o Markdown é amplamente aceito em repositórios de código (como GitHub), tornando-o uma escolha ideal para a documentação técnica de projetos.

### 5.A padronização e boas práticas garantem que todos os desenvolvedores sigam uma estrutura comum ao escrever o código, o que facilita o trabalho em equipe, a identificação de erros e a adição de novas funcionalidades. A manutenção se torna mais simples, pois qualquer alteração pode ser compreendida rapidamente por outros membros da equipe, e a escalabilidade do sistema é facilitada, pois o código é escrito de forma modular e bem estruturada, permitindo que novos recursos sejam integrados sem complicações.

