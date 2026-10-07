```markdown
# Tasks — Decomposição

- [ ] T01: Rodar `python scripts/variante.py` e anotar os valores (TARIFA_HORA_CENTAVOS, FRACAO_MINUTOS, tolerância).
- [ ] T02: Instalar Flask e pytest.
- [ ] T03: Criar `app.py` e `tests/test_bilhetes.py` vazios.
- [ ] T04: Definir as constantes da variante no `app.py`.

- [ ] T05: [Teste] Abrir bilhete com placa válida retorna 201 e id = 1.
- [ ] T06: [Teste] IDs seguem sequência (1, 2, 3...).
- [ ] T07: [Teste] Bilhete aberto tem saida, minutos e valor_centavos como null.
- [ ] T08: [Código] Implementar POST /bilhetes até T05–T07 passarem.

- [ ] T09: [Teste] Placa com menos ou mais de 7 caracteres → 422.
- [ ] T10: [Teste] Placa com minúsculas ou símbolos → 422.
- [ ] T11: [Teste] Campo entrada com formato inválido → 422.
- [ ] T12: [Teste] Campo entrada válido abre o bilhete naquele instante.
- [ ] T13: [Teste] Placa que já tem bilhete aberto → 409.
- [ ] T14: [Código] Implementar as validações até T09–T13 passarem.

- [ ] T15: [Teste] Listagem vazia retorna 200 e lista vazia.
- [ ] T16: [Teste] Listagem retorna os bilhetes abertos.
- [ ] T17: [Código] Implementar GET /bilhetes.

- [ ] T18: [Teste] Encerrar bilhete aberto retorna 200 com saida, minutos e valor_centavos preenchidos.
- [ ] T19: [Teste] Dentro da tolerância → valor_centavos = 0.
- [ ] T20: [Teste] Passou 1 minuto da tolerância → cobra desde o primeiro minuto.
```
