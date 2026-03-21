### Tutorial Analítico: O Guia de Interpretação Qualitativa

A presente aplicação destina-se a pesquisadores, docentes e discentes interessados na análise de dados qualitativos em diferentes campos do saber. Seu design possui aplicabilidade evidente nas áreas de saúde coletiva, gestão pública e ciências humanas. A plataforma atende tanto a usuários leigos, oferecendo interfaces intuitivas e assistentes de inteligência artificial para apoio analítico, quanto a especialistas em estatística textual que demandam rigor metodológico, reprodutibilidade e controle granular sobre hiperparâmetros matemáticos.

O objetivo pedagógico e investigativo do sistema concentra-se em reduzir a opacidade algorítmica ('caixa-preta') frequentemente associada a softwares proprietários. A ferramenta compromete-se a investigar padrões discursivos ocultos, trajetórias semânticas e polarizações ideológicas por meio de um método sólido. Dessa forma, viabiliza a transformação de transcrições complexas e não estruturadas em evidências visuais e estatísticas claras, respeitando a natureza exploratória das pesquisas.

---

#### Módulo 2: Léxico e Frequência

**1. ☁️ Nuvem de Palavras**
* **Conceito:** Representação de estatística descritiva primária (univariada).
* **Aplicação:** Dimensiona visualmente o tamanho da palavra de forma proporcional à sua frequência matemática no *corpus*.
* **Controles:** Ocultação de palavras curtas, limites máximos de volume, mascaramento geométrico e modelo de escalonamento.
* **Interpretação:** É importante para evidenciar as categorias de base do discurso em fases exploratórias. Palavras centrais e gigantescas formam a "espinha dorsal" da preocupação do entrevistado.

**2. 🔍 KWIC (Key Word In Context)**
* **Conceito:** Análise de vizinhança discursiva e coocorrência quantitativa estrita.
* **Aplicação:** Localiza todas as menções a um termo específico e extrai *N* palavras antes e depois. Calcula a *Força de Associação (PMI)* entre o termo-alvo e o seu entorno.
* **Controles:** Inserção do termo-alvo, tamanho da janela de vizinhança e ajuste de um filtro de rigor logarítmico (PMI).
* **Interpretação:** Funciona como um selo de segurança do método qualitativo. O filtro PMI superior a 0 assegura que dois termos aparecem juntos mais vezes do que o esperado pelo simples acaso. Isso oferece respaldo estatístico para interpretar o real uso do termo, evitando generalizações.

**3. 📚 Dicionários Léxicos (Categorização Dedutiva)**
* **Conceito:** Análise temática categorial orientada por teoria (Top-Down).
* **Aplicação:** Conta a ocorrência de listas de palavras pertencentes a "Eixos Analíticos" e plota o seu peso num Gráfico de Radar duplo e Árvore Hierárquica.
* **Controles:** Quantidade de eixos, acionamento do **Assistente Temático (IA)** e Limiar de Similaridade.
* **Interpretação:** Usa-se esse recurso quando se possui uma hipótese prévia. A IA atua como apoio hermenêutico. Na opção 'Similaridade Semântica', o valor 0.65 permite capturar sinônimos e paráfrases. As classificações vetoriais não são garantias prévias ou definições absolutas. Elas representam horizontes que a pesquisa se compromete a investigar por meio de um método sólido. O investigador deve realizar a leitura atenta da tabela de resultados para comprovar a aderência real da sentença.

**4. 🎭 Análise de Sentimento (Polaridade)**
* **Conceito:** Detecção determinística de valência emocional em textos.
* **Aplicação:** Varre o documento analisando frase por frase, isolando as intercorrências de negação e partículas adversativas.
* **Controles:** Adição de léxicos customizados e acionamento do **Assistente Léxico (IA)**.
* **Interpretação:** Importante para a mensuração de clima. Se a "Taxa de Neutros" ficar acima de 70%, sugere-se que o pesquisador refine o dicionário com termos locais para captar com precisão o jargão de aprovação ou queixa.

---

#### Módulo 3: Estatística Espacial (Análise Multivariada)

**1. 🕸️ Similitude (Grafo de Rede)**
* **Conceito:** Topologia de centralidade e conexão não supervisionada.
* **Aplicação:** Desenha um grafo no qual esferas representam palavras e a espessura das linhas quantifica a constância com que aparecem juntas.
* **Controles:** Poda do grafo, física espacial interativa (força de repulsão magnética) e coloração por Sentimento Espacializado.
* **Interpretação:** Revela a "constelação de ideias". Termos no meio da rede classificam-se como "conceitos-ponte", fundamentais para a fluidez da narrativa.

**2. 🔗 Grafo Bipartido**
* **Conceito:** Conexão entre a Origem (documento) e a Variável Lexical (TF-IDF).
* **Aplicação:** Relaciona a fonte aos nós das palavras que lhe são estatisticamente exclusivas.
* **Controles:** Ajuste do volume de palavras exclusivas extraídas de cada arquivo.
* **Interpretação:** Compara a singularidade. Se a rede bifurcar completamente, demonstra-se que grupos distintos usam jargões radicalmente separados.

**3. 📈 Componentes Principais (PCA)**
* **Conceito:** Redução dimensional ortogonal e agrupamento estatístico via algoritmo K-Means.
* **Aplicação:** Achata a matriz para um plano 2D, agrupando palavras semanticamente similares.
* **Controles:** Definição da quantidade de classes matemáticas (clusters).
* **Interpretação:** Demonstra polarizações de foco evidenciando correntes de pensamento concorrentes no texto.

