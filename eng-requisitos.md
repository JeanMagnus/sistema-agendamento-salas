# Engenharia de Requisitos

* 'casos de uso'
* 'diagrama de casos de uso'
* 'histórias de usuário (US)'


## Casos de uso

***Ator: Usuário (Aluno)***

**CRIAR CONTA**

*Fluxo normal*

1. Aluno informa nome
2. Aluno informa matrícula
3. Aluno informa e-mail
4. Aluno informa senha

*Extensões:*

- 2a. Se a matrícula for inválida, informar novamente
- 3a. e-mail inválido, informar novamente
- 3b. e-mail não cadastrado


**SOLICITAR SALA**

*Fluxo normal*

1. Aluno visualiza lista de salas disponíveis
2. Aluno escolhe sala disponível
3. Aluno escolhe horário e dia disponível para a sala escolhida
4. Aluno descreve motivo da reserva
5. Aluno confirma o envio da solicitação
6. Aluno aguarda a confirmação de um Administrador para o uso da sala

*Extensões:*

- 2a. Se nenhuma sala estiver disponível, o sistema informará.
- 6a. Caso o agendamento for feito fora do horário de trabalho, o sistema informará o horário útil até a confirmação.


**CANCELAR AGENDAMENTO**

*Fluxo normal*

1. Aluno visualiza as salas que foram agendadas
2. Aluno escolhe escolhe agendamento de sala que deseja cancelar
3. Aluno descreve o motivo do cancelamento
4. Aluno descreve motivo da reserva
5. Aluno confirma o cancelamento

---

***Ator: Usuário (Professor)***

**SOLICITAR SALA**

*Fluxo normal*

1. Professor visualiza lista de salas disponíveis
2. Professor escolhe sala disponível
3. Professor escolhe horário e dia disponível para a sala escolhida
4. Professor confirma o envio da solicitação

*Extensões:*

- 2a. Se nenhuma sala estiver disponível, o sistema informará.


**CANCELAR AGENDAMENTO**

*Fluxo normal*

1. Professor visualiza salas agendadas
2. Professor escolhe sala que deseja cancelar agendamento
3. Professor descreve o motivo do cancelamento
4. Professor confirma o cancelamento


**INFORMAR PROBLEMAS NA SALA**

*Fluxo normal*

1. Professor informa sala utilizada
2. Professor descreve problemas encontrados
3. Professor confirma descrição de problemas na sala


---


***Ator: Admnistrador (Bolsista)***


**CADASTRAR PROFESSOR**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de cadastramento de professor 
3. O administrador informa nome de professor 
4. O administrador informa senha de professor 
5. O administrador informa email de professor 

*Extensões:*

- 5a. E-mail inválido, informar novamente.


**GERENCIAR PROFESSORES**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de gerenciamento de professores 
3. O administrador pode cadastrar professor
4. O administrador pode editar informações do professor
5. O administrador pode remover professor 


**CADASTRAR SALA**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de cadastramento de salas
3. O administrador informa o setor da sala
4. O administrador informa o bloco da sala
5. O administrador informa o número de identificação da sala
6. O administrador informa o status de uso da sala 


**GERENCIAR SALAS**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de salas
3. O administrador visualiza lista de salas cadastradas
4. O administrador pode Cadastrar salas
5. O administrador pode visualizar as solicitações de agendamento
6. O administrador pode visualizar problemas informados sobre as salas
7. O administrador pode excluir uma sala cadastrada


**VISUALIZAR SOLICITAÇÕES DE AGENDAMENTO**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de solicitações
3. O administrador visualiza a lista de solicitações 
4. O administrador pode confirmar/indeferir solicitação


---


***Ator: Sistema***


**AUTENTICAÇÃO**

*Fluxo normal*

1. O usuário acessa a página de login do sistema
2. O sistema exibe campos de entrada para email e senha
3. O usuário preenche os campos com email e senha
4. O usuário clica em login enviando as informações
5. O sistema valida as credenciais fornecidas
6. Se as credenciais são as corretas, sistema redireciona usuário para página personalizada que será diferente dependendo do tipo de usuário
7. Se as credenciais estão incorretas, sistema exibe mensagem de erro   


**NOTIFICAR USUÁRIOS**

*Fluxo normal*

1. O sistema verifica as solicitações de salas
2. O sistema notifica usuário caso seja confirmada sua solicitação
3. O sistema notifica usuário agendador quando chega o dia do agendamento 
4. O sistema notifica usuário que informou o problema quando consertado


**NOTIFICAR ADMINISTRADOR**

*Fluxo normal*

1. O sistema notifica ao Administrador caso algum usuário informe problema
2. O sistema notifica ao Administrador caso seja agendada uma sala

## Diagrama de casos de uso (UML)


![]()


## Histórias de usuário (US)