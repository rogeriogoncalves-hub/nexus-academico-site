# **Quali.analise Visioespacial**

O **Quali.analise Visioespacial** é uma plataforma avançada desenvolvida em Python (via Streamlit) focada na análise léxica e estatística textual multivariada para pesquisas qualitativas. O sistema propõe-se a converter corpus discursivos em representações visuais, métricas estatísticas e projeções topológicas de alta precisão.

A solução opera por processamento local e em contêineres efêmeros, assegurando o sigilo e a confidencialidade de dados de pesquisa. A plataforma permite parametrização granular e explícita de todos os filtros morfológicos, dicionários léxicos e procedimentos de redução dimensional. Essa abordagem supera a opacidade ("caixa-preta") das soluções genéricas de mercado e garante rigorosa auditabilidade para publicação científica.

---

## 🚀 Estrutura e Funcionalidades

A aplicação estrutura-se em um sistema de autenticação e três macro-módulos metodológicos.

### 0. 🔐 Autenticação e Gestão de Projeto
* **Acesso Seguro:** Tela de login obrigatória requerendo perfil de usuário, e-mail e senha de acesso configurada em variáveis de ambiente (Railway) para liberação da interface. A arquitetura está preparada para integração com plataformas de gestão de identidade (ex: Clerk/Stripe via tokens de URL).
* **Armazenamento Efêmero:** Aviso de inatividade para ambientes em nuvem. O banco de dados é excluído automaticamente após a suspensão, exigindo exportação de resultados.
* **Relatório Metodológico:** Exportação em formato `.txt` de um registro auditável contendo todas as configurações ativas (filtros, agrupamentos, status das stopwords), ideal para compor o apêndice metodológico de artigos e dissertações.

### 1. 📥 Importação e Gerenciamento
* **Formatos Suportados:** PDF, DOCX e TXT.
* **Segurança Metodológica:** Isolamento rigoroso de sessão. O processamento ocorre 100% na máquina ou contêiner de execução temporária, sem retenção permanente de base de dados para terceiros.
* **Gestão de Documentos:** Permite renomear arquivos diretamente na interface ou excluí-los individualmente.
* **Alerta Epistemológico Integrado:** Orientação explícita para a limpeza prévia do corpus (remoção das falas dos entrevistadores ou roteiros) antes do carregamento. Esse procedimento previne o enviesamento da coocorrência.
* **Agrupamento Automático (Prefixo):** O sistema reconhece prefixos nos nomes dos arquivos (ex: `MED_01`, `FIS_02`). Isso permite que a análise espacial una estatisticamente documentos do mesmo estrato, formando macrocategorias discursivas.

### 2. 🔤 Léxico e Frequência (Análise Univariada e Contextual)
Exploração descritiva do vocabulário, com diagnóstico automático da qualidade da transcrição e aplicação de filtros combinados (plural, oralidade, base gramatical e detecção de bigramas).

* **Métricas Dinâmicas (Diagnóstico):** Avaliação de Volume de Dados (Tokens), Riqueza Vocabular (Types), Densidade Lexical (TTR) e Extensão Média de Sentença, indicando a fluência e a articulação do discurso.
* **☁️ Nuvem de Palavras:** Representação vetorial com tipografia customizável, máscaras geométricas, filtros de tamanho mínimo e escalonamento linear ou hierárquico. Exportação nativa em PNG 300 dpi.
* **🔍 KWIC (Key Word In Context):** Extração de coocorrências empíricas ao redor de um termo-alvo. O módulo calcula a *Força de Associação (PMI - Pointwise Mutual Information)*, permitindo aplicar um filtro de relevância (corte logarítmico) para destacar laços semânticos reais em vez de repetições triviais.
* **📚 Dicionários Léxicos (Categorização Dedutiva):** Mapeamento por meio de eixos teóricos definidos pelo usuário.
  * **Assistente Temático (IA):** Integração com modelos de linguagem (Amostragem Estratificada via Kimi K2.5 ou DeepSeek Reasoner) para dedução hermenêutica das macrocategorias. A IA atua como assistente para deduzir eixos analíticos diretamente do texto livre ou ancorado em referencial teórico.
  * **Motor Vetorial de Similaridade Semântica:** Opcional à correspondência exata. Usa embeddings para agrupar frases por aproximação de sentido. Inclui ajuste de Limiar de Pertencimento (Threshold). O valor padrão de 0.65 estabelece um equilíbrio matemático para identificar paráfrases e sinônimos.
  * Plotagem dos resultados em Gráfico de Radar duplo (frequência absoluta e relativa) e Árvore Hierárquica (Sunburst).
* **🎭 Análise de Sentimento (Polaridade):** Motor lexicográfico complexo para identificação de bigramas, inversão por partículas negativas (ex: "não") e modulação por conjunções adversativas (ex: "mas").
  * **Assistente Léxico (IA):** Ferramenta autônoma para mapear jargões específicos de queixa ou aprovação no vocabulário do próprio entrevistado.
  * Inclui auditoria de Cobertura Léxica, Taxa de Neutros e exportação dos escores detalhados por sentença.

### 3. 🌐 Estatística Espacial (Análise Multivariada)
Exploração matemática avançada, conectando variáveis por similaridade, probabilidade e redução de dimensionalidade.

