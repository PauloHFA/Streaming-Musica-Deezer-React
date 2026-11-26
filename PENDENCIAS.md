# PENDÊNCIAS — PH Music (Deezer Clone com React 19 e Vite)

Este documento rastreia o status de validação, o backlog técnico e os requisitos de infraestrutura da aplicação web de player musical integrada à API pública do Deezer.

---

## 1. ✅ Escopo Validado e Concluído
- **Frontend Moderno:** React 19, Vite 6, Material UI v7 (MUI), React Router DOM v7.5 e Tailwind/Emotion.
- **Testes Automatizados:** **201/201 testes aprovados** (17 test suites rodando via Vitest com Happy DOM).
- **Qualidade de Código:** Validação estrita do ESLint com zero erros e build de produção concluído com sucesso (`vite build`).
- **Funcionalidades Principais Implementadas:**
  - Busca em tempo real com debounce para artistas, faixas, álbuns e playlists.
  - Player fixo no rodapé com suporte a prévia de 30s da API Deezer e fallback para integração com YouTube Player.
  - Gerenciamento de favoritos, histórico de reproduções e playlists editáveis com persistência em `localStorage` e sincronização opcional via Supabase.
  - Sistema de notificações Toast e tratamento de erros com Error Boundary e Skeleton Loaders.

---

## 2. 📋 Backlog de Engenharia (Próximas Melhorias Opcionais)
- [ ] Aplicar divisão de chunks via `manualChunks` no Rollup para otimizar os avisos de tamanho de bundle do Vite (> 500 kB).

---

## 3. ⚙️ Infraestrutura e Dependências Externas (Requer Ação do Desenvolvedor)
- **Supabase (Opcional):** Configurar `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY` no arquivo `.env` para sincronização em nuvem da biblioteca de favoritos e playlists do usuário.
