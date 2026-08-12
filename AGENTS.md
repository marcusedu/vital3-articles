# AGENTS.md — Diretrizes de Redação e Publicação da Academia Vital3

Este documento serve como guia de referência e estilo para agentes de IA e contribuidores humanos encarregados de redigir, traduzir ou cadastrar novos artigos na **Academia Vital3**.

---

## 🖤 1. O Tom da Academia Vital3: "Dark Industrial"

O Vital3 não é um aplicativo de autoajuda comum. O tom deve ser **sóbrio, ultraobjetivo, realista e pragmático**.

- **Menos Discurso, Mais Execução**: Evite promessas exageradas, jargões motivacionais vazios ("você é um campeão", "alcance as estrelas") ou textos excessivamente calorosos.
- **Autoresponsabilidade**: A mensagem central é de que a disciplina e o foco dependem de decisões antecipadas e da construção de estruturas externas (sistemas), não de impulsos emocionais momentâneos.
- **Estilo Cortante**: Frases mais curtas, vocabulário direto e argumentos baseados em fatos práticos do cotidiano e em atitudes concretas.
- **Fricção Recompensadora**: O desconforto da escolha diária de limitar prioridades é encarado como o preço real de qualquer avanço relevante.

---

## 🧱 2. Estrutura do Artigo

Todos os artigos devem ser escritos em Markdown padrão e conter:

1. **Título (`# Título`)**: Uma única tag `<h1>` clara e impactante.
2. **Introdução Curta**: 1 a 2 parágrafos situando o problema.
3. **Seções Principais (`## Seção`)**: Tópicos estruturados com explicações diretas e ações imediatas.
4. **Listas com Bullet Points (`-`)**: Usadas para separar passos claros ou itens de diagnóstico para facilitar a leitura no app móvel.
5. **Destaques em Negrito**: Use **negrito** de forma estratégica para palavras-chave cruciais, sem sobrecarregar o texto.

---

## 🎨 3. Integrações Especiais no Aplicativo (CTAs)

O leitor Markdown do Vital3 suporta a renderização de botões de ação nativos no dispositivo inseridos diretamente no meio do texto através de marcadores especiais:

- **Configuração de Tempo de Tela**: 
  - Marcador: `[OS_ACTION_BUTTON:screen_time]`
  - Comportamento: O aplicativo substitui este texto por um botão styled que abre diretamente as configurações nativas de "Tempo de Tela" (iOS) ou "Bem-Estar Digital" (Android).
  - Uso ideal: Apenas em artigos focados em redução de tempo de uso ou distrações em celulares.

---

## 🏷️ 4. Categorias Aceitas

Mantenha a organização dos artigos dentro de uma dessas categorias estruturadas:
- `Foco & Tecnologia`
- `Filosofia & Foco`
- `Constância & Hábitos`
- `Saúde & Energia`

---

## 🌐 5. Tradução e Internacionalização (i18n)

Sempre que um artigo for inserido, as traduções para **Português (`pt`)**, **Inglês (`en`)** e **Espanhol (`es`)** devem ser providenciadas nos caminhos correspondentes em `articles/[id]/[lang].md` e cadastradas em `articles.json` com suas respectivas chaves de idioma para evitar falhas de visualização no app.
