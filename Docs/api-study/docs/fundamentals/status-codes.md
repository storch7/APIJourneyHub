# Status Codes

[Fonte](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status) desta sessão.

---

## HTTP response status codes

HTTP response status codes indicate whether a specific HTTP request has been successfully completed. Responses are grouped in five classes:

- Informational responses (100 – 199)
- Successful responses (200 – 299)
- Redirection messages (300 – 399)
- Client error responses (400 – 499)
- Server error responses (500 – 599)

---

## Erros mais comuns

### 1xx – Informativos

| Código | Nome | Descrição | Causa mais comum | Ação recomendada |
|--------|------|------------|------------------|------------------|
| 100 | Continue | O servidor recebeu parte da requisição e o cliente pode continuar | Comunicação HTTP em múltiplas etapas (ex.: upload grande) | Nenhuma ação; parte do fluxo normal |
| 101 | Switching Protocols | O servidor aceita mudar o protocolo de comunicação | Upgrade de protocolo (ex.: HTTP → WebSocket) | Nenhuma ação; apenas informativo |

---

### 2xx – Sucesso

| Código | Nome | Descrição | Causa mais comum | Ação recomendada |
|--------|------|------------|------------------|------------------|
| 200 | OK | A requisição foi bem-sucedida | Endpoint correto e dados válidos | Validar conteúdo retornado |
| 201 | Created | Recurso criado com sucesso | Uso de POST para criação | Armazenar ID retornado |
| 202 | Accepted | Requisição aceita para processamento assíncrono | Processamento em background | Verificar status posteriormente |
| 204 | No Content | Requisição bem-sucedida, sem corpo de resposta | DELETE bem-sucedido ou atualização sem retorno | Nenhuma ação adicional |

---

### 3xx – Redirecionamento

| Código | Nome | Descrição | Causa mais comum | Ação recomendada |
|--------|------|------------|------------------|------------------|
| 301 | Moved Permanently | O recurso foi movido para uma nova URL permanente | Mudança de endpoint | Atualizar URL usada pelo cliente |
| 302 | Found | Redirecionamento temporário | Recurso temporariamente em outra URL | Seguir redirecionamento automático |
| 304 | Not Modified | Recurso não modificado desde última requisição | Cache válido | Usar conteúdo local armazenado |

---

### 4xx – Erros do Cliente

| Código | Nome | Descrição | Causa mais comum | Ação recomendada |
|--------|------|------------|------------------|------------------|
| 400 | Bad Request | Requisição inválida ou malformada | JSON incorreto, parâmetro ausente | Validar corpo e formato antes do envio |
| 401 | Unauthorized | Requisição sem autenticação válida | Token ausente, inválido ou expirado | Adicionar header Authorization corretamente |
| 403 | Forbidden | Usuário autenticado, mas sem permissão | Escopos insuficientes ou acesso negado | Revisar permissões e escopos de API |
| 404 | Not Found | Recurso ou endpoint inexistente | ID incorreto ou endpoint errado | Confirmar URL e parâmetros |
| 405 | Method Not Allowed | Método HTTP não permitido | Uso incorreto de POST/GET/PUT | Consultar documentação da API |
| 409 | Conflict | Conflito de estado no servidor | Tentativa de criar recurso duplicado | Verificar existência antes de criar |
| 415 | Unsupported Media Type | Tipo de conteúdo não aceito | Content-Type incorreto | Ajustar header e formato de dados |
| 422 | Unprocessable Entity | Requisição bem-formada mas inválida semanticamente | Campos obrigatórios ausentes, validação falha | Corrigir payload conforme regras da API |
| 429 | Too Many Requests | Limite de requisições excedido | Excesso de chamadas em curto período | Implementar retry com backoff e controle de taxa |

---

### 5xx – Erros do Servidor

| Código | Nome | Descrição | Causa mais comum | Ação recomendada |
|--------|------|------------|------------------|------------------|
| 500 | Internal Server Error | Erro genérico no servidor | Exceção não tratada ou falha interna | Retry após alguns segundos; registrar erro |
| 501 | Not Implemented | Funcionalidade não implementada | Método ou recurso ainda não disponível | Verificar suporte na documentação |
| 502 | Bad Gateway | Gateway recebeu resposta inválida | Falha entre proxies ou serviços intermediários | Retry com intervalo crescente |
| 503 | Service Unavailable | Servidor temporariamente indisponível | Manutenção ou sobrecarga | Retry após tempo indicado no header Retry-After |
| 504 | Gateway Timeout | Timeout em comunicação entre servidores | API demorou demais para responder | Ajustar tempo de espera ou otimizar requisição |
| 507 | Insufficient Storage | Falta de espaço no servidor | Limite de armazenamento atingido | Notificar suporte e tentar novamente mais tarde |

---

## Links interessantes

HTTP Erros as cats: [Link](https://http.cat/).

--- 

## Histórico de versão

| Versão | Alteração | Data |
|---|---|---|
|1.0| Construção da página e conteúdo | 31/10/25 |