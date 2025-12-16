# INSTRUCOES PARA CLAUDE CODE - Storytelling USG-Game

## LOCALIZACAO
- **Projeto**: /Users/priscoleao/Documents/Storytelling
- **GitHub**: https://github.com/petroscarvslho/Storytelling.git
- **Projetos relacionados**:
  - Usg-game: /Users/priscoleao/Usg-game
  - Gamefinal: /Users/priscoleao/Gamefinal
  - pixelmed-pro: /Users/priscoleao/pixelmed-pro

## OBJETIVO DO PROJETO
Criar cenas em pixel art para storytelling do jogo USG-Game. O jogo mistura RPG com educacao medica (procedimentos anestesicos e ultrassom).

## ESTRUTURA DO PROJETO
```
Storytelling/
├── CLAUDE.md                 <- Este arquivo
├── diario_progresso.md       <- Historico de desenvolvimento
├── prompts/
│   ├── templates.md          <- Templates base para Leonardo.ai
│   ├── ambientes.md          <- Prompts de cenarios
│   ├── personagens.md        <- Prompts de personagens
│   ├── cutscenes.md          <- Prompts de cenas narrativas
│   └── equipamentos.md       <- Prompts de itens/equipamentos
├── assets/
│   ├── ambientes/            <- Imagens geradas de cenarios
│   ├── personagens/          <- Sprites de personagens
│   ├── cutscenes/            <- Cenas de dialogo/narrativa
│   └── equipamentos/         <- Icones de itens
├── roteiro/
│   ├── historia_principal.md <- Narrativa principal
│   ├── dialogos/             <- Dialogos por cena
│   └── fluxo_jogo.md         <- Fluxo entre cenas e minigames
└── referencias/
    └── pesquisa_visual.md    <- Referencias visuais coletadas
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
1. Ler CLAUDE.md e diario_progresso.md
2. Verificar estado atual do git
3. Identificar o que precisa ser feito/melhorado
4. Fazer correcoes e melhorias necessarias
5. Atualizar diario_progresso.md
6. Atualizar iniciar_novo_terminal.txt
7. Fazer commit e push
8. Gerar relatorio do que foi feito

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
