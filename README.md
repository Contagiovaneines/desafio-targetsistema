# Soluções de Problemas

Este documento contém as soluções para uma série de problemas básicos, incluindo verificações de Fibonacci, contagem de letras em uma string, e questões matemáticas e lógicas.

## 1) Verificar se um número pertence à sequência de Fibonacci

Codigo completo nos arquivos
```
<script>
        function isFibonacci(num) {
            if (num < 0) return false;
            let a = 0, b = 1;
            while (a < num) {
                [a, b] = [b, a + b];
            }
            return a === num;
        }

        function verificarFibonacci() {
            const numero = document.getElementById('numero').value;
            const resultado = document.getElementById('resultado');
            
            if (isFibonacci(Number(numero))) {
                resultado.textContent = `O número ${numero} pertence à sequência de Fibonacci.`;
            } else {
                resultado.textContent = `O número ${numero} não pertence à sequência de Fibonacci.`;
            }
        }
    </script>
```
## 2) Verificar a existência e a quantidade da letra 'a' em uma string
Codigo completo nos arquivos
```
<script>
        function contarLetraA(texto) {
            return (texto.match(/a/gi) || []).length;
        }

        function contarLetrasA() {
            const texto = document.getElementById('texto').value;
            const resultado = document.getElementById('resultado');
            
            const quantidadeA = contarLetraA(texto);
            resultado.textContent = `A letra 'a' aparece ${quantidadeA} vez(es) na string.`;
        }
    </script>
```

## 3) Valor da variável SOMA após a execução do código

Dado o código abaixo:

```
int INDICE = 12, SOMA = 0, K = 1;
while (K < INDICE) {
    K = K + 1;
    SOMA = SOMA + K;
}
print(SOMA);
```

O valor final da variável `SOMA` após a execução do código é **77**.

## 4) Completar os próximos elementos das sequências

### a) Sequência: 1, 3, 5, 7, ___
   - Padrão: Números ímpares consecutivos. Próximo número: **9**

### b) Sequência: 2, 4, 8, 16, 32, 64, ____
   - Padrão: Multiplicação por 2. Próximo número: **128**

### c) Sequência: 0, 1, 4, 9, 16, 25, 36, ____
   - Padrão: Quadrados perfeitos (n²). Próximo número: **49** (7²)

### d) Sequência: 4, 16, 36, 64, ____
   - Padrão: Quadrados de números pares (2², 4², 6², 8²). Próximo número: **100** (10²)

### e) Sequência: 1, 1, 2, 3, 5, 8, ____
   - Padrão: Sequência de Fibonacci. Próximo número: **13**

### f) Sequência: 2, 10, 12, 16, 17, 18, 19, ____
   - Padrão: Números que não contêm o dígito 1 na sua forma decimal. Próximo número: **20**
```
// a) 1, 3, 5, 7, ___
const proximoElementoA = 7 + 2; // 9

// b) 2, 4, 8, 16, 32, 64, ____
const proximoElementoB = 64 * 2; // 128

// c) 0, 1, 4, 9, 16, 25, 36, ____
const proximoElementoC = 36 + 12 + 1; // 49

// d) 4, 16, 36, 64, ____
const proximoElementoD = 8 * 8; // 100

// e) 1, 1, 2, 3, 5, 8, ____
const proximoElementoE = 8 + 5; // 13

// f) 2, 10, 12, 16, 17, 18, 19, ____
const proximoElementoF = 19 + 1; // 20

console.log(proximoElementoA);
console.log(proximoElementoB);
console.log(proximoElementoC);
console.log(proximoElementoD);
console.log(proximoElementoE);
console.log(proximoElementoF);
```
## 5) Identificar qual interruptor controla cada lâmpada

Para identificar qual interruptor controla qual lâmpada:

1. **Ligue o primeiro interruptor** e deixe-o ligado por alguns minutos para que a lâmpada associada aqueça.
2. **Desligue o primeiro interruptor** e **ligue o segundo interruptor**.
3. **Vá até as salas das lâmpadas** e observe:
   - A lâmpada que está acesa está conectada ao segundo interruptor.
   - A lâmpada que está apagada, mas quente, está conectada ao primeiro interruptor.
   - A lâmpada que está apagada e fria está conectada ao terceiro interruptor.

```
