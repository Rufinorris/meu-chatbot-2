# Vale a pena a proposta?

Simulador de remuneração total (CLT) para comparar a sua situação atual com uma
proposta recebida. Página única, sem dependências e sem back-end: abra o
`index.html` no navegador.

## O que ele calcula

Para cada cenário — **Situação atual** e **Proposta recebida**:

| Entrada | Observação |
| --- | --- |
| Salário mensal bruto | 12 salários + 13º + 1/3 de férias |
| Bônus anual | em reais no ano ou em % do salário anual, × atingimento esperado; tributável como PLR (tabela exclusiva, sem INSS nem FGTS) ou como salário |
| ILP | valor por ano, total do grant ÷ vesting, ou calculado pelo cronograma de vesting; tributável como salário ou a 15% |
| Cronograma de vesting | preço de exercício, preço esperado da ação, câmbio e quantas ações vencem por ano — só o que ainda está em carência |
| Previdência privada | aporte da empresa e o seu, em R$/mês ou % do salário (o seu deduz IRRF até 12%, regra do PGBL) |
| Benefícios mensais | lista editável (VR/VA, saúde, odonto, home office, educação…) |
| Descontos em folha | coparticipação, vale-transporte, mensalidade do plano |
| Empresa | nome que aparece nos gráficos, nas tabelas e no resumo |
| Ao trocar de empresa | bônus/PLR que fica para trás, ILP não vestido e bônus de contratação (só na proposta) |

E devolve três números anuais:

- **Remuneração total (total comp)** — salário + 13º/férias + bônus + ILP + previdência da empresa + benefícios + FGTS.
- **Líquido em folha** — o que cai na conta no ano, com INSS e IRRF descontados mês a mês, no 13º, no mês das férias e na margem sobre bônus e ILP.
- **Líquido + benefícios** — o líquido em folha mais o que não passa pelo contracheque (benefícios, previdência da empresa, FGTS). É o número que compara duas propostas de verdade.

Como o que se perde na saída acontece uma vez só, ele fica fora da comparação
anual e vira um recorte de **primeiro ano**, com o tempo que a troca leva para se
pagar.

Além disso: composição do pacote separando o que é garantido do que é variável,
diferença componente a componente, alíquota efetiva, o **ponto de equilíbrio** — o
salário que a proposta precisaria ter para empatar com hoje — e um **resumo** em
texto corrido, com listas de prós e contras por empresa e um campo de observações
para o que os números não dizem.

A proposta é o cenário em foco: o cartão da situação atual abre recolhido, já que
muda pouco. No celular os dois viram abas, os blocos longos ficam recolhidos e a
barra de veredito acompanha a rolagem.

## Premissas fiscais

Tabelas de INSS e IRRF mensais vigentes em 2025/2026, desconto simplificado,
dedução por dependente, tabela anual da PLR e o redutor do IRRF da Lei
15.270/2025 (isenção até R$ 5.000). **Todos os parâmetros são editáveis** no painel "Parâmetros fiscais e
premissas" — confirme os valores vigentes antes de decidir.

Os dados ficam salvos apenas no `localStorage` do navegador. Nada sai da máquina.

> Estimativa para orientar a decisão. Não é aconselhamento fiscal, contábil ou jurídico.