**4. 🌌 Mapeamento Não-Linear (t-SNE)**
* **Conceito:** Topologia estocástica focada em vizinhança probabilística.
* **Aplicação:** Desfaz "emaranhados" de palavras complexas e identifica nichos de sentido que métodos lineares omitem.
* **Controles:** Ajuste do índice de Perplexidade e número de classes.
* **Interpretação:** Evidencia nichos discursivos e vocabulários muito específicos.

**5. 📊 Modelagem de Tópicos (LDA)**
* **Conceito:** Aprendizado não supervisionado via Alocação Latente Dirichlet.
* **Aplicação:** Descobre empiricamente quais assuntos estruturais habitam o texto.
* **Controles:** Quantidade de tópicos e botão para rotulagem semântica pela Inteligência Artificial.
* **Interpretação:** Recurso de pesquisa indutiva (Bottom-Up). A IA atua na etapa hermenêutica sugerindo nomes formais para os agrupamentos matemáticos gerados.

**6. 🔥 Mapa de Calor (Heatmap Lexical)**
* **Conceito:** Densidade cromática por matriz de exclusividade (TF-IDF).
* **Aplicação:** Tabela térmica que cruza o vocabulário (colunas) e os grupos (linhas).
* **Controles:** Inserção de um Dicionário de Foco restritivo e paletas de cor.
* **Interpretação:** Fundamental para mapear a posse discursiva e comparar quais grupos adotaram mais fortemente determinados termos.

**7. 🌳 Dendrograma (CHD Palavras)**
* **Conceito:** Classificação Hierárquica Descendente de vocabulário.
* **Aplicação:** Usa a distância euclidiana para estruturar uma "árvore genealógica" conectando palavras por proximidade de uso.
* **Controles:** Ajuste do número total de termos.
* **Interpretação:** Exibe as partições lógicas da fala. Termos que compartilham ramificações curtas formam núcleos indissociáveis.

**8. 📑 Dendrograma (CHD Documentos)**
* **Conceito:** Macrocomparação da similitude estrutural interdocumental.
* **Aplicação:** Avalia o vetor vocabular integral de cada arquivo identificando "almas gêmeas" semânticas.
* **Controles:** Configuração autônoma.
* **Interpretação:** Afere o grau de convergência global ou ruptura corporativa entre os entrevistados.

**9. 🔀 Cruzamento (LDA × Sentimento)**
* **Conceito:** Análise multivariada mista.
* **Aplicação:** Após descobrir os tópicos latentes, mede a polaridade embutida em cada um desses eixos.
* **Controles:** Quantidade de partições e dicionários valorativos.
* **Interpretação:** Responde à pergunta central sobre os afetos de cada tema específico.

**10. 📈 Fluxo Semântico Temporal**
* **Conceito:** Cartografia cronológica intra-sujeito.
* **Aplicação:** Fatia o documento linearmente para traçar a flutuação do sentimento e mapear a Trajetória Discursiva.
* **Controles:** Quantidade de recortes de tempo.
* **Interpretação:** O mapa demonstra as viradas de assunto; curvas acentuadas provam momentos em que o entrevistado modificou o eixo da sua fala.

**11. 🧠 Regressão Logística (Termos × Contextos)**
* **Conceito:** Aprendizado de máquina supervisionado para discriminação contextual.
* **Aplicação:** Treina um algoritmo para descobrir quais palavras servem como "assinaturas" de contextos. Produz Mapa de Bolhas (Aderência).
* **Controles:** Foco léxico, ajuste de regularização (C) e seleção de eixos.
* **Interpretação:** Termos com altos coeficientes positivos puxam um documento para aquela classe. O Mapa de Bolhas comprova se há documentos invadindo o espaço semântico do grupo vizinho.

**12. 🌌 Espaço Semântico 3D (Galáxia)**
* **Conceito:** Projeção topológica de alta dimensionalidade.
* **Aplicação:** Projeta o vocabulário mais relevante em um espaço tridimensional orbitável. Termos geograficamente próximos partilham contextos de uso semelhantes, sendo agrupados em 'constelações' pelo algoritmo K-Means.
* **Controles:** Escolha do algoritmo base (PCA ou t-SNE), número de constelações e volume de palavras renderizadas.
* **Interpretação:** A proximidade reflete padrões matemáticos de frequência, e não sinonímia exata. As projeções geradas representam horizontes que a pesquisa se compromete a investigar por meio de um método sólido, permitindo rotacionar o gráfico para encontrar ângulos de convergência lexical.

**13. ⭕ Diagrama Circular de Transição**
* **Conceito:** Topologia relacional radial (Chord Diagram).
* **Aplicação:** Mapeia as conexões e coocorrências do discurso em um formato circular. Essa geometria limpa a poluição visual de redes emaranhadas.
* **Controles:** Quantidade máxima de nós (palavras) e tamanho das fontes.
* **Interpretação:** Permite identificar facilmente os 'nós de trânsito' — palavras centrais que cruzam e sustentam as narrativas. Exibe a proximidade textual intrafrasal, evidenciando o fluxo do raciocínio em vez de relações causais puras.

**14. 🕸️ Grafo de Similitude (Árvore Kruskal)**
* **Conceito:** Árvore Geradora Mínima (Minimum Spanning Tree - MST).
* **Aplicação:** Mapeia a coocorrência de termos e aplica o algoritmo de Kruskal para extrair apenas as conexões mais fortes e estruturais, eliminando redundâncias.
* **Controles:** Volume de palavras que formarão a espinha dorsal e tamanho tipográfico.
* **Interpretação:** Útil para revelar a matriz narrativa do corpus, identificando conceitos centrais (nós de maior grau) e como os temas periféricos se ramificam a partir deles. A árvore força uma topologia de ramificação estrita, ocultando conexões secundárias transversais para destacar a macroestrutura principal do discurso.