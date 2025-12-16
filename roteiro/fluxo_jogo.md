# Fluxo do Jogo - Cenas e Minigames

## ESTRUTURA DE CADA CAPITULO

```
[CUTSCENE ABERTURA]
       |
       v
[EXPLORACAO HOSPITAL] (opcional)
       |
       v
[DIALOGO COM NPC]
       |
       v
[BRIEFING DO CASO]
       |
       v
[MINIGAME/PROCEDIMENTO]
       |
       v
[CUTSCENE RESULTADO]
       |
       v
[DIALOGO DE ENCERRAMENTO]
       |
       v
[PROXIMO CAPITULO]
```

---

## CAPITULO 1: PRIMEIRO DIA

```
CENA 1.1 - Abertura
├── Tipo: Cutscene cinematica
├── Prompt: "primeiro dia no hospital, chegada, sol nascendo"
├── Duracao: 5 segundos
└── Transicao: Fade para interior

CENA 1.2 - Recepcao
├── Tipo: Ambiente exploravel
├── Prompt: "recepcao do hospital"
├── Interacoes: Recepcionista (dialogo)
└── Objetivo: Receber crachas e instrucoes

CENA 1.3 - Encontro com Chefe
├── Tipo: Dialogo
├── Personagens: Dr. Silva (chefe)
├── Conteudo: Boas-vindas, expectativas
└── Transicao: Caminho para vestiario

CENA 1.4 - Vestiario
├── Tipo: Ambiente
├── Prompt: "vestiario medico"
├── Acao: Trocar roupa (animacao simples)
└── Item: Recebe estetoscopio

[SEM MINIGAME - Capitulo introdutorio]

CENA 1.5 - Encerramento
├── Tipo: Cutscene
├── Prompt: "corredor hospital, fim do primeiro dia"
└── Transicao: Fade para capitulo 2
```

---

## CAPITULO 2: O MENTOR

```
CENA 2.1 - Sala de Ultrassom
├── Tipo: Ambiente
├── Prompt: "sala de ultrassom"
└── Personagem: Dra. Costa esperando

CENA 2.2 - Dialogo Tutorial
├── Tipo: Dialogo
├── Personagem: Dra. Costa
├── Conteudo: Explicacao basica de ultrassom
└── Ilustracoes: Imagens didaticas (probe, tela)

CENA 2.3 - Briefing
├── Tipo: Dialogo com imagens
├── Conteudo: Como posicionar probe
└── Transicao: Para minigame tutorial

[MINIGAME: Tutorial de Ultrassom]
├── Modo: Sandbox (sem penalidades)
├── Objetivo: Familiarizacao com controles
└── Feedback: Dra. Costa guiando

CENA 2.4 - Resultado
├── Tipo: Dialogo
├── Conteudo: Parabens, proximo passo
└── Desbloqueio: Badge "Primeiro Contato"
```

---

## CAPITULO 3: PRIMEIRO BLOQUEIO

```
CENA 3.1 - Centro Cirurgico
├── Tipo: Ambiente
├── Prompt: "corredor centro cirurgico"
└── Atmosfera: Movimento, preparacao

CENA 3.2 - Briefing do Caso
├── Tipo: Dialogo com ficha
├── Personagem: Dra. Costa
├── Caso: Paciente para cirurgia de mao
├── Info: Maria Santos, 35a, ASA I
└── Procedimento: Bloqueio supraclavicular

CENA 3.3 - Conversa com Paciente
├── Tipo: Dialogo
├── Personagem: Paciente Maria
├── Conteudo: Explicar procedimento, consentimento
└── Atmosfera: Calma, tranquilizadora

CENA 3.4 - Preparacao
├── Tipo: Cutscene curta
├── Prompt: "preparacao bloqueio, posicionamento"
└── Transicao: Para minigame

[MINIGAME: Supraclavicular]
├── Modo: Tutorial (guias visuais ativos)
├── Supervisao: Dra. Costa ao lado
└── Dificuldade: Facil

CENA 3.5 - Sucesso
├── Tipo: Cutscene
├── Prompt: "sucesso procedimento, paciente aliviado"
├── Desbloqueio: Badge "Primeiro Bloqueio"
└── XP: +100
```

---

## CAPITULO 4: URGENCIA NA MADRUGADA

```
CENA 4.1 - Quarto Escuro
├── Tipo: Cutscene
├── Prompt: "quarto hospital noite, celular tocando"
└── Atmosfera: Urgencia, despertar subito

CENA 4.2 - Corredor Noturno
├── Tipo: Ambiente
├── Prompt: "corredor hospital noite, luzes baixas"
└── Musica: Tensa, urgente

CENA 4.3 - Briefing Rapido
├── Tipo: Dialogo
├── Personagem: Enf. Maria
├── Caso: Paciente septico, precisa de acesso central
└── Tempo: Limitado (timer comeca)

[MINIGAME: Acesso Venoso Central]
├── Modo: Normal
├── Timer: Ativo (pressao de tempo)
└── Dificuldade: Media

CENA 4.4 - Resultado
├── Se sucesso: Paciente estabiliza, alívio
├── Se falha: Complicacao, mas salvo por backup
└── Reflexao: Dialogo sobre pressao e calma
```

---

## FLUXO RESUMIDO - TODOS OS CAPITULOS

| Cap | Titulo | Ambiente Principal | Minigame | Dificuldade |
|-----|--------|-------------------|----------|-------------|
| 1 | Primeiro Dia | Recepcao | Nenhum | - |
| 2 | O Mentor | Sala USG | Tutorial | Facil |
| 3 | Primeiro Bloqueio | Centro Cirurgico | Supraclavicular | Facil |
| 4 | Urgencia Madrugada | Corredor Noite | Acesso Venoso | Medio |
| 5 | Paciente Dificil | Enfermaria | TAP Block | Medio |
| 6 | Trauma | Emergencia | FAST | Medio |
| 7 | Coracao em Foco | UTI | FoCUS | Dificil |
| 8 | Falta de Ar | Enfermaria | Lung USG | Dificil |
| 9 | A Gestante | Obstetricia | Raqui + Epidural | Dificil |
| 10 | Caso Impossivel | Centro Cirurgico | Interescalenico | Expert |
| 11 | Prova Final | Sala Avaliacao | Multiplos | Expert |
| 12 | Formatura | Auditorio | Nenhum | - |

---

## CONTAGEM DE ASSETS NECESSARIOS

### Por Capitulo (media)
- 4-5 cenas de cutscene/dialogo
- 1-2 ambientes
- 2-3 expressoes de personagem
- 1-2 itens novos

### Total do Jogo
- **Cutscenes**: ~50 cenas
- **Ambientes**: ~15 diferentes
- **Personagens**: 10 principais + variacoes
- **Equipamentos**: 30+ icones
- **Badges**: 25+ conquistas

---

## NOTAS DE IMPLEMENTACAO

1. **Cenas de dialogo**: Usar sistema de dialogo do Gamefinal
2. **Transicoes**: Fade in/out entre cenas
3. **Timer**: Alguns capitulos tem pressao de tempo
4. **Branching**: Resultados afetam dialogos seguintes
5. **Save**: Salvar apos cada capitulo completo
