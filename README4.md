# Prática Full Cycle: DevOps - Atividade Nº4

## Visão Geral

Este repositório contém a resolução da atividade prática focada em **Integração Contínua (CI)** aplicada ao desenvolvimento de software. O objetivo central foi a configuração de um pipeline automatizado utilizando **GitHub Actions** (adaptado do roteiro original de GitLab-CI) para garantir a integridade do código através de testes unitários e métricas de cobertura em cada atualização do repositório.

## Objetivos da Prática

- Configurar um ambiente de automação de CI utilizando ferramentas modernas.
- Automatizar a execução de testes unitários integrados ao fluxo de trabalho (Pipeline).
- Analisar métricas de qualidade de código, garantindo a detecção precoce de falhas.
- Alcançar e validar uma cobertura de testes de **100%** para assegurar a confiabilidade da entrega.

## Tecnologias e Ferramentas

| Ferramenta | Descrição |
|-----------|-----------|
| Python | Versão 3.11 ou superior utilizada para o desenvolvimento da API. |
| Flask | Framework web utilizado para construir os endpoints da aplicação. |
| GitHub Actions | Motor de CI/CD utilizado para orquestrar o pipeline de automação. |
| unittest | Framework nativo do Python para a criação dos testes unitários. |
| coverage.py | Ferramenta para cálculo e exibição do relatório de cobertura de código. |

## O Pipeline de CI (GitHub Actions)

O processo de integração contínua foi estruturado em três ações progressivas fundamentais:

### Ação 1: Configuração do Ambiente

- **Foco:** Criação da estrutura do pipeline e validação da execução básica de jobs.
- **Resultado:** Garantia de que o GitHub reconhece o arquivo de workflow e executa comandos simples de terminal (echo).

### Ação 2: Automação de Testes Unitários

- **Foco:** Instalação do ambiente Python e execução real do arquivo `tests/appTest.py`.
- **Comando base:** `python -m unittest -v tests/appTest.py`.
- **Resultado:** Validação automatizada das funcionalidades do sistema a cada commit.

### Ação 3: Métricas de Qualidade

- **Foco:** Implementação da análise de cobertura para identificar partes do código não testadas.
- **Resultado Final:** Geração de relatórios que confirmam **100% de cobertura** nos arquivos `app/app.py` e `tests/appTest.py`.

## Como Executar os Testes no GitHub Actions

Para reproduzir os resultados desta prática em seu próprio ambiente GitHub:

1. **Habilite as Actions:** Certifique-se de que o arquivo `.github/workflows/main.yml` está presente.
2. **Envie seu código:**
   ```bash
   git add -A
   git commit -m "Executando testes e cobertura"
   git push
   ```
3. **Monitore o Build:** Acesse o menu "Actions" no seu repositório para observar a execução dos scripts e o relatório final de cobertura.

### Saída Esperada no Log

```
Name              Stmts   Miss  Cover
-------------------------------------
app/app.py           11      0   100%
tests/appTest.py     17      0   100%
-------------------------------------
TOTAL                28      0   100%
```

## Estrutura do Projeto

- `app/app.py`: Código fonte da aplicação Flask.
- `tests/appTest.py`: Conjunto de testes unitários que validam a lógica da aplicação.
- `.github/workflows/ci.yml`: Definição do pipeline de integração contínua (GitHub Actions).


## Instituição

**UNIVERSIDADE SENAI CIMATEC**  
**Componente Curricular:** Práticas Integradas: Full Cycle  
