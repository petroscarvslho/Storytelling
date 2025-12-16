# Diario de Progresso - Storytelling USG-Game

## 2025-12-16 - Sessao 3: Novos Arquivos de Contexto

### Criado
- **resumo_contexto.md** - Resumo completo de tudo (projetos, decisoes, duvidas)
- **ramificacao.md** - Esquema de como funcionam as ramificacoes

### Teste de Geracao Leonardo (mobile/desktop)
- Retratos 768x1024 (seed 424242, guidance 7):
  - protagonista: neutro/feliz/preocupado
  - Dra. Costa: neutro/feliz/preocupada
- Cutscenes (mesmo seed):
  - chegada (widescreen 768x512, teste anterior)
  - briefing com mentora: mobile 768x1024 e desktop 1024x640
Paleta: hospital pastel blues/teals, light grey tiles, soft beige; blocky shading, crisp pixels.

### Estilos Gerados (samples)
- style1_clean (base Limezu, sem dithering)
- style2_dither (retro com dithering leve)
- style3_late16 (mais detalhe)
- style4_night (dramatico/noturno)
- style5_crt (retro/CRT)

### Novo arquivo
- prompts/estilos_pixel.md - consolida estilos e prompts de cenas/expressoes

### Atualizado
- CLAUDE.md - Novos passos no "passo a passo"
- iniciar_novo_terminal.txt - Inclui novos arquivos

### Novos passos do "passo a passo":
1. Ler todos os arquivos principais
2. Verificar git
3. Identificar melhorias
4. Fazer correcoes
5. **Atualizar resumo_contexto.md**
6. **Atualizar ramificacao.md**
7. Atualizar diario
8. Atualizar texto terminal
9. Commit e push
10. Gerar relatorio

### Discussao
Usuario ainda em duvida sobre melhor abordagem para criar assets.
Criados arquivos de contexto para ajudar a manter clareza entre sessoes.

---

## 2025-12-16 - Sessao 2: Reorganizacao e Foco

### Decisao de Design
Definido que este repositorio foca em:
- **Retratos Visual Novel** - Personagens em busto com expressoes para dialogos
- **Cutscenes Ilustradas** - Cenas completas para momentos importantes

Sprites top-down continuam sendo feitos no Usg-game/Gamefinal.

### Reorganizado
- CLAUDE.md atualizado com novo objetivo e estrutura
- Estrutura de pastas reorganizada:
  - assets/retratos/ (protagonista, mentores, equipe, pacientes, familiares)
  - assets/cutscenes/ (cap01-cap06)
- Prompts reorganizados:
  - retratos.md - Prompts para visual novel (15+ personagens)
  - expressoes.md - Guia de expressoes (72 imagens planejadas)
  - cutscenes.md - Mantido para cenas ilustradas

### Quantidades Planejadas
- 18 personagens com expressoes
- 72 imagens de retratos (3-6 expressoes por personagem)
- ~50 cutscenes ilustradas

### Proximos passos
- [ ] Gerar retratos do protagonista (6 expressoes)
- [ ] Gerar retratos da Dra. Costa (6 expressoes)
- [ ] Testar consistencia no Leonardo.ai
- [ ] Criar cutscenes do Capitulo 1

---

## 2025-12-16 - Sessao 1: Criacao do Repositorio

### Criado
- Estrutura inicial do repositorio Storytelling
- CLAUDE.md com instrucoes do projeto e comandos rapidos
- iniciar_novo_terminal.txt para continuidade
- Prompts para Leonardo.ai:
  - templates.md - Configuracoes base
  - ambientes.md - 11 cenarios de hospital
  - personagens.md - 15+ personagens
  - cutscenes.md - 20+ cenas narrativas
  - equipamentos.md - 30+ itens

### Roteiro
- historia_principal.md - 12 capitulos (3 atos)
- fluxo_jogo.md - Fluxo cenas + minigames
- arvore_ramificacoes.md - 27+ ramificacoes de escolhas

### Contexto
Parte do projeto USG-Game:
- Usg-game: Minigames de procedimentos (9 funcionais)
- Gamefinal: Hospital RPG com Gemini AI
- pixelmed-pro: Assets e design system

---
