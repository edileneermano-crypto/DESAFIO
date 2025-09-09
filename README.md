# DESAFIO
DESAFIO GERADO ATRAVÉS DA ATIVIDADE CODE GIRLS
---

````markdown
# Arquitetura AWS com S3, EC2 e Lambda

Este projeto descreve uma arquitetura em nuvem utilizando **Amazon S3**, **Amazon EC2** e **AWS Lambda** para demonstrar boas práticas de armazenamento, processamento e execução de aplicações serverless.

---

## 📐 Desenho Arquitetônico

A arquitetura proposta funciona da seguinte forma:

1. **Amazon S3 (Simple Storage Service)**  
   - Responsável por armazenar arquivos (ex.: imagens, relatórios, dados brutos).
   - Serve como ponto de entrada, onde o usuário ou aplicação faz o upload dos arquivos.
   - Pode ser configurado com eventos para disparar funções Lambda.

2. **AWS Lambda**  
   - Função serverless acionada automaticamente quando novos arquivos chegam no bucket do S3.  
   - Realiza o processamento (ex.: redimensionamento de imagem, validação de dados, envio de notificações).  
   - Não precisa de servidor dedicado, escala automaticamente e cobra apenas pelo uso.

3. **Amazon EC2 (Elastic Compute Cloud)**  
   - Responsável por rodar a aplicação principal, como uma API, um sistema web ou um banco de dados.  
   - Pode se comunicar com o S3 para ler e gravar arquivos.  
   - Pode receber dados já processados pelo Lambda para armazenamento ou análise.

---

## 🔄 Fluxo de Funcionamento

1. O usuário faz upload de um arquivo para o **Amazon S3**.  
2. O evento de upload aciona uma **função Lambda**.  
3. A **Lambda** processa os dados (ex.: comprime, transforma, valida).  
4. Os resultados podem ser:  
   - Guardados novamente no **S3**;  
   - Enviados para a aplicação rodando no **EC2**.  
5. O **EC2** armazena, exibe ou manipula os dados de acordo com a necessidade do sistema.

---

## ✅ Benefícios da Arquitetura

- **Escalabilidade:** Lambda ajusta automaticamente a demanda de processamento.  
- **Custo-benefício:** paga-se apenas pelo uso do Lambda e pelo armazenamento no S3.  
- **Flexibilidade:** EC2 permite rodar aplicações personalizadas de qualquer complexidade.  
- **Automação:** eventos do S3 eliminam tarefas manuais, acelerando o fluxo.  

---

## 🚀 Possíveis Casos de Uso

- Processamento de imagens ou vídeos enviados pelos usuários.  
- ETL (extração, transformação e carga) de dados para análise.  
- Geração de relatórios automáticos a partir de arquivos.  
- Armazenamento e exibição de documentos em sistemas web.  

---

## 📌 Diagrama (exemplo visual)

```plaintext
[ Usuário ] 
     │
     ▼
[ Amazon S3 ] ---> [ AWS Lambda ] ---> [ Amazon EC2 ]
       │                 │                  │
       │                 ▼                  ▼
       └────────> [ Processamento ] --> [ Aplicação / Banco de Dados ]
````

---

## 📄 Licença

Este projeto é apenas um exemplo educacional e pode ser adaptado para diferentes cenários de arquitetura em nuvem.

```

---

Você quer que eu **faça também um diagrama visual (em PNG ou SVG)** dessa arquitetura para complementar o README, ou prefere manter só o texto em Markdown?
```
