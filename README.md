# Teste: Construa uma API simples para reserva de hotel

## Descrição

Crie uma API para gerenciar reservas de hotéis usando a linguagem de programação de sua escolha (exemplo: Node.js com TypeScript, Python, Ruby, etc.). A API deve permitir que os usuários reservem quartos de hotel e, em caso de sucesso, visualizem um PDF com as informações da reserva. O fornecimento do código é opcional, mas preferível. Caso opte por não fornecer o código, explique como você abordaria cada etapa do projeto. Considere que usamos um banco de dados não relacional, e nossa arquitetura é baseada em funções Lambda e mensageria.

## Requisitos

1. Implemente um endpoint para criar uma reserva de hotel. O endpoint deve aceitar informações como nome do usuário, datas de check-in e check-out, e número de quartos.
   - Dica: Considere usar um banco de dados não relacional (por exemplo, MongoDB, DynamoDB, etc.) para armazenar as informações das reservas.

2. Implemente um mecanismo para tratar situações em que dois usuários tentem reservar o mesmo quarto ao mesmo tempo.
   - Dica: Pesquise sobre "lock otimista" e "lock pessimista" para lidar com concorrência.

3. Implemente um endpoint para enviar um comprovante de pagamento da reserva. O comprovante de pagamento pode ser uma imagem ou arquivo PDF.
   - Dica (Node.js): Use o Multer para lidar com o upload de arquivos.

4. Após a confirmação do pagamento, gere um PDF com as informações da reserva.
   - Dica (Node.js): Utilize a biblioteca `pdf-lib` ou `puppeteer` para gerar o PDF.

5. Implemente um endpoint para permitir que o usuário baixe o PDF da reserva confirmada.
   - Dica: Armazene o PDF gerado no sistema de arquivos ou no banco de dados e sirva-o através do endpoint.

6. Adicione um endpoint para que o usuário adicione saldo à sua conta.
   - Dica: Armazene o saldo do usuário no banco de dados e atualize-o conforme necessário.

7. Implemente um mecanismo que, quando o check-in é feito, o saldo do usuário seja gasto de acordo com o valor da reserva.
   - Dica: Crie um endpoint para registrar o check-in do usuário e, em seguida, atualize o saldo do usuário no banco de dados.

8. Adapte a solução para utilizar a arquitetura baseada em funções Lambda e mensageria.
   - Dica: Use AWS Lambda para implementar as funções e Amazon SQS ou SNS para mensageria.

9. Escreva testes unitários e de integração para a API.

10. Use boas práticas de desenvolvimento, como modularização, tratamento de erros e validação de dados.

## Recursos adicionais (opcionais)

1. Implemente autenticação e autorização para proteger os endpoints.
   - Dica (Node.js): Utilize o `jsonwebtoken` (JWT) para autenticação e autorização.

2. Implemente uma solução de cache para melhorar o desempenho e a escalabilidade da API.
   - Dica (Node.js): Utilize o Redis como cache.

3. Implemente um mecanismo de log para registrar eventos e erros na API

Ao concluir o teste, forneça instruções claras sobre como instalar, configurar e executar a API, bem como os testes associados. Se você optar por não fornecer código, explique como abordaria cada etapa do projeto, levando em consideração o uso de um banco de dados não relacional e uma arquitetura baseada em funções Lambda e mensageria.
