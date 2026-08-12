# Vital3 Articles

Repositório público e centralizado de artigos e guias práticos da **Academia Vital3**. 

Este repositório funciona como uma CDN estática sem servidor. O aplicativo Vital3 busca o arquivo `articles.json` para mapear os metadados dos artigos disponíveis e, em seguida, baixa os respectivos arquivos Markdown de forma localizada conforme o idioma do usuário.

---

## 📂 Estrutura de Diretórios

```text
vital3-articles/
├── articles.json                  # Índice centralizado dos artigos (Banco de Dados)
├── README.md                      # Instruções de uso deste repositório
├── AGENTS.md                      # Diretrizes de redação, estilo e publicação (para IAs e Contribuidores)
└── articles/                      # Conteúdo dos artigos
    ├── como_reduzir_tempo_de_tela/
    │   ├── pt.md                  # Versão em Português
    │   ├── en.md                  # Versão em Inglês
    │   └── es.md                  # Versão em Espanhol
    └── imposto_da_inteligencia/
        ├── pt.md
        ├── en.md
        └── es.md
```

---

## 🗂️ Estrutura do Índice (`articles.json`)

O arquivo `articles.json` na raiz é o banco de dados de metadados. Cada objeto de artigo deve seguir o seguinte esquema de internacionalização:

```json
[
  {
    "id": "identificador_unico",
    "category": {
      "pt": "Categoria em Português",
      "en": "Category in English",
      "es": "Categoría en Español"
    },
    "title": {
      "pt": "Título em Português",
      "en": "Title in English",
      "es": "Título en Español"
    },
    "description": {
      "pt": "Descrição em Português",
      "en": "Description in English",
      "es": "Descripción en Español"
    },
    "targetOS": "all", // "all" | "android" | "ios"
    "publishDate": "2026-08-12T12:00:00Z",
    "markdownPath": "articles/identificador_unico"
  }
]
```

---

## ⚙️ Como o App Consome os Artigos

1. O app lê o índice remoto via `GET` no link raw do GitHub:
   `https://raw.githubusercontent.com/[usuario]/vital3-articles/main/articles.json`
2. O app localiza as chaves correspondentes (`title`, `description`, `category`) usando a linguagem ativa do sistema do usuário (`pt`, `en`, `es`, caindo em `pt` por padrão).
3. Ao abrir o detalhe do artigo, o app monta a URL do arquivo markdown correspondente:
   `https://raw.githubusercontent.com/[usuario]/vital3-articles/main/articles/[markdownPath]/[languageCode].md`
   Exemplo: `.../articles/imposto_da_inteligencia/pt.md`
