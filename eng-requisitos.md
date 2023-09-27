# Engenharia de Requisitos

* `casos de uso`
* `diagrama de casos de uso`
* `histórias de usuário (US)`


## Casos de uso

***Ator: Usuário (Aluno)***

**CRIAR CONTA:**

*Fluxo normal*

1. Aluno informa nome
2. Aluno informa matrícula
3. Aluno informa e-mail
4. Aluno informa senha

*Extensões:*

- 2a. Se a matrícula for inválida, informar novamente
- 3a. e-mail inválido, informar novamente
- 3b. e-mail não cadastrado


**SOLICITAR SALA:**

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


**CANCELAR AGENDAMENTO:**

*Fluxo normal*

1. Aluno visualiza as salas que foram agendadas
2. Aluno escolhe escolhe agendamento de sala que deseja cancelar
3. Aluno descreve o motivo do cancelamento
4. Aluno descreve motivo da reserva
5. Aluno confirma o cancelamento

---

***Ator: Usuário (Professor)***

**SOLICITAR SALA:**

*Fluxo normal*

1. Professor visualiza lista de salas disponíveis
2. Professor escolhe sala disponível
3. Professor escolhe horário e dia disponível para a sala escolhida
4. Professor confirma o envio da solicitação

*Extensões:*

- 2a. Se nenhuma sala estiver disponível, o sistema informará.


**CANCELAR AGENDAMENTO:**

*Fluxo normal*

1. Professor visualiza salas agendadas
2. Professor escolhe sala que deseja cancelar agendamento
3. Professor descreve o motivo do cancelamento
4. Professor confirma o cancelamento


**INFORMAR PROBLEMAS NA SALA:**

*Fluxo normal*

1. Professor informa sala utilizada
2. Professor descreve problemas encontrados
3. Professor confirma descrição de problemas na sala


---


***Ator: administrador (administrador)***


**CADASTRAR PROFESSOR:**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de cadastramento de professor 
3. O administrador informa nome de professor 
4. O administrador informa senha de professor 
5. O administrador informa email de professor 

*Extensões:*

- 5a. E-mail inválido, informar novamente.


**GERENCIAR PROFESSORES:**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de gerenciamento de professores 
3. O administrador pode cadastrar professor
4. O administrador pode editar informações do professor
5. O administrador pode remover professor 


**CADASTRAR SALA:**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de cadastramento de salas
3. O administrador informa o setor da sala
4. O administrador informa o bloco da sala
5. O administrador informa o número de identificação da sala
6. O administrador informa o status de uso da sala 


**GERENCIAR SALAS:**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de salas
3. O administrador visualiza lista de salas cadastradas
4. O administrador pode Cadastrar salas
5. O administrador pode visualizar as solicitações de agendamento
6. O administrador pode visualizar problemas informados sobre as salas
7. O administrador pode excluir uma sala cadastrada


**VISUALIZAR SOLICITAÇÕES DE AGENDAMENTO:**

*Fluxo normal*

1. O administrador acessa o painel de administração
2. O administrador escolhe a seção de solicitações
3. O administrador visualiza a lista de solicitações 
4. O administrador pode confirmar/indeferir solicitação


---


***Ator: Sistema***


**AUTENTICAÇÃO:**

*Fluxo normal*

1. O usuário acessa a página de login do sistema
2. O sistema exibe campos de entrada para email e senha
3. O usuário preenche os campos com email e senha
4. O usuário clica em login enviando as informações
5. O sistema valida as credenciais fornecidas
6. Se as credenciais são as corretas, sistema redireciona usuário para página personalizada que será diferente dependendo do tipo de usuário
7. Se as credenciais estão incorretas, sistema exibe mensagem de erro   


**NOTIFICAR USUÁRIOS:**

*Fluxo normal*

1. O sistema verifica as solicitações de salas
2. O sistema notifica usuário caso seja confirmada sua solicitação
3. O sistema notifica usuário agendador quando chega o dia do agendamento 
4. O sistema notifica usuário que informou o problema quando consertado


**NOTIFICAR ADMINISTRADOR:**

*Fluxo normal*

1. O sistema notifica ao Administrador caso algum usuário informe problema
2. O sistema notifica ao Administrador caso seja agendada uma sala

## Diagrama de casos de uso (UML)


