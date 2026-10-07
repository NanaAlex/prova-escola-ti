## constitution.md

```markdown
# Constitution — Regras persistentes do projeto

1. Identificadores em português.
2. Constantes em letras maísculas.
3. Valores monetários sempre em centavos, como número inteiro.
4. Cobra por fração de minuto, sempre arredondando para cima.
5. API REST, recurso conforme o contrato do enunciado(`/bilhetes`).

6. Datas em ISO 8601 com fuso horário.
7. Placa com 7 caracteres alfanuméricos, em maiúsculas.
8. IDs inteiros sequenciais, começando em 1.
9. Erros: 422 Formato inválido 
          404 não encontrado 
          409 conflito.
10. Todo requisito da spec deve ter pelo menos um teste correspondente.
12. Antes de implementar, rodar `python scripts/variante.py` para definir a variante do projeto.
```
