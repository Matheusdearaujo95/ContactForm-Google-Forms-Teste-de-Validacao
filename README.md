# ContactForm (Google Forms) – Teste de Validação ✉️

Este repositório documenta o Teste de Validação realizado em um formulário de contato criado no Google Forms, com foco nos campos Nome, E-mail, Assunto e Mensagem. A proposta foi garantir que entradas inválidas fossem bloqueadas e que dados corretos fossem enviados sem problemas, cobrindo uma série de possíveis cenários de uso.

## 1. Contexto do Projeto

O ContactForm é um formulário de contato hospedado no Google Forms que recebe informações do usuário por meio de quatro campos principais:

Nome (Resposta Curta)

E-mail (Resposta Curta, validação de e-mail)

Assunto (Resposta Curta)

Mensagem (Parágrafo)

Cada campo foi marcado como obrigatório, para que o usuário não consiga enviar o formulário sem preencher todas as informações necessárias.

## 2. Escopo e Objetivos

### Escopo
Validação de Campos: Nome, E-mail, Assunto e Mensagem.
Verificação de Formatos: Particularmente no campo E-mail, usando o recurso de Validação de Resposta do Google Forms.
Comportamento em Diferentes Cenários: Campos vazios, caracteres especiais, HTML, limites de texto etc.
### Objetivos Principais
Garantir que o Google Forms exiba mensagens de erro ao detectar entradas inválidas ou campos em branco.
Confirmar que campos válidos sejam aceitos e enviados corretamente.
Documentar todos os cenários de teste (40 ao todo) e seus resultados.
## 3. Ferramentas Utilizadas

Google Forms:	Formulário de contato alvo do teste
Google Sheets / Excel:	Registro de casos de teste e resultados
DevTools:	Observação de erros no console ou na rede (opcional)
Observação: Poderia ter sido utilizado Jira ou Trello para gerenciar possíveis bugs, mas todos os testes foram aprovados sem falhas.
## 4. Metodologia de Teste

### Criação do Formulário
Campos: Nome, E-mail, Assunto, Mensagem
Todos marcados como obrigatórios
Validação de e-mail ativada para o campo E-mail (Google Forms → Validação de resposta → Texto → E-mail)
### Planejamento de Casos de Teste
Foram criados 40 cenários (10 para cada campo), contemplando entradas vazias, caracteres especiais, limites de texto, HTML, entre outros.
Cada cenário foi listado em uma planilha (Excel / Google Sheets), com colunas:
ID, Campo(s), Test Scenario, Passos, Resultado Esperado, Resultado Obtido, Status, Bug ID
### Execução
Para cada caso de teste, preenchemos o Google Forms com os dados indicados (ex.: inserir e-mails incorretos, nomes muito longos etc.).
Observamos se o formulário bloqueava o envio ou exibia mensagem de erro conforme esperado.
### Registro de Resultados
Preenchemos a coluna “Resultado Obtido” e marcamos “Pass” para os testes que corresponderam ao “Resultado Esperado”.
Como não houve falhas, não foram abertos tickets de bug.
## 5. Resultados e Conclusões ✅

### Resultados Gerais
Total de Casos de Teste: 40
Aprovados: 40
Reprovados: 0
Bugs Encontrados: Nenhum
### Conclusões Principais
O Google Forms atendeu de forma satisfatória aos requisitos de validação nos campos obrigatórios, exibindo mensagens de erro claras ao usuário quando necessário.

E-mail: Qualquer formato que não atendesse aos padrões mínimos (@ e domínio) foi rejeitado adequadamente.

Campos Obrigatórios: Ao deixar algum campo vazio, o envio foi bloqueado com a mensagem “Este é um campo obrigatório”.

Entradas Extensas / Caracteres Especiais: Onde não havia limites configurados, o Forms aceitou sem quebrar o layout. Onde havia limite (ex.: 50 caracteres), apresentou aviso ao exceder.

Embora nenhum bug tenha sido encontrado, este processo reforçou a confiabilidade do Google Forms para casos básicos de validação de formulário de contato.

6. Planilha de Testes 📋

A planilha com os 40 testes está disponível neste repositório (ou via link do Google Sheets, caso você prefira). Ela inclui:

ID (Ex.: 1, 2, 3...),

Campo(s) em Teste (Nome, E-mail, Assunto ou Mensagem),

Teste cenário (cenário / condição validada),

Passos (para reproduzir a condição),

Resultado Esperado e Resultado Obtido,

Status (Aprovado/Reprovado) e Bug ID (quando aplicável).
Como todos os casos foram aprovados, a planilha reflete Status = Aprovados em cada cenário.
