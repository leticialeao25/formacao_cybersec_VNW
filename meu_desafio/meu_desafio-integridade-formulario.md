 🧪 Desafio Prático: Integridade com Manipulação de Dados (DVWA)

## 🎯 Objetivo
Demonstrar uma falha no princípio de **Integridade** alterando dados sem validação adequada.

1. Acesse o DVWA no navegador:
http://localhost:8080

2. Faça login com:
Usuário: admin
Senha: password


4. No menu lateral, acesse o módulo **Guestbook** (pode estar dentro de **XSS (Stored)** ou similar).



5. Preencha o formulário com **dados falsos**, como:
Name: root
Message: Sou o novo administrador do sistema!


6. Clique em **Sign Guestbook** para registrar.


## 🔍 O que observar
- A mensagem aparece na lista de comentários.
- Não houve autenticação ou validação.
- Qualquer pessoa pode alterar dados visíveis da aplicação.


## 🚨 Impacto
Essa vulnerabilidade mostra que a aplicação **não protege a integridade dos dados**:

- Dados falsos ou maliciosos podem ser inseridos por qualquer usuário.
- Pode resultar em **manipulação de informações**, **fraudes**, ou **ataques sociais**.

## 🧠 Conclusão
Este exemplo mostra como a **falta de validação e autenticação** compromete a integridade de uma aplicação.  
A manipulação de formulários sem controle é um vetor real de ataque, inclusive em aplicações do mundo real.
