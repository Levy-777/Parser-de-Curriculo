<div align="center">
  <img src="https://img.shields.io/badge/Status-Propriet%C3%A1rio%20%7C%20Showcase-8b5cf6?style=for-the-badge" alt="Status do Projeto">
  <img src="https://img.shields.io/badge/AI-vLLM%20%7C%20Gemini%202.5-10b981?style=for-the-badge" alt="AI Stack">
  <br><br>
  <h1>Recrutador IA: Motor de Matching Semântico Inclusivo</h1>
  <p><b>Um sistema ATS (Applicant Tracking System) de nova geração baseado em Modelos de Linguagem (LLMs) e Busca Vetorial.</b></p>
  <p><b>Acesse a Interface: <a href="https://levy-777.github.io/Parser-de-Curriculo/">https://levy-777.github.io/Parser-de-Curriculo/</a></b></p>
</div>

<br>

> **Nota sobre o Código-Fonte:** Este repositório atua como um showcase da interface front-end e da documentação arquitetural do projeto. Os algoritmos de matching vetorial, a engenharia de prompts dos LLMs e o backend de processamento (Python/FastAPI) são mantidos como código fechado (Closed Source) por razões acadêmicas e de propriedade intelectual.

## O Problema

Plataformas tradicionais de recrutamento e seleção baseiam seus filtros na correspondência exata de palavras-chave. Isso gera dois grandes problemas no mercado de RH:
1. **O descarte de Joias Ocultas:** Profissionais altamente capacitados são ignorados pelo sistema simplesmente porque não possuem o termo exato buscado, mesmo dominando tecnologias funcionalmente idênticas.
2. **A ditadura da experiência:** Sistemas tradicionais pesam excessivamente o tempo de experiência formal, prejudicando perfis iniciantes (juniores e estagiários) que possuem excelente fundamentação técnica e projetos práticos.

## A Filosofia da Solução

Este projeto foi desenvolvido para subverter a lógica tradicional, criando um funil de triagem inclusivo e cognitivo:

*   **Busca por Contexto, não por Exatidão:** Utilizando expansão semântica e modelos de Embeddings, o sistema entende correlações tecnológicas e a similaridade estrutural entre ferramentas. 
    *   *Exemplificação Prática:* Em um sistema tradicional, um desenvolvedor experiente em JavaScript puro que aplique para uma vaga de Python seria sumariamente descartado na triagem inicial. No nosso motor semântico, o algoritmo compreende que ambas são linguagens de alto nível, dinâmicas, multiparadigma e com curvas de aprendizado estruturais semelhantes. O candidato, em vez de reprovado, é mantido no funil como uma possível contratação estratégica, valorizando sua lógica de programação sobre a sintaxe específica.
*   **Democratização para Iniciantes:** O algoritmo redistribui os pesos da avaliação. Para vagas de base, ele valoriza ativamente habilidades técnicas e projetos acadêmicos/pessoais, balanceando a falta de experiência formal.
*   **Penalização de Sobrequalificação:** O motor possui heurísticas matemáticas que penalizam perfis muito seniores aplicando para vagas juniores, garantindo aderência estrita à realidade da vaga e evitando problemas de retenção de talentos para a empresa.

## Arquitetura de Alto Nível

O sistema opera em uma arquitetura distribuída e modular (Microsserviços em Nuvem e Interface Web Estática), processando os dados em três grandes etapas:

### 1. Ingestão e Extração (Parser via vLLM)
Currículos em formato PDF são ingeridos por um servidor dedicado processando LLMs locais (Qwen 2.5 7B via vLLM). Diferente de parsers baseados em OCR tradicional, o LLM lê, interpreta e estrutura os dados de forma inteligente, lidando com formatações complexas e extraindo um schema JSON padronizado.

### 2. Matching Semântico e Busca Vetorial
Os dados estruturados são enviados para o motor central. As exigências da vaga e o perfil do candidato são transformados em vetores de alta dimensionalidade usando modelos SentenceTransformers. O ranqueamento é calculado via Similaridade de Cosseno aliada a um Dicionário de Correlações proprietário.

### 3. Revisão Qualitativa (Agente Gemini)
Os candidatos pré-filtrados passam por uma última revisão por um agente de IA alimentado pela API do Google Gemini 2.5 Flash. O modelo atua como um Tech Recruiter, gerando um parecer qualitativo para cada candidato, justificando pontos fortes, gaps técnicos e o motivo de sua posição no ranking.

## Tecnologias Utilizadas (Backend Fechado)

*   **Inteligência Artificial & NLP:** HuggingFace, vLLM (Qwen 2.5), Google Gemini 2.5 Flash, SentenceTransformers (paraphrase-multilingual-MiniLM-L12-v2).
*   **Engenharia de Dados:** Extração estruturada (JSON), Numpy, Scikit-learn (Cosine Similarity).
*   **Backend & Infra:** Python, FastAPI, Uvicorn, Ngrok (Túneis reversos).
*   **Frontend (Visível neste repositório):** HTML5, Vanilla CSS (Glassmorphism UI), JavaScript (Async Fetch).

---
<div align="center">
  <i>Desenvolvido por Levy José Santos Montes, Gabriel da Pureza Irmão e Guilherme Santana Dória para TCC na FATEC Rubens Lara.</i>
</div>
