🔐 Análise de Tráfego HTTP no Wireshark — Aula 7

 🎯 Objetivo
Capturar, filtrar e analisar requisições HTTP usando Wireshark, verificando o conceito de Confidencialidade na Segurança da Informação.


📡 Requisição HTTP Capturada
- **Método:** `GET / HTTP/1.1`
- **Origem (IP):** `10.0.10.162`
- **Destino (IP):** `23.60.101.25`
- **Protocolo:** HTTP
- **Porta:** 80 (destino)
- **Status posterior:** `304 Not Modified`

 🧠 Cabeçalhos HTTP observados:
Host: ocsp.c.lencr.org
User-Agent: Microsoft-CryptoAPI/10.0
Connection: Keep-Alive
📌 Observações Técnicas
O tráfego foi identificado e filtrado com:


A requisição GET solicita a raiz do domínio (/) via protocolo HTTP puro (sem criptografia).
A resposta 304 Not Modified indica que o conteúdo requisitado não sofreu alteração desde a última requisição.

📁 Evidência Visual


🧼 Finalização
Após a análise, o ambiente foi limpo com:
cd formacao-cybersec/modulo1-fundamentos/aula_7
docker compose down



✅ Resultado esperado atingido: tráfego HTTP visível, campos analisados e vulnerabilidade potencial identificada (tráfego sem criptografia).
