# Lab: Arquitetura de Times de Agentes de IA

Laboratório prático de estudos focado em **Engenharia de Contexto** e orquestração de Agentes de Inteligência Artificial. O foco deste projeto é mapear teoricamente e estruturar as *Skills* necessárias para criar uma esteira de produção autônoma de artigos para blog.

## O Desafio
Modelos de linguagem tradicionais sofrem com degradação de memória em conversas longas e alucinação de dados. Este laboratório propõe uma arquitetura descentralizada, dividindo o processo em um time de especialistas com papéis restritos.

## Estrutura da Esteira de Agentes
O fluxo de trabalho funciona como uma linha de montagem, onde cada agente possui um `SKILL.md` com regras de execução inegociáveis:

- **Scout (Pesquisador):** Acessa APIs de busca para extrair palavras-chave e faz o *offload* de dados pesados para evitar estouro de contexto.
- **Strategist (Estrategista):** Recebe os dados limpos do Scout e monta o briefing estrutural (H1, H2, etc).
- **Worker (Redator):** Focado puramente na escrita criativa baseada no esqueleto aprovado.
- **Reviewer (QA/Revisor):** Audita o texto final contra regras de SEO e tom de voz.

## Foco em Qualidade e Prevenção de Falhas
Como o foco do projeto também engloba Qualidade de Software (QA), as instruções dos agentes foram desenhadas para prevenir os seguintes cenários negativos:
* **Prevenção de Alucinação:** O *Scout* é travado para abortar a missão caso não encontre dados reais, impedindo a invenção de estatísticas.
* **Mitigação de Loops Infinitos:** Regras rígidas de aprovação para o *Reviewer*, evitando consumo excessivo de tokens em refações sem fim.
* **Isolamento de Contexto:** Cada agente recebe apenas o *input* estritamente necessário para sua etapa, mantendo o ambiente previsível.

---
*Estudo desenvolvido para aprofundamento prático em frameworks de Multi-Agentes (como LangGraph e CrewAI) e construção de fluxos confiáveis de IA.*