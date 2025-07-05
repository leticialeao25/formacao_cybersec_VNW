 Desafio Prático: Integridade com Manipulação de Dados (DVWA)

 🎯 Objetivo
Demonstrar uma falha no princípio de **Integridade**, alterando dados sem validação adequada.




✅ Etapas

1. Acesse o DVWA no navegador:
http://localhost:8080


2. Faça login com:
Usuário: admin
Senha: password





3. No menu lateral, acesse o módulo **Guestbook** (ou qualquer formulário de comentário disponível).



4. Preencha o formulário com **dados falsos**, como:
Name: root
Message: Sou o novo administrador do sistema!



5. Clique em **Sign Guestbook** para registrar.



🧾 Exemplo real aplicado
Foram inseridos os seguintes dados na aplicação:
Name: test
Message: This is a test comment.

Name: leticia
Message:

Name: root
Message: Sou um novo administrador do sistema


Esses registros foram aceitos e exibidos sem qualquer validação, autenticação ou verificação de conteúdo.


 🔍 O que observar
- A mensagem aparece na lista de comentários.
- Não houve autenticação nem validação.
- Qualquer usuário consegue manipular dados da aplicação.


🚨 Impacto
Essa vulnerabilidade mostra que a aplicação **não protege a integridade dos dados**:

- Dados falsos ou maliciosos podem ser inseridos por qualquer pessoa.
- Pode resultar em **manipulação**, **enganos**, ou **engenharia social**.


 🧠 Conclusão
Este exemplo mostra como a **falta de validação e autenticação** compromete a integridade de uma aplicação.  
Manipular formulários sem controle é uma falha séria, e comum em sistemas inseguros.
