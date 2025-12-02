🔒 Revogação de Permissões MySQL – REVOKE para o Usuário ALUNO

Esta parte do projeto mostra como remover permissões do usuário 'ALUNO'@'localhost' utilizando o comando REVOKE no MySQL.
É o complemento perfeito da Parte 1 (GRANT), formando um ciclo completo de estudo de controle de acesso. 🧠💡

🧹 O que o script faz

O código demonstra como retirar cada tipo de permissão concedida anteriormente:

🔄 Atualização

Revoga o acesso de UPDATE na tabela e também em todos os bancos.

❌ Exclusão

Remove permissões de DELETE em FUNCIONARIOS e no escopo global.

➕ Inserção

Revoga INSERT do usuário ALUNO.

🔍 Seleção

Remove SELECT, incluindo versões combinadas e até SELECT restrito por colunas.

⚙️ Procedures

Revoga a permissão de EXECUTE sobre a procedure proc_quadrado.

🛑 Revogação total

Inclui remoção completa de todos os privilégios usando:
REVOKE ALL PRIVILEGES ON ...

🔃 Atualização de privilégios

O comando FLUSH PRIVILEGES; é usado para recarregar as permissões imediatamente.

🧭 Para que serve isso?

Este material ajuda a compreender a parte mais importante da segurança de um banco:
remover acessos que não deveriam existir.
Com isso, é possível:

Proteger dados sensíveis

Limitar ações de usuários

Garantir que apenas permissões necessárias permaneçam

Entender o fluxo completo de GRANT → uso → REVOKE

Perfeito para estudo e prática profissional de administração de bancos. 🔧📚

🧪 Como testar

Crie o usuário ALUNO (se ainda não existir).

Execute os GRANTs da Parte 1.

Rode este script para ver as permissões sendo removidas.

Use:

SELECT * FROM mysql.user WHERE User='ALUNO';
