# Mineração de Repositórios - Foco em UI

Este projeto aplica técnicas de mineração de repositórios de software para investigar práticas de Experiência do Usuário (UI) em projetos de software. O objetivo é identificar e analisar padrões de UI, contribuindo para que equipes de desenvolvimento criem produtos mais eficientes, acessíveis e com usabilidade aprimorada.

Este trabalho faz parte da disciplina **Tópicos em Engenharia de Sistemas de Software 1** do programa de Pós-Graduação em Ciência da Computação da Universidade Estadual de Maringá (UEM).


## Objetivo

A mineração de repositórios possibilita a análise de grandes volumes de dados de projetos de software, permitindo a extração de informações valiosas. Neste projeto, buscamos compreender como as práticas de UI são integradas aos projetos de software e identificar insights que ajudem no desenvolvimento de produtos mais eficazes.

## Funcionalidades

- **Coleta de Dados**: Extração de dados de repositórios hospedados no GitHub, focando em projetos relacionados à UI/UX.
- **Análise de UI**: Identificação de práticas relacionadas à UI em arquivos de configurações, commits e entre outros.
- **Insights e Relatórios**: Geração de visualizações e relatórios sobre o impacto de práticas de UI, auxiliando na tomada de decisões.
- **Classificação e Organização**: Agrupamento dos repositórios conforme categorias de UI, facilitando análises específicas e direcionadas.

## Estrutura do Projeto

O projeto está organizado em três diretórios principais:

- **`Code`**: Contém os scripts para mineração de repositórios.
- **`Database`**: Armazena os arquivos CSV gerados durante a análise.
- **`Image`**: Contém imagens geradas pelos scripts para visualização dos resultados.

## Ordem de Execução

Para realizar a mineração e análise de repositórios com foco em UI, siga a ordem de execução dos scripts abaixo:

### Criar o Dataset

1. **`01-pesquisa.ipynb`**  
   Realiza a busca inicial de repositórios no GitHub usando palavras-chave relacionadas à UI/UX.

2. **`02-detectar-idioma.ipynb`**  
   Detecta o idioma de cada repositório e filtra apenas os que estão em inglês.

3. **`03-filtros-aplicados.ipynb`**  
   Aplica filtros adicionais nos repositórios coletados para refinar os dados com base em critérios definidos.

4. **`04-filtros-por-arquivo-config.ipynb`**  
   Verifica a presença de arquivos específicos, como `package.json` e `composer.json`, para categorizar os repositórios.

5. **`05-categorizar-repositórios.ipynb`**  
   Classifica os repositórios nas categorias **Ferramenta UI**, **Aplicação UI**, **Componente UI**, ou **Não Classificado**. Gera dois arquivos CSV: um para repositórios classificados e outro para os não classificados.

6. **`06-data.ipynb`**  
   Organiza o conjunto de dados para análise, incluindo formatação de datas.

7. **`07-primeiras-analise.ipynb`**  
   Realiza uma análise preliminar, como a distribuição de repositórios por ano.

### Responder a Primeira Pergunta

8. **`08-busca-pelo-arquivo-config.ipynb`**  
   Realiza a busca e armazena o conteúdo dos arquivos de configuração presentes nos repositórios filtrados.

9. **`09-separar-dataset.ipynb`**  
   Segrega o dataset com base nos arquivos de configuração, criando CSVs específicos para cada tipo, como `package.json` e `composer.json`.

10. **`10-ranking.ipynb`**  
    Identifica e armazena os principais componentes de UI usados nos arquivos de configuração dos repositórios.

11. **`11-repositorios-frequencia.ipynb`**  
    A partir dos dados anteriores, realiza uma análise da frequência de uso de componentes de UI e configuração em diferentes repositórios.

### Responder a Segunda Pergunta

*(Incluir descrição e scripts relevantes para a segunda pergunta)*

### Responder a Terceira Pergunta

12. **`12-historico-repositorios.ipynb`**  
    Com o dataset dos repositórios, é possível realizar uma análise histórica dos arquivos de configurações e armazenar os dados para cada repositório.

13. **`13-analise-dependencies.ipynb`**  
    Coleta dados ao longo do tempo e analisa as mudanças no `package.json`, gerando uma análise que compara o número de dependências ao longo do tempo.

### Responder a Quarta Pergunta