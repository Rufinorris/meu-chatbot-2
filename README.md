# Vale a pena a proposta?

Simulador de remuneração total (CLT) para comparar a sua situação atual com uma
proposta recebida. Página única, sem dependências: abra o `index.html` no navegador.

## O que ele calcula

Para cada cenário (**Situação atual** e **Proposta recebida**):

| Entrada | Observação |
| --- | --- |
| Salário mensal bruto | 12 salários + 13º + 1/3 de férias |
| Bônus anual | alvo em % do salário anual × atingimento esperado |
| ILP | valor total do grant ÷ anos de vesting; tributável como salário ou 15% |
| Previdência privada | aporte da empresa e aporte próprio (deduz IRRF até 12%, regra do PGBL) |
| Benefícios mensais | lista editável (VR/VA, saúde, odonto, home office, educação…) |
| Descontos mensais | coparticipação, vale-transporte, mensalidade do plano |

E devolve três números anuais:

- **Remuneração total (total comp)** — salário + 13º/férias + bônus + ILP + previdência da empresa + benefícios + FGTS.
- **Líquido no bolso** — o que cai na conta no ano, com INSS e IRRF descontados mês a mês, no 13º, no mês das férias e na margem sobre bônus e ILP.
- **Valor percebido** — o líquido mais o que não passa pelo contracheque (benefícios, previdência da empresa, FGTS). É o número que compara duas propostas.

Além disso: composição do pacote separando o que é garantido do que é variável,
diferença componente a componente, alíquota efetiva e o **ponto de equilíbrio** —
o salário que a proposta precisaria ter para empatar com a situação atual.

## Premissas fiscais

Tabelas de INSS e IRRF mensais vigentes em 2025/2026, desconto simplificado,
dedução por dependente e o redutor do IRRF da Lei 15.270/2025 (isenção até
R$ 5.000). **Todos os parâmetros são editáveis** no painel "Parâmetros fiscais e
premissas" — confirme os valores vigentes antes de decidir.

Os dados ficam salvos apenas no `localStorage` do seu navegador. Nada é enviado
para lugar nenhum.

> Estimativa para orientar a decisão. Não é aconselhamento fiscal, contábil ou jurídico.
