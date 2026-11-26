# PENDÊNCIAS — Streaming-Musica-Deezer-React (PH Music)

Este documento rastreia o status de validação, o backlog técnico e os requisitos de infraestrutura da aplicação web de streaming e player musical integrada à API pública do Deezer.

---

## 1. ✅ Escopo Validado e Concluído
- **Frontend Moderno & Otimizado:** React 19, Vite 6, Material UI v7 (MUI), React Router DOM v7.5 e Emotion.
- **Divisão de Chunks (Code-Splitting):** Configurado `manualChunks` no Rollup (`vendor-react`, `vendor-mui`) eliminando alertas de tamanho de bundle e acelerando carregamento inicial.
- **Esteira de CI/CD Completa:** Workflow do GitHub Actions configurado (`.github/workflows/ci.yml`) executando linting, testes Vitest e build de produção a cada push.
- **Testes Automatizados:** **201/201 testes aprovados** (17 test suites rodando via Vitest com Happy DOM).
- **Qualidade de Código:** Validação estrita do ESLint com zero erros e build de produção concluído com sucesso (`vite build`).
- **Funcionalidades Principais Implementadas:**
  - Busca em tempo real com debounce para artistas, faixas, álbuns e playlists.
  - Player fixo no rodapé com suporte a prévia de 30s da API Deezer e fallback para integração com YouTube Player.
  - Gerenciamento de favoritos, histórico de reproduções e playlists editáveis com persistência em `localStorage` e sincronização opcional via Supabase.
  - Sistema de notificações Toast e tratamento de erros com Error Boundary e Skeleton Loaders.

---

## 2. 📋 Backlog de Engenharia (Próximas Melhorias Opcionais)
- [ ] Implementar visualizador de espectro de áudio com Web Audio API.

---

## 3. ⚙️ Infraestrutura e Dependências Externas (Requer Ação do Desenvolvedor)
- **Supabase (Opcional):** Configurar `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY` no arquivo `.env` para sincronização em nuvem da biblioteca de favoritos e playlists do usuário.

