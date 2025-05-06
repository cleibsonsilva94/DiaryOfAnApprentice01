# Teste Unitário em Java

## O que é um Teste Unitário?

O teste unitário (ou de unidade) é um tipo de **teste automatizado** que verifica se um trecho específico do código — geralmente uma função ou método — está funcionando corretamente.

> 💡 Ele é sempre executado por código, de forma automática.

---

## Exemplo Prático

Vamos considerar um método simples que soma dois números.

### Método a ser testado

```java
public double somarDoisNumeros(double num1, double num2) {
    return num1 + num2;
}
```

### Teste Unitário

```java
import static org.junit.Assert.assertEquals;
import org.junit.Test;

public class CalculadoraTest {

    @Test
    public void testarSomarDoisNumeros() {
        // Prepara - Arrange
        double num1 = 4;
        double num2 = 5;
        double resultadoEsperado = 9;

        // Executa - Act
        double resultadoAtual = somarDoisNumeros(num1, num2);

        // Valida - Assert
        assertEquals(resultadoEsperado, resultadoAtual, 0.0001);
    }

    // Método sendo testado (caso esteja no mesmo arquivo)
    public double somarDoisNumeros(double num1, double num2) {
        return num1 + num2;
    }
}
```

---

## Estrutura de um Teste Unitário

Todo teste unitário segue três etapas principais:

1. **Arrange (Prepara)** – Configura os dados e o ambiente.
2. **Act (Executa)** – Executa o código a ser testado.
3. **Assert (Valida)** – Verifica se o resultado está correto.

---

## Ferramenta usada

- **JUnit**: framework de testes para Java.

---

### ✅ Vantagens do Teste Unitário

- Garante que o código funciona como esperado.
- Ajuda a evitar bugs futuros.
- Torna a manutenção mais segura.
- Facilita refatorações.
