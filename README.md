# 🔍 SearchRAG

> **Um motor de busca e recuperação avançado com interface visual, projetado para executar um algoritmo rigoroso de busca híbrida de alta precisão em bancos vetoriais, combinando semântica profunda com correspondência exata de palavras-chave e reconstrução contextual por vizinhança mecânica.**

---

## 📝 Descrição do Projeto

O **SearchRAG** é uma interface desktop feita exclusivamente para buscar informações com precisão cirúrgica em bancos de dados populados. Ele elimina o risco de respostas inventadas, fora de contexto ou vagas, sendo ideal para áreas críticas que exigem respostas exatas e conferência imediata de fontes textuais, como medicina, engenharia ou direito.

O aplicativo opera sob um algoritmo rigoroso estruturado em três etapas principais:

1. **Busca Híbrida e Reranking:** O sistema realiza duas consultas paralelas ao banco de dados no momento da pesquisa. Ele aplica 70% de peso para a busca semântica por similaridade de cosseno (que entende o conceito e sinônimos da pergunta) e 30% de peso para a busca por palavras-chave/BM25 (que localiza termos exatos, códigos, artigos de lei ou números de prontuário), recalculando e refinando o ranking de relevância.

2. **Algoritmo de Janela de Contexto Dinâmica (Vizinhos Colados):** Ao identificar o bloco de texto mais preciso (índice N), o motor faz um resgate mecânico imediato dos blocos adjacentes originais: os blocos anteriores (N-1 e N-2) e os blocos posteriores (N+1 e N+2).

3. **Recomposição Determinística:** O aplicativo cola esses 5 blocos de forma linear e cronológica na tela, destacando visualmente o fragmento principal. Isso garante que parágrafos que continuavam na página seguinte ou ressalvas descritas na página anterior nunca sejam omitidos, entregando um ambiente 100% determinístico e auditável.

---

## 🛠️ Tecnologias Utilizadas

O sistema foi otimizado para entregar buscas matemáticas eficientes sem travar a experiência do usuário:

* **Gerenciamento:** Isolado de ponta a ponta com o ecossistema **uv**, rodando pacotes em ambientes virtuais blindados de conflitos de biblioteca.
* **Interface Gráfica (GUI):** Desenvolvida em **PyQt6**, contendo barras de ajuste dinâmico de pesos de precisão, visualizadores de texto rico com realce de termos e painéis dedicados a rastrear metadados das fontes.
* **Arquitetura de Software:** Estruturado em **Arquitetura em Camadas (Layered Architecture)**, garantindo que o algoritmo matemático complexo e as transações de banco rodem em threads secundárias de forma independente das telas.
* **Comunicação e Banco de Vetores:** Conexão otimizada via drivers relacionais nativos para efetuar buscas por similaridade de cosseno com a extensão de vetores do banco alvo e cálculos rápidos de ordenação com **NumPy**.

---

## 🚀 Como Executar o App Localmente

Por ser um sistema de alta precisão focado em rodar ao lado dos seus servidores de dados, ele pode ser instalado de forma simples. Baixe a versão recomendada para o seu ambiente corporativo ou pessoal:

Windows: 📥 Baixar executável para Windows (x64)

Linux: 📥 Baixar binário para Linux (x64)

Após baixar, basta dar um duplo clique no executável para abrir o seu terminal de pesquisas avançadas.

---
<p align="center">Developed by <b>Ldov - AI & IT Solutions</b> </p>
