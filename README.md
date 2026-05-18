# Estudante - Cálculo de Média

Este projeto contém um script em Python chamado `calcular_media` que avalia o desempenho de um estudante com base em três critérios:

- foco
- dedicação
- persistência

Cada valor deve estar entre **0 e 10**.

---

## Como o código funciona

### 1) Classe `Estudante`
A classe guarda os três valores informados e possui o método:

- `calcular_media()`
  - calcula a média aritmética: `(foco + dedicacao + persistencia) / 3`
  - retorna a média
  - lança `ValueError` se a média for maior que 10

---

### 2) Função `avaliar_estudante(foco, dedicacao, persistencia)`
Essa função concentra a regra de negócio:

1. Valida se todos os valores estão entre 0 e 10.
2. Cria um objeto `Estudante`.
3. Calcula a média.
4. Retorna:
   - `"Reprovado"` se média < 6
   - `"Aprovado"` se média >= 6

Essa separação facilita testes e reutilização da lógica sem depender de entrada interativa.

---

### 3) Função `main()`
A função `main()` executa o modo interativo:

- pede os três valores para o usuário
- chama `avaliar_estudante(...)`
- imprime o resultado
- repete o processo em caso de erro (`ValueError`)

O trecho:

```python
if __name__ == "__main__":
    main()
```

faz com que o programa interativo rode apenas quando o arquivo é executado diretamente.

---

## Regras de aprovação

- **Média < 6** → `Reprovado`
- **Média >= 6** → `Aprovado`

---

## Como executar

No terminal, dentro da pasta do projeto:

```bash
python3 calcular_media
```

Digite os valores quando solicitado.

---

## Exemplo de uso

Entradas:

- foco: `8`
- dedicação: `7`
- persistência: `9`

Saída esperada:

```text
Aprovado
```

---

## Estrutura atual do projeto

- `calcular_media`: script principal com classe, regras de avaliação e modo interativo.
- `README.md`: documentação do funcionamento.
