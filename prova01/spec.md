
```markdown
## Contrato REST

| Método | Rota | Descrição | Sucesso | Erros |
| --- | --- | --- | --- | --- |
| POST | /bilhetes | Abrir bilhete | 201 + JSON com id | 422 (entada_invalida) |
| POST | /bilhetes/{id}/encerramento | Encerrar bilhete | 200 + JSON com id | 409 (bilhete_ja_encerrado) |
| GET | /bilhetes/ativos | Listar ativos | 200 + array | 404 (bilhete_nao_encontrado) |
| GET | /relatorios/diario?data=AAAA-MM-DD | Relatório diário | 200 | - |
| POST | /bilhetes/{id}/cancelamento | Cancelar bilhete | 200 + status: "cancelados" | 409 (bilhete_ja_encerrado) |
| GET | /bilhetes?placa=ABC1D23| Histórico por placa | 200 + status | - |

| POST | POST /bilhetes | Uma vaga por placa | 409 | 409(bilhete_em_aberto) |

Convenções: datas ISO 8601, IDs inteiros sequenciais.

## Entidades

- Bilhetes: id (int), placa (string, obrigatório), entrada (string), saida (string), minustos(int), valor_centavos(int).
