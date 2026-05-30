# 🌱 Agrotrack robot v2 🌱

Projeto de automação desenvolvido usando o microsoft power automate de forma independente com foco em automação de processos repetitivos.

---

## 🔄 Fluxo do robô

- 📥 Inserção de número de container que deseja ser rastreado a partir de um excel previamente preenchido *(seria tipo: quero que você preencha tudo sobre este container em específico)*
- 🌐 Rastreamento no site para saber onde se encontra o container
- 📦 Instalação do arquivo json gerado a partir do front-end (javascript)
- 📖 Ler arquivo json
- 📊 Inserção dos dados obtidos pelo site numa tabela excel, contendo todas as informações

> 🔁 O loop se repete **ENQUANTO TIVER** container para preencher — é ilimitado e automático.

---

## 📊 O que é obtido

Dados brutos prontos para futuras análises utilizando PowerBI ou outras ferramentas.

---

## ⚡ Ganhos

O TEMPO que é gasto trabalhando num processo repetitivo como este pode ser dirigido a alguma outra tarefa mais complexa ou que tenha mais prioridade.

### Resumo do impacto para inserção de dados sobre 50 containeres:

| | Tempo |
|---|---|
| 👤 Humano | ~3 horas |
| 🤖 Robô | ~7 minutos |
| ⚡ Ganho | **96% de redução no tempo** |

E o robô ainda:

- ✅ Não erra digitação
- ✅ Não se cansa
- ✅ Roda de madrugada se precisar
- ✅ Já entrega os dados prontos para o Power BI

---

## 📋 Regras do projeto

**1.** O front-end web foi criado através de um prompt com o Claude, porém foi totalmente ideia minha.

**2.** É um MVP (minimum viable product), o que significa que não conta com sistemas de segurança robustos nem dados sobre containeres reais. É um projeto teste.

**3.** O site não possui comunicação com back-end algum *(o que seria, no caso, o banco de dados onde os status dos contêineres estão guardados).*

> **Exemplo:** conteinerA está em X cidade, X país e está se dirigindo a Y localidade através do navio Z. Esses são dados incluídos já no front-end o que, na vida real, nunca aconteceria. Os dados estariam protegidos no database, permitindo acesso somente através da chave da API.

Numa situação real, esses dados seriam obtidos através de uma requisição para a API para obter os dados no banco de dados da empresa (um GET). Porém, a informação retornaria da mesma forma que é retornada neste projeto, e o robô funcionaria da mesma forma.

> **a.** Logo, todos os status são fictícios e servem para mostrar a funcionalidade do robô.

Porém, mesmo se tratando de dados fictícios, a eficácia dele é demonstrada através do que ele faz a partir dos dados e como agiliza um trabalho manual e extremamente repetitivo.

---

## 🛠️ Stack

`HTML/CSS/JS` · `Power Automate Desktop` · `Excel` · *(futuro: API REST + banco de dados real)*

## Imagens do site:

![Print1](https://raw.githubusercontent.com/davicarb/agrotrack_v2/refs/heads/main/web_picture.png)
![Print2](https://raw.githubusercontent.com/davicarb/agrotrack_v2/refs/heads/main/web_picture2.png)
