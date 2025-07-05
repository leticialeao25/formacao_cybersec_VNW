🧪 Desafio Prático: Disponibilidade com Simulação de Queda (DVWA)

🎯 Objetivo
Demonstrar o impacto da **indisponibilidade de serviços**, simulando a queda do sistema com o Docker.

✅ Etapas
1. **Verificar se o container DVWA está em execução:**

No terminal Git ou VScode digite:
docker ps
Deve aparecer algo assim:
CONTAINER ID   IMAGE                    ...   PORTS                  NAMES
1c8a51e0d474   vulnerables/web-dvwa    ...   0.0.0.0:8080->80/tcp   dvwa_lab
Simular queda do sistema parando o container DVWA:

docker stop dvwa_lab
Isso simula uma falha ou ataque que tira o sistema do ar.

Acessar novamente no navegador:
http://localhost:8080
Resultado esperado:
Não é possível acessar esse site
A conexão com localhost foi recusada.

✅ Isso confirma que a aplicação DVWA está indisponível.

🔍 O que esse teste mostra?
A página fica fora do ar.

O sistema não responde.
Simula situações reais como ataques de negação de serviço (DoS), falhas de infraestrutura, panes ou desligamentos.

⚠️ Impacto no mundo real
Usuários não conseguem acessar o sistema.
Transações e serviços ficam interrompidos.

Gera prejuízos operacionais, financeiros e de reputação.

🧠 Conclusão
Esse desafio mostra como é fácil simular a violação do pilar de Disponibilidade da segurança da informação (CIA).

Sem disponibilidade, o sistema se torna inútil, mesmo que os dados estejam protegidos.

🔁 Recuperando o sistema
Para colocar o sistema no ar novamente, digite:
docker start dvwa_lab
Depois, acesse de novo:
http://localhost:8080


💡 Dica extra
Você também pode usar o comando abaixo para reiniciar todos os containers do projeto:
docker-compose up -d
