# excel_declaracao
Ideia de modelo de declaração de imposto de renda usando excel

1. Estrutura Básica do Formulário
Crie as seguintes abas (planilhas) no Excel:

Dados Pessoais (Nome, CPF, Endereço, etc.)

Rendimentos (Salários, Aluguéis, Dividendos, etc.)

Despesas Dedutíveis (Saúde, Educação, Dependentes, etc.)

Resumo (Cálculo do imposto devido ou restituição)

2. Modelo Simplificado
Planilha "Dados Pessoais"
Campo	Valor
Nome Completo	[____________________]
CPF	[____________________]
Data de Nascimento	[______]
Endereço	[____________________]
Planilha "Rendimentos"
Fonte de Renda	Valor (R$)
Salário	[__________]
Aluguéis	[__________]
Dividendos	[__________]
Total Rendimentos	=SOMA(B2:B4)
Planilha "Despesas Dedutíveis"
Tipo de Despesa	Valor (R$)
Saúde	[__________]
Educação	[__________]
Previdência Oficial	[__________]
Total Deduções	=SOMA(B2:B4)
Planilha "Resumo"
Descrição	Valor (R$)
Total Rendimentos	=Rendimentos!B5
Total Deduções	=Despesas!B5
Base de Cálculo	=B2-B3 (Rend - Ded)
Imposto Devido	=CalcularImposto(B4)
3. Fórmula para Cálculo do Imposto (Simples)
Na célula "Imposto Devido", você pode usar uma fórmula baseada nas alíquotas da tabela progressiva (exemplo para 2023):

excel
=SE(B4<=1903.98; 0;
 SE(B4<=2826.65; B4*0.075-142.80;
 SE(B4<=3751.05; B4*0.15-354.80;
 SE(B4<=4664.68; B4*0.225-636.13;
 B4*0.275-869.36))))
(Ajuste os valores conforme a tabela vigente)

4. Dicas Extras
Proteja as células com fórmulas (use Revisão > Proteger Planilha).

Validação de Dados: Use Dados > Validação para criar listas suspensas (ex.: tipos de rendimento).

Formatação Condicional: Destaque valores altos ou negativos.

Botões de Ação: Insira botões para imprimir ou salvar (opcional).

Modelo Pronto 
Se quiser um modelo mais completo, você pode baixar um template grátis como:

Receita Federal (Modelo Oficial) > https://www.gov.br/receitafederal/pt-br/assuntos/meu-imposto-de-renda

