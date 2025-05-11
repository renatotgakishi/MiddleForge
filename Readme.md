# Middleware para Formatação Padrão de API

Um middleware para padronização de respostas de API é extremamente útil para garantir consistência em todas as respostas JSON da sua aplicação. 
Solução robusta que inclui tratamento de erros, formatação padrão e boas práticas.


## Padrão de Resposta Gerado

**Sucesso (200 OK):**
```json
{
  "success": true,
  "data": { /* seus dados reais */ },
  "timestamp": "2023-08-20T12:00:00Z",
  "statusCode": 200
}
```

**Erro (500 Internal Server Error):**
```json
{
  "success": false,
  "error": {
    "message": "Ocorreu um erro ao processar sua requisição",
    "details": "Mensagem específica do erro",
    "exceptionType": "NullReferenceException"
  },
  "timestamp": "2023-08-20T12:00:00Z",
  "statusCode": 500
}
```

## Vantagens Desta Abordagem

1. **Consistência**: Todas as respostas seguem o mesmo padrão
2. **Manutenibilidade**: Fácil de modificar o formato globalmente
3. **Tratamento de Erros Centralizado**: Exceções não tratadas são convertidas em JSON
4. **Metadata**: Timestamp e status code incluídos automaticamente
5. **Separação de Conceitos**: Lógica de formatação separada dos controllers