* **🕸️ Similitude (Grafo Pyvis):** Topologia interativa de conexões lexicais. Apresenta ferramentas ajustáveis de física espacial (força de repulsão magnética e tração de mola) para organizar a rede. Permite colorir as esferas com base na valência emocional (Sentimento Espacializado).
* **🔗 Grafo Bipartido:** Relaciona os documentos (ou grupos) aos seus termos de maior exclusividade estatística (TF-IDF), evidenciando os perfis discursivos singulares de cada estrato da pesquisa.
* **📈 Componentes Principais (PCA) e 🌌 t-SNE:** Projeções cartesianas e não-lineares. Aplicam o algoritmo de *K-Means* para criar agrupamentos geométricos baseados na distância semântica. Incluem uma tabela de diagnóstico emocional médio para cada cluster gerado.
* **📊 Modelagem de Tópicos (LDA):** Descoberta indutiva via *Latent Dirichlet Allocation*. Identifica construtos latentes e mede a "Estabilidade Semântica" executando rodadas com sementes diferentes. Conta com a Inteligência Artificial para sugerir rótulos acadêmicos precisos para cada eixo estrutural encontrado.
* **🔥 Mapa de Calor (Heatmap):** Gráfico de densidade térmica que traça o uso intensivo de um vocabulário específico (Dicionário de Foco) ou das palavras mais frequentes por documento ou categoria comparada.
* **🌳 Dendrogramas (CHD Palavras e Documentos):** Classificação Hierárquica Descendente baseada em distâncias euclidianas e critério de ligação de Ward. Cria árvores de aproximação lexical ou similitude interdocumental.
* **🔀 Cruzamento (LDA × Sentimento):** Processamento mimetizado que interliga o espaço semântico latente à valência emocional, mapeando de forma quantitativa qual tópico levanta mais queixas ou elogios.
* **📈 Fluxo Semântico Temporal:** Fatiamento longitudinal das entrevistas para gerar gráficos da evolução cronológica da polaridade (Início → Fim). Inclui o mapeamento da **Trajetória Discursiva** no espaço semântico, evidenciando mudanças bruscas de assunto ao longo do tempo.
* **🧠 Regressão Logística (Termos × Contextos):** Modelo de aprendizado supervisionado (Machine Learning). Mede a importância discriminativa dos termos para cada contexto (log-odds). Gera um Heatmap de Coeficientes e um Mapa de Bolhas (Aderência Contextual) indicando como os documentos se distribuem probabilisticamente entre as classes.
* **🌌 Espaço Semântico 3D (Galáxia):** Projeta o vocabulário mais relevante em um espaço tridimensional interativo. Termos geograficamente próximos partilham contextos de uso semelhantes, agrupados por K-Means em 'constelações' discursivas orbitáveis.
* **⭕ Diagrama Circular de Transição:** Mapeia as conexões e coocorrências do discurso em um grafo radial perfeito (Chord Diagram), limpando a poluição visual para identificar 'nós de trânsito' na narrativa.
* **🕸️ Grafo de Similitude (Árvore Kruskal):** Aplica o algoritmo de Kruskal (Árvore Geradora Mínima) para extrair as conexões intrafrasais mais fortes, eliminando redundâncias visuais e destacando a espinha dorsal narrativa do corpus.

---

## 🛠️ Requisitos e Deploy (Ambientes Nuvem)
A arquitetura *Clean* baseia-se em módulos separados para garantir a facilidade de manutenção. É imperativo manter a estrutura de diretórios do repositório:

* `app.py` (Controlador da interface Streamlit).
* `database.py` (Gestor do banco de dados SQLite e persistência).
* Pasta `pipeline/`:
  * `preprocessamento.py` (Limpeza, normalização e heurísticas morfológicas).
  * `lexico.py` (Frequências univariadas, PMI e pontuação de polaridade).
  * `espacial.py` (Cálculos matemáticos, vetores TF-IDF, matrizes e Machine Learning).
  * `visualizacao.py` (Renderização de gráficos Plotly, Pyvis e Wordclouds).
* `api_clients.py` (Orquestrador de chamadas externas para as APIs de LLMs como OpenAI, Together AI e DeepSeek).
* `requirements.txt` (Dependências do ambiente).

**Nota importante para Deploy na Railway:**
O aplicativo foi otimizado para execução em instâncias com 8GB de RAM (Plano Hobby). Configurações sensíveis, como `APP_PASSWORD` e chaves de API, devem ser declaradas exclusivamente no painel de variáveis de ambiente do serviço, mantendo o repositório GitHub estritamente privado. A atual arquitetura de armazenamento efêmero demanda exportações manuais contínuas para evitar perdas de progresso durante reinicializações do contêiner.

**Comentários adicionais:**
O aplicativo Quali.analise Visioespacial funciona como uma plataforma de análise léxica e estatística textual voltada para a pesquisa qualitativa. O processamento isolado assegura o rigor metodológico e preserva o sigilo dos dados empíricos. Tal característica mostra-se importante para investigações envolvendo relatos complexos em ambientes institucionais e comunitários. 

Na comunicação da interface com o pesquisador, a cautela acadêmica exige que as projeções geradas pelos algoritmos e pela IA sejam apresentadas de forma cuidadosa. Os mapas gerados representam horizontes exploratórios que a pesquisa se compromete a investigar por meio de um método sólido, não constituindo garantias prévias ou respostas definitivas e irrefutáveis sobre o objeto estudado.