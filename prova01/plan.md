```markdown
## Stack
- Python.

## Contrato que o código deve respeitar
- Rotas: /bilhetes.
- Campos JSON: id, placa, entrada, saida, minutos, valor_centavos, data, status.
- Status: 201 Abrir, 200 Encerrar, 200 Listar, 409 bilhete em aberto, 422 placa invalida, 422 entrada invalida, 422 data invalida, 404 bilhete nao encontrado, 409 bilhete nao encontrado, 409 bilhete nao aberto, 409 bilhete em aberto.

## Estrutura de arquivos
variante.py       # api e rotas

## Decisões
1. Levantando erro com 422/404/409.
2. Entrada:ISO-8601 com fuso - 03:00(Opcional).
3. Passado: quando presente, o bilhete abre naquele instante em vez de "agora". É o gancho de testabilidade da correção — sem ele, testar fração/teto exigiria esperar tempo real. Formato inválido.

5. Tolerancia de minutos: Passou da tolerância (mesmo por 1 minuto) → cobra integral desde o primeiro minuto — a tolerância não é descontada.

6. Cancelamento: Só bilhetes abertos podem ser cancelados — sem cobrança (não gera saida nem valor_centavos).

8. IDs: contador inteiro por entidade, começando em 1.

9. Placa: 7 caracteres alfanuméricos, maiúsculos. FRACAO_MINUTOS minutos, arredondando para cima (fração exata cobra 1 fração; 1 minuto a mais já cobra a fração seguinte).
10. hora cheia = TARIFA_HORA_CENTAVOS; valor da fração = tarifa ÷ (60 ÷ FRACAO_MINUTOS);
```