![](https://github.com/JeanMagnus/sistema-agendamento-salas/blob/main/images/casos-de-uso.png)


## Histórias de usuário (US)

***História de usuário (Aluno):***

**Criar conta:**
>*"Como aluno, gostaria de criar uma conta."*
> - Critérios de aceitação:
>  1. O aluno deve ser capaz de inserir seu nome.
>  2. O aluno deve ser capaz de inserir matrícula.
>  3. O aluno deve ser capaz de inserir seu endereço de e-mail.
> 4.  O aluno deve ser capaz de inserir uma senha.
> 5. O aluno deve ser capaz de inserir a confirmação da senha.
> - - A conta do usuário deve ser criada com sucesso; o usuário deve ser capaz de acessar os recursos do sistema.

**Solicitar sala:**

>*“Como aluno,  gostaria de solicitar uma sala.”*
> - Critérios de aceitação:
> 1. O aluno deve ser capaz de selecionar a data e a hora da solicitação.
> 2. O aluno deve ser capaz de selecionar a sala solicitada.
> 3. O aluno deve ser capaz de inserir seu nome.
> 4. O aluno deve ser capaz de inserir o motivo da solicitação.
 > - - A sala deve ser reservada com sucesso; o usuário deve receber uma notificação de confirmação da reserva.

**Cancelar agendamento:**

> *"Como aluno,  gostaria de cancelar agendamento"*
> - Critérios de aceitação:
> - - O agendamento deve ser cancelado com sucesso; o usuário deve receber uma notificação de cancelamento do agendamento.

---


***História de usuário (Professor):***

**SOLICITAR SALA:**

> *“Como professor, gostaria de solicitar sala.”*
> - Critérios de aceitação: 
> 1. O professor deve ser capaz de visualizar salas disponíveis.
>2. O professor deve ser capaz de selecionar a data e a hora da solicitação.
>3. O professor deve ser capaz de selecionar a sala solicitada.
>4. O professor deve ser capaz de inserir seu nome.
>5. O professor deve ser capaz de inserir o motivo da solicitação.
> - - A sala deve ser reservada com sucesso; o professor deve receber uma notificação de confirmação da reserva.

**Informar problemas:**

>*“Como professor, gostaria informar problemas.”*
> - Critérios de aceitação: 
> 1. O professor deve ser capaz de inserir uma descrição detalhada do problema.
>2. O professor deve ser capaz de inserir a data e a hora em que o problema ocorreu.
>3. o professor deve conseguir confirmar descrição.
 > - - O professor deve receber uma notificação de confirmação do registro do problema.

**CANCELAR AGENDAMENTO:**

> *“Como professor, gostaria de cancelar agendamentos.”*
> - Critérios de aceitação: 
> - - O professor deve visualizar salas agendadas; professor de ve escolher sala que deseja cancelar; Professor deve ser capaz de descrever o motivo do cancelamento

---

***História de usuário (Administrador/administrador):***

**Cadastrar professores:**

>*“Como administrador, gostaria de cadastrar professores.”*
> - Critérios de aceitação: 
> 1. O administrador deve ser capaz de acessar o painel de administração.
> 2. O administrador deve ser capaz de escolher a seção de cadastramento de professor. 
> 3. O administrador deve ser capaz de informar nome de professor. 
> 4. O administrador deve ser capaz de informar senha de professor.
> 5. O administrador deve ser capaz de informar email de professor.


**GERENCIAR PROFESSORES:**

> *“Como administrador gostaria de gerenciar professores.”*
> - Critérios de aceitação: 
> 1. O administrador deve ser capaz de ter acesso ao painel de administração.
> 2. O administrador de ser capaz de escolher a seção de gerenciamento de professores. 
> 3. O administrador deve ser capaz de cadastrar professor.
> 4. O administrador deve ser capaz de editar informações do professor.
> 5. O administrador deve ser capaz de remover professor. 

**CADASTRAR SALA:**

> *“Como administrador, gostaria de cadastrar salas.”*
> - Critérios de aceitação:
> 1. O administrador deve ser capaz de acessar o painel de administração.
> 2. O administrador deve ser capaz de escolher a seção de cadastramento de salas.
> 3. O administrador deve ser capaz de informar o setor da sala.
> 4. O administrador deve ser capaz de  informar o bloco da sala.
> 5. O administrador deve ser capaz de informar o número de identificação da sala.
> 6. O administrador deve ser capaz de informar o status de uso da sala. 


**GERENCIAR SALAS:**

> *“Como administrador, gostaria de gerenciar salas.”*
> - Critérios de aceitação: 
> 1. O administrador deve ser capaz de acessar o painel de administração.
> 2. O administrador deve ser capaz de escolher a seção de salas.
> 3. O administrador deve ser capaz de visualizar lista de salas cadastradas.
> 4. O administrador deve ser capaz de cadastrar salas.
> 5. O administrador deve ser capaz de visualizar as solicitações de agendamento.
> 6. O administrador deve ser capaz de visualizar problemas informados sobre as salas.
> 7. O administrador deve ser capaz de excluir uma sala cadastrada.

**VISUALIZAR PROBLEMAS RELATADOS:**

>*“Como administrador, gostaria visualizar problemas relatados.”*
> - Critérios de aceitação: 
> 1. O administrador deve ser capaz de acessar o painel de administração
> 2. O administrador deve ser capaz de escolher a seção de salas e visualiza a lista das salas
> 3. O administrador deve ser capaz de acessar a seção de problemas de sala
> 4. O administrador deve ser capaz de avaliar problema da sala
> 5. O administrador deve ser capaz de  acrescentar o problema no status da sala 
> 6. O administrador deve ser capaz de marcar um problema como resolvido
> 7. O administrador deve ser capaz de excluir problemas resolvidos da sala

**Visualizar solicitações de agendamento:**

> *“Como administrador, gostaria de visualizar solicitações de agendamento”*
 > - Critérios de aceitação: 
 > 1. O administrador deve ter acesso ao painel de administração
> 2. O administrador deve conseguir escolher a seção de solicitações
> 3. O administrador deve visualizar a lista de solicitações 
> 4. O administrador deve confirmar/indeferir solicitação

