# INSTRUCOES PARA CLAUDE CODE - Storytelling USG-Game

## LOCALIZACAO
- **Projeto**: /Users/priscoleao/Documents/Storytelling
- **GitHub**: https://github.com/petroscarvslho/Storytelling.git
- **Projetos relacionados**:
  - Usg-game: /Users/priscoleao/Usg-game
  - Gamefinal: /Users/priscoleao/Gamefinal
  - pixelmed-pro: /Users/priscoleao/pixelmed-pro

## OBJETIVO DO PROJETO
Criar assets visuais para storytelling do jogo USG-Game:
- **Retratos Visual Novel** - Personagens em busto com expressoes para dialogos
- **Cutscenes Ilustradas** - Cenas completas para momentos importantes

**NOTA**: Sprites top-down estao sendo feitos no Usg-game/Gamefinal.

## ESTILO DO JOGO
- Exploracao em top-down (Usg-game)
- Dialogos em visual novel (este repo)
- Cutscenes em momentos importantes (este repo)

## ESTRUTURA DO PROJETO
```
Storytelling/
├── CLAUDE.md                     <- Este arquivo
├── diario_progresso.md           <- Historico de desenvolvimento
├── iniciar_novo_terminal.txt     <- Instrucoes para novo terminal
├── resumo_contexto.md            <- Resumo de tudo (atualizado no passo a passo)
├── ramificacao.md                <- Esquema de ramificacoes (atualizado no passo a passo)
├── prompts/
│   ├── templates.md              <- Configuracoes Leonardo.ai
│   ├── retratos.md               <- Prompts de retratos (visual novel)
│   ├── cutscenes.md              <- Prompts de cenas ilustradas
│   ├── expressoes.md             <- Guia de expressoes por personagem
│   └── estilos_pixel.md          <- Estilos (clean/dither/late16) e exemplos
├── assets/
│   ├── retratos/                 <- Retratos para dialogos (usar para mobile/tablet/PC)
│   │   ├── protagonista/         <- Dr. Residente (expressoes)
│   │   ├── mentores/             <- Dr. Silva, Dra. Costa, etc.
│   │   ├── equipe/               <- Enfermeiros, tecnicos
│   │   └── pacientes/            <- Diversos tipos
│   └── cutscenes/                <- Cenas ilustradas completas
│       ├── cap01/                <- Por capitulo (mobile/tablet: 768x1024; PC: 1024x640)
│       ├── cap02/
│       └── ...
├── roteiro/
│   ├── historia_principal.md     <- Narrativa (12 capitulos)
│   ├── fluxo_jogo.md             <- Fluxo cenas + minigames
│   ├── arvore_ramificacoes.md    <- Escolhas e consequencias
│   └── dialogos/                 <- Textos por cena
└── referencias/
    └── pesquisa_visual.md        <- Referencias coletadas
```

## APIS DISPONIVEIS

### 1. Leonardo.ai (Principal para cenas)
- Usar para gerar cenas de storytelling
- Modelo recomendado: Lucid Origin ou Leonardo Diffusion XL
- Guidance Scale: 6-8
- Seed fixo para consistencia

### 2. PixelLab (MCP) - Ja integrado no Claude Code
- `mcp__pixellab__create_character` - Personagens com direcoes
- `mcp__pixellab__animate_character` - Animacoes
- `mcp__pixellab__create_isometric_tile` - Tiles isometricos
- `mcp__pixellab__create_topdown_tileset` - Tilesets top-down

## ESTILO VISUAL

### Paleta de Cores (consistente com Usg-game)
- Outline: #1e293b (azul-preto)
- Floor: #f8fafc (claro)
- Wall: #cbd5e1 (cinza neutro)
- Medical Blue: #93c5fd
- Accent Red: #f87171
- Monitor Green (ECG): #22c55e
- SpO2 Cyan: #06b6d4

### Estilo Pixel Art
- 16-bit SNES style
- Limited color palette
- Visible pixels
- Clean outlines

## FLUXO DE TRABALHO

1. **LER** - Ler arquivo antes de modificar
2. **CRIAR** - Gerar prompts ou assets
3. **DIARIO** - Atualizar diario_progresso.md
4. **GIT** - `git add -A && git commit -m "descricao" && git push origin main`

## COMANDOS RAPIDOS (funcionam em qualquer terminal)

| Comando             | O que faz                                                              |
|---------------------|------------------------------------------------------------------------|
| "passo a passo"     | Executa verificacao completa, correcoes, melhorias, commit e relatorio |
| "atualize o diario" | Atualiza diario_progresso.md                                           |
| "atualize o texto"  | Atualiza iniciar_novo_terminal.txt                                     |
| "faca commit"       | git add + commit + push                                                |
| "antes de fechar"   | Diario + texto + commit                                                |

### O que "passo a passo" faz:
1. Ler CLAUDE.md, diario_progresso.md, resumo_contexto.md, ramificacao.md
2. Verificar estado atual do git
3. Identificar o que precisa ser feito/melhorado
4. Fazer correcoes e melhorias necessarias
5. **Atualizar resumo_contexto.md** com tudo que foi conversado/aprendido
6. **Atualizar ramificacao.md** com evolucao do esquema de ramificacoes
7. Atualizar diario_progresso.md
8. Atualizar iniciar_novo_terminal.txt
9. Fazer commit e push
10. Gerar relatorio do que foi feito

## REGRA OBRIGATORIA AO FECHAR CHAT

ANTES DE FECHAR QUALQUER SESSAO, SEMPRE:
1. Atualizar diario_progresso.md com o que foi feito
2. Atualizar iniciar_novo_terminal.txt com estado atual
3. Fazer commit e push
4. Confirmar que nao ha mudancas pendentes

## CONTEXTO DO JOGO

### Tema
RPG hospitalar educacional focado em anestesiologia e POCUS (Point-of-Care Ultrasound)

### Protagonista
Dr. Residente - medico anestesista em treinamento

### Mecanica
- Exploracao do hospital (overworld)
- Dialogos com NPCs (pacientes, equipe)
- "Batalhas" = Procedimentos medicos (minigames)
- Progressao: casos mais complexos

### Minigames existentes (9 funcionais)
1. Bloqueio Supraclavicular
2. Bloqueio Interescalenico
3. TAP Block
4. Epidural
5. Raquianestesia
6. Acesso Venoso Central
7. FAST/eFAST (trauma)
8. FoCUS (cardiaco)
9. Lung USG (BLUE Protocol)

## COMANDOS UTEIS

```bash
# Navegar para o projeto
cd /Users/priscoleao/Documents/Storytelling

# Ver estado do git
git status
git log --oneline -10

# Commit rapido
git add -A && git commit -m "msg" && git push origin main
```
