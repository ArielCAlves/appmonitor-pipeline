# Assessment - appmonitor-pipeline
Este repositório simula o monitoramento e automacao com GitHub Actions

## Tipos e Contextos de Variáveis no GitHub Actions

### env
Variáveis definidas no nível de escopo do job ou step. Visíveis com `$NOME_DA_VARIAVEL`.  

### vars
Variáveis definidas em Settings > Variables.  
Acessadas com `vars.NOME`.  

### secrets
Usadas para armazenar informações sensíveis como tokens e senhas.  
Definidas em *Settings > Secrets*.  
Acessadas com `secrets.NOME`.  

### Principais Diferencas
- `env`: visível diretamente no shell como variável de ambiente.
- `vars`: são públicas, gerenciadas via interface (visíveis no log).
- `secrets`: criptografadas e ocultas nos logs.

Obs: Cada uma delas foi criada dentro deste repositório e funcionaram apenas para este projeto do jeito que foram configuradas.

## Badges
![CI](https://github.com/ArielCAlves/appmonitor-pipeline/actions/workflows/ci.yml/badge.svg)

## Logs e Summaries

Os logs detalhados ajudam a identificar as falhas nos steps de cada job melhorando a manutenabilidade do pipeline.  
O resumo foi automatizado com (`$GITHUB_STEP_SUMMARY`). Ele exibe o ambiente, branch e artefatos gerados para facilitar a depuração.
Mensagens com `::warning::` e `::error::` ajudam a identificar os problemas.


