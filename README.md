# Briefing Sistema de Agendamento de Consultas

    Uma clínica necessita controlar a agenda dos seus profissionais. Todo o sistema de agendamento é feito por telefone somente pelos atendentes da clínica. Nessa primeira versão será implementado um MVP (Produto Mínimo Viável), e dessa forma, atender somente às necessidades do MVP. Existem diversas outras funcionalidades que serão implementadas nas versões futuras, assim que o MVP for validado pelo cliente.
    Os seguintes itens foram levantamos na primeira reunião com o cliente: 


## Informações Básicas:
    - O horário de funcionamento da clínica é das 8:00 às 12:00 e das 14:00 às 18:00. (Isso poderá mudar no futuro).
    - Cada profissional indica em quais dias da semana e horários ele vai trabalhar em intervalos de 30 minutos, das 08:00 às 12:00 e das 14:00 às 18:00 horas de segunda à sexta) (Isso poderá mudar no futuro).
    - Cada atendimento deve durar o tempo de 30 minutos e os horários de agendamento são intercalados a cada 30 minutos começando das 08:00 às 11:30 e das 14:00 às 17:30 horas de segunda à sexta) (Isso poderá mudar no futuro).
    - Um profissional pode estar ativo ou desativo.
    - Um profissional pode atender de várias áreas e o cliente deve indicar a área e o profissional desejado ao fazer o agendamento.
    - Um agendamento tem um tipo: convênios ou particular.

## Fazendo um agendamento:
    - O agendamento deverá ter: cliente, profissional, área, tipo, comentários, data e horário de início (validar todas as informações).
    - Mostrar a disponibilidade de datas e horários dentro de um mês de um profissional.
    - Ao agendar uma consulta, confirmar o telefone do cliente selecionado.

## Restrições ao fazer um agendamento ou cancelamento:
    - Não deve permitir agendar fora do horário e dias da semana de cada profissional ou fora do horário de funcionamento da clínica.
    - Não deve permitir agendar dois ou mais clientes no mesmo dia e horário de um profissional.
    - Não permitir agendar o mesmo cliente no mesmo dia e horário.
    - Agendar somente com profissionais ativos.
    - Não agendar no passado.
    - Ao agendar uma consulta, selecionar primeiro a área e depois o profissional.
    - O atendente pode cancelar um atendimento quando solicitado pelo cliente, mas não apagar o histórico do agendamento, apenas mudar o status do agendamento para CANCELADO. Não existe a possibilidade de reagendamento de uma consulta, ela só pode ser cancelada. Ao cancelar uma consulta, o horário do profissional deverá ser liberado para novos agendamentos.

## No dia do agendamento:
    - O sistema deve controlar a frequência dos clientes (PRESENTE ou AUSENTE) no dia da consulta.
    - Listar as consultas do dia da clínica, selecionando a área e o profissional. Essa opção deve permitir definir o cliente como ausente ou presente.
    - O status PRESENTE só deve ser alterado no dia do Agendamento.
    - O status AUSENTE só pode ser alterado depois da data e hora do Agendamento.


## Tipos de usuários:
    -  Usuário Operador:
        - Permite fazer a manutenção de clientes.
        - Permite agendar e cancelar consultas.

    - Administrador: 
        - Tem as mesmas opções do operador.
        - Permite fazer a manutenção de novos usuários.
        - Permite fazer a manutenção do tipo de agendamento.
        - Permite fazer a manutenção de áreas.
        - Permite fazer a manutenção de profissionais.


## Manutenções (CRUDs):
    - Manutenção do tipo de atendimento (particular, convênios 1, convênio 2). 
        Campo: tipo.
    - Manutenção de clientes. 
        Campos: nome, telefone e data de nascimento.
        Listar o histórico de consultas de um cliente.
    - Manutenção de profissionais. 
        Campos: nome, telefone, ativo e áreas.
        Ao desativar um profissional, manter os agendamentos em aberto.
    - Manutenção de áreas. 
        Campo: nome.
    - Manutenção da disponibilidade do profissional: 
        Campos (dias e horários de trabalho).
        Ao mudar a disponibilidade de um profissional, manter os agendamentos em aberto.
    - Manutenção de usuários. 
        Campo: nome, email, password, phone, roles.

    Observação: Não remover dados com relacionamentos. 

## Responsividade:
    - Ter o layout correto para larguras de tela com 350px ou mais.
    - Não considerar larguras menores que 350px.


## Diagramas
### Use Cases
![Use Cases](/out/docs/use_cases/use_cases.png)

### Model
![Model](/out/docs/model/model.png)

### EndPoints
![EndPoints](/out/docs/end_points/end_points.png)



