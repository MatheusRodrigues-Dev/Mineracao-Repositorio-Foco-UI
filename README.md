# Mineração de Repositórios - Foco em UI

Este projeto aplica técnicas de mineração de repositórios de software para investigar práticas de **Experiência do Usuário** (UI) em projetos de software. O objetivo é identificar e analisar padrões de UI, proporcionando insights para que equipes de desenvolvimento criem produtos mais eficientes, acessíveis e com melhor usabilidade.

O trabalho é parte da disciplina **Tópicos em Engenharia de Sistemas de Software 1** do programa de Pós-Graduação em Ciência da Computação da Universidade Estadual de Maringá (UEM).

## Objetivo

A mineração de repositórios permite a análise de grandes volumes de dados provenientes de projetos de software, possibilitando a extração de informações valiosas. Neste projeto, o foco é entender como as práticas de UI estão sendo aplicadas nos repositórios de software, com o intuito de identificar padrões que ajudem a aprimorar o desenvolvimento de produtos mais eficazes e com uma experiência de usuário melhorada.

## Funcionalidades

- **Coleta de Dados**: Extração de dados de repositórios hospedados no GitHub, com foco em projetos relacionados a UI/UX.
- **Análise de UI**: Identificação de práticas relacionadas à UI em arquivos de configuração, commits e outros documentos presentes nos repositórios.
- **Geração de Insights e Relatórios**: Criação de visualizações e relatórios que detalham o impacto das práticas de UI, auxiliando na tomada de decisões informadas.
- **Classificação e Organização**: Agrupamento de repositórios conforme categorias de UI, facilitando análises específicas e direcionadas.

## Estrutura do Projeto

O projeto está organizado em três diretórios principais:

- **`Code`**: Contém os scripts utilizados para a mineração de repositórios.
- **`Database`**: Armazena os arquivos CSV gerados durante as análises.
- **`Image`**: Contém imagens geradas pelos scripts para visualização dos resultados.

## Ordem de Execução

Para realizar a mineração e análise de repositórios com foco em UI, siga a ordem dos scripts abaixo:

### Criar o Dataset

1. **`01-pesquisa.ipynb`**  
   Realiza a busca inicial de repositórios no GitHub usando palavras-chave relacionadas à UI/UX.

2. **`02-detectar-idioma.ipynb`**  
   Detecta o idioma de cada repositório e filtra os que estão em inglês.

3. **`03-filtros-aplicados.ipynb`**  
   Aplica filtros adicionais nos repositórios coletados para refinar os dados de acordo com critérios definidos.

4. **`04-filtros-por-arquivo-config.ipynb`**  
   Verifica a presença de arquivos específicos, como `package.json` e `composer.json`, para categorizar os repositórios.

5. **`05-categorizar-repositórios.ipynb`**  
   Classifica os repositórios em categorias como **Ferramenta UI**, **Aplicação UI**, **Componente UI** ou **Não Classificado**. Gera dois arquivos CSV: um para repositórios classificados e outro para os não classificados.

6. **`06-data.ipynb`**  
   Organiza e formata o conjunto de dados, incluindo a manipulação de datas.

7. **`07-primeiras-analise.ipynb`**  
   Realiza uma análise preliminar, como a distribuição de repositórios por ano.

### Responder à Primeira Pergunta

8. **`08-busca-pelo-arquivo-config.ipynb`**  
   Busca e armazena o conteúdo dos arquivos de configuração presentes nos repositórios filtrados.

9. **`09-separar-dataset.ipynb`**  
   Segrega o dataset com base nos arquivos de configuração, criando arquivos CSV específicos para cada tipo, como `package.json` e `composer.json`.

10. **`10-ranking.ipynb`**  
    Identifica e armazena os principais componentes de UI utilizados nos arquivos de configuração dos repositórios.

Após a execução do item 10, os dados gerados são utilizados para responder à primeira questão. O CSV gerado, `questao1-ranking-geral.csv`, contém os componentes utilizados nos repositórios, e uma análise manual é realizada para identificar os componentes de UI mais frequentes.

11. **`11-repositorios-frequencia.ipynb`**  
    Exibe os principais componentes utilizados nos repositórios.

### Responder à Segunda Pergunta

12. **`12-tratamento-dados.ipynb`**  
    Realiza o tratamento dos dados necessários para responder à segunda questão de pesquisa, ordenando os repositórios e fazendo merge para comparar os dados. Também realiza uma análise dos dados para ajudar a responder à segunda questão.

### Responder à Terceira Pergunta

13. **`13-historico-repositorios.ipynb`**  
    Com o dataset dos repositórios, realiza uma análise histórica dos arquivos de configuração, armazenando os dados para cada repositório.

14. **`14-analise-dependencies.ipynb`**  
    Coleta dados ao longo do tempo e analisa as mudanças nos arquivos `package.json`, gerando uma análise que compara o número de dependências ao longo do tempo.

### Responder à Quarta Pergunta

**A ser detalhado conforme os próximos passos do projeto.**

---

### Considerações Finais

Este projeto visa fornecer uma análise profunda das práticas de UI em projetos de software, com o intuito de melhorar a compreensão e a integração das práticas de experiência do usuário. Ao realizar a mineração de dados de repositórios de código aberto, a expectativa é oferecer insights valiosos para a comunidade de desenvolvimento de software, auxiliando na criação de produtos mais bem projetados e com melhor usabilidade.
