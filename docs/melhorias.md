# 📈 Melhorias Futuras

## 🔧 **1. Melhorar a performance da query**
- Atualmente, usamos `SELECT` dentro de `SELECT` para buscar marca e ICMS.
- Podemos testar um **`JOIN`** com `PCMARCA` e `PCTRIBUT` para reduzir consultas repetitivas.

## 📊 **2. Tornar a consulta dinâmica para qualquer região**
- Em vez de fixar `NUMREGIAO = 2`, podemos usar uma variável SQL dinâmica:
```sql
AND TABPR_F1.NUMREGIAO = :NUMREGIAO
AND TABPR_F3.NUMREGIAO = :NUMREGIAO
AND TABPR_F6.NUMREGIAO = :NUMREGIAO

- Assim, podemos passar a região como parâmetro e não precisar editar a query sempre.

## 📌 **3. Criar um relatório completo**

- Atualmente, a consulta retorna os dados na tela.
- Podemos criar uma VIEW para facilitar a consulta:

sql
CREATE VIEW VW_PRODUTOS_FILIAIS AS
    (AQUI ENTRA A QUERY ATUAL)

- Assim, podemos simplesmente fazer:

SELECT * FROM VW_PRODUTOS_FILIAIS WHERE CODPROD = 55933;