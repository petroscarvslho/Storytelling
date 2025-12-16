# Resumo de Contexto - Storytelling USG-Game

> Este arquivo e atualizado automaticamente no comando "passo a passo"

---

## O PROJETO COMPLETO

### USG-Game - Visao Geral
Um jogo educacional que mistura **RPG hospitalar** com **storytelling** para ensinar procedimentos anestesicos e ultrassom (POCUS). O jogador e um medico residente aprendendo tecnicas atraves de casos clinicos.

### 3 Repositorios do Projeto

| Repositorio | Funcao | Status |
|-------------|--------|--------|
| **Usg-game** | Minigames de procedimentos (9 funcionais) | Em desenvolvimento |
| **Gamefinal** | Hospital RPG, mapa, Gemini AI | Em desenvolvimento |
| **Storytelling** | Retratos visual novel + cutscenes | Estrutura pronta |

---

## COMO O JOGO FUNCIONA

### Fluxo de Gameplay
```
EXPLORACAO (top-down no hospital)
        ↓
DIALOGOS (visual novel com retratos)
        ↓
CUTSCENES (momentos importantes)
        ↓
MINIGAMES (procedimentos medicos)
        ↓
RESULTADOS (ramificacoes baseadas em escolhas)
```

### Estilo Visual
- **Exploracao**: Pixel art top-down (Usg-game/Gamefinal)
- **Dialogos**: Retratos em busto com expressoes (este repo)
- **Cutscenes**: Cenas ilustradas completas (este repo)
- **Minigames**: Interface USG realista (Usg-game)

---

## O QUE JA EXISTE

### Usg-game (9 Minigames)
1. Bloqueio Supraclavicular
2. Bloqueio Interescalenico
3. TAP Block
4. Epidural
5. Raquianestesia
6. Acesso Venoso Central
7. FAST/eFAST (trauma)
8. FoCUS (cardiaco)
9. Lung USG (BLUE Protocol)

### Gamefinal
- Mapa do hospital (80x60 tiles)
- 15 salas cirurgicas
- Sistema de dialogos
- Integracao Gemini AI
- Assets LimeZu (Modern Interiors)

### Storytelling (este repo)
- Roteiro: 12 capitulos em 3 atos
- Arvore de ramificacoes: 27+ escolhas
- Prompts para Leonardo.ai prontos
- Estrutura de pastas organizada

---

## O QUE FALTA DECIDIR

### Duvidas do Usuario (2025-12-16)
1. **Como organizar a criacao dos assets?**
   - Sao muitos personagens e cenas
   - Precisa de consistencia visual

2. **Qual a melhor abordagem para gerar?**
   - Gerar tudo de uma vez?
   - Gerar por capitulo?
   - Gerar por tipo (todos retratos, depois cutscenes)?

3. **Como garantir consistencia?**
   - Mesmo estilo em todos os assets
   - Personagens reconheciveis

---

## QUANTIDADES PLANEJADAS

| Tipo | Quantidade |
|------|------------|
| Personagens com retratos | 18 |
| Expressoes por personagem | 3-6 |
| Total de retratos | ~72 imagens |
| Cutscenes ilustradas | ~50 cenas |
| Capitulos | 12 |
| Ramificacoes | 27+ |

---

## PERSONAGENS PRINCIPAIS

### Protagonista
- **Dr. Residente** - Jovem medico em treinamento

### Mentores
- **Dr. Silva** - Chefe da anestesia, serio
- **Dra. Costa** - Especialista em bloqueios, paciente
- **Dr. Ferreira** - Intensivista, sabio

### Colegas
- **Dr. Pedro** - Residente veterano, competitivo
- **Dra. Ana** - Colega de turma, apoio

### Equipe
- **Enf. Maria** - Enfermeira experiente
- **Tec. Joao** - Tecnico prestativo

---

## TECNOLOGIAS

| Ferramenta | Uso |
|------------|-----|
| Leonardo.ai | Gerar retratos e cutscenes |
| PixelLab MCP | Sprites e animacoes (top-down) |
| Claude Code | Organizacao e documentacao |
| GitHub | Versionamento |

---

## DECISOES TOMADAS

1. ✅ Separar sprites top-down (Usg-game) de retratos/cutscenes (Storytelling)
2. ✅ Usar visual novel para dialogos
3. ✅ Cutscenes em momentos importantes
4. ✅ 12 capitulos divididos em 3 atos
5. ✅ Sistema de ramificacoes com consequencias

---

## PROXIMAS DECISOES PENDENTES

- [ ] Definir ordem de criacao dos assets
- [ ] Definir workflow de geracao no Leonardo.ai
- [ ] Testar consistencia visual com 1 personagem primeiro
- [ ] Decidir nivel de detalhe das cutscenes

---

*Ultima atualizacao: 2025-12-16*
