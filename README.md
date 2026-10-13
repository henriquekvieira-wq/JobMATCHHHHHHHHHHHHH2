# JobMatch AI — Python + Streamlit

Aplicação acadêmica para comparar currículos com descrições de vagas e praticar entrevistas técnicas. Líder do projeto: **Felipe Araújo**.

## Funcionalidades

- Comparação de competências técnicas entre currículo e vaga.
- Normalização de caixa, espaços e acentos para reconhecer termos conhecidos.
- Sugestões de competências relacionadas ao cargo, identificadas separadamente.
- Escolha opcional de cargo de referência.
- Pontuação textual de compatibilidade, lista de competências encontradas e lacunas com prioridade.
- Carregamento de currículo PDF, DOCX ou TXT (até 5 MB) com extração de texto.
- Banco de perguntas técnicas por competência, sorteio entre rodadas e controle de 3 a 8 perguntas.
- Respostas com feedback imediato por regras heurísticas.
- Modo claro/escuro, exemplo de demonstração, botão para limpar campos e histórico temporário da sessão.
- Exportação de relatório TXT e JSON.

## Como executar no Windows

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

## Como executar no Linux/macOS

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

## Publicar no Streamlit Community Cloud

1. Envie `app.py`, `requirements.txt` e `README.md` para a raiz do repositório GitHub.
2. No Streamlit Community Cloud, selecione esse repositório, a branch e `app.py` como arquivo principal.
3. Publique ou reinicie o aplicativo. O ambiente instalará as dependências indicadas em `requirements.txt`.

## Limitações conhecidas

- O diagnóstico é baseado em palavras-chave conhecidas e regras simples de contexto. Não realiza análise semântica completa.
- PDFs escaneados sem camada de texto não são lidos por OCR; nesse caso, copie o texto para o campo.
- O percentual é uma proporção de competências textualmente encontradas, não uma probabilidade de contratação.
- O feedback das respostas é heurístico e não comprova correção técnica. O protótipo não chama um modelo generativo externo.
- O histórico existe apenas na sessão ativa e não utiliza banco de dados.

## Próximas evoluções sugeridas

Integração opcional com modelo generativo, testes automatizados, suporte a OCR para documentos escaneados, persistência segura de histórico e avaliação do algoritmo com currículos e vagas de teste anonimizados.
