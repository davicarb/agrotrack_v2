# 🌱 agrotrack v2

Projeto de automação desenvolvido usando o microsoft power automate de forma independente com foco em automação de processos repetitivos.

---

## 🔄 Fluxo do robô

- 📥 Inserção de número de container que deseja ser rastreado a partir de um excel previamente preenchido *(seria tipo: quero que você preencha tudo sobre este container em específico)*
- 🌐 Rastreamento no site para saber onde se encontra o container
- 📦 Instalação do arquivo json gerado a partir do front-end (javascript)
- 📖 Ler arquivo json
- 📊 Inserção dos dados obtidos pelo site numa tabela excel, contendo todas as informações

> 🔁 O loop se repete **ENQUANTO TIVER** container para preencher — é ilimitado e automático.

## 🎥 demonstração
[assistir o robô em execução sem precisar instalar](https://youtu.be/eOnwEOX_JKs)

## 📋 Regras do projeto

**1.** O front-end web foi criado através de um prompt com o Claude, porém foi totalmente ideia minha.

**2.** É um MVP (minimum viable product), o que significa que não conta com sistemas de segurança robustos nem dados sobre containeres reais. É um projeto teste.

**3.** O site não possui comunicação com back-end algum *(o que seria, no caso, o banco de dados onde os status dos contêineres estão guardados).*

> **Exemplo:** conteinerA está em X cidade, X país e está se dirigindo a Y localidade através do navio Z. Esses são dados incluídos já no front-end o que, na vida real, nunca aconteceria e seria uma catástrofe para a segurança da informação. Os dados estariam protegidos no back-end, no database, permitindo acesso somente através da chave privada da API.

Numa situação real, esses dados seriam obtidos através de uma requisição para a API para obter os dados no banco de dados da empresa (um GET). Porém, a informação retornaria da mesma forma que é retornada neste projeto, e o robô funcionaria da mesma forma.

> **a.** Logo, leve em consideração que todos os status são fictícios e servem para mostrar a funcionalidade do robô. Mesmo se tratando de dados fictícios, a eficácia dele é demonstrada através do que ele faz a partir dos dados e como agiliza um trabalho manual e extremamente repetitivo.

---

## Como rodar o projeto?

**1.** crie uma pasta chamada `agrotrack_v2` na área de trabalho do seu pc

**2.** coloque dentro dela os arquivos do repositório:
- `web-rastreio-conteiner-agro.html`
- a note que `containers_entrada.xlsx` você deverá preencher com os codigos do container que você deseja que o robô preencha os dados. logo, é necessário que você crie essa planilha por conta própria e com exatamente o nome descrito acima.

> siga o modelo descrito no site: `LDCU` para líquidos, `AGRO` para soja ou milho, `RFGR` para refrigerados ou `GRAN` para granel. o número que vem após essas letras pode ser qualquer um.
>
> o código do contêiner que você deseja obter os resultados deve permanecer na coluna `A` a partir da linha `2`, para que o power automate consiga funcionar corretamente. você pode adicionar quantos contêineres quiser. é ilimitado, desde que haja espaço no seu computador!

**3.** crie uma pasta vazia chamada `Execucoes` dentro da pasta base `agrotrack_v2`

**4.** crie um novo fluxo no power automate desktop

**5.** cole o código do power automate que está neste repo do github dentro do seu fluxo

**6.** rode o fluxo

**7.** deixe o robô trabalhar por você enquanto toma um café! ☕

## 📈 Aonde ficarão as planilhas produzidas pelo power automate?
As planilhas produzidas ficarão dentro das pastas de cada execução dentro da pasta "Execucoes", contendo a data exata de quando aquela execução aconteceu.
Exemplo de nome de planilha após execução bem-sucedida: *agrotrackreport_2026-05-30_16-55-56*

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

## 🛠️ Stack

`HTML/CSS/JS` · `Power Automate Desktop` · `Excel` · *(futuro: API REST + banco de dados real)*

## Imagens do site:

![Print1](https://raw.githubusercontent.com/davicarb/agrotrack_v2/refs/heads/main/web_picture.png)
![Print2](https://raw.githubusercontent.com/davicarb/agrotrack_v2/refs/heads/main/web_picture2.png)
