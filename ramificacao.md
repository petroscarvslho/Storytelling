# Ramificacao - Esquema de Criacao

> Este arquivo e atualizado automaticamente no comando "passo a passo"

---

## CONCEITO GERAL

O jogo tem **escolhas que afetam a historia**. Cada escolha leva a consequencias diferentes, criando ramificacoes na narrativa.

---

## COMO FUNCIONA

```
[SITUACAO]
     |
     ├── Escolha A → Consequencia A → Afeta futuro
     ├── Escolha B → Consequencia B → Afeta futuro
     └── Escolha C → Consequencia C → Afeta futuro
```

### Tipos de Consequencias
1. **Imediata** - Dialogo muda na hora
2. **Futura** - Afeta cenas posteriores
3. **Relacionamento** - Muda como NPCs tratam jogador
4. **Gameplay** - Desbloqueia ou bloqueia opcoes

---

## VARIAVEIS DO SISTEMA

```javascript
gameState = {
  // Relacionamentos (-100 a +100)
  relacionamentos: {
    drSilva: 0,
    draCosta: 0,
    drPedro: 0,
    enfMaria: 0
  },

  // Atributos do jogador
  reputacao: {
    tecnica: 0,      // Habilidade em procedimentos
    empatia: 0,      // Relacao com pacientes
    lideranca: 0,    // Tomada de decisao
  },

  // Historico de escolhas
  escolhas: {
    // cap1_cena2_escolha: "opcaoA"
  }
}
```

---

## ESTRUTURA POR CAPITULO

### Capitulo 1: Primeiro Dia
| Cena | Escolha | Opcoes | Consequencia |
|------|---------|--------|--------------|
| Recepcao | Pedir ajuda? | Sim/Nao/Perguntar por alguem | Relacionamento com staff |
| Encontro chefe | Motivacao | Tecnica/Pacientes/Descobrindo | Tom dos dialogos futuros |

### Capitulo 3: Primeiro Bloqueio
| Cena | Escolha | Opcoes | Consequencia |
|------|---------|--------|--------------|
| Conversa paciente | Como explicar | Honesto/Tranquilizador/Tecnico | Cooperacao do paciente |
| Resultado | Sucesso/Falha | - | Ramifica para aprendizado ou celebracao |

### Capitulo 4-6: Desenvolvimento
- Escolhas afetam dificuldade
- Escolhas afetam ajuda disponivel
- Escolhas acumulam para finais

---

## FINAIS POSSIVEIS

| Final | Requisitos | Cena |
|-------|------------|------|
| Excelencia | tecnica>80, empatia>60, sem erros graves | Formatura com honras |
| Competente | tecnica>50, maioria ok | Formatura normal |
| Crescimento | Muitas falhas mas persistiu | Discurso sobre aprender |
| Relacional | empatia>80, relacionamentos altos | Reconhecido pela equipe |

---

## PASSOS PARA CRIAR RAMIFICACOES

### Passo 1: Identificar Momentos de Escolha
- Dialogos importantes
- Antes de procedimentos
- Apos resultados (sucesso/falha)
- Interacoes com NPCs

### Passo 2: Definir Opcoes
- Sempre 2-4 opcoes
- Uma opcao "neutra"
- Opcoes devem ser distintas

### Passo 3: Mapear Consequencias
- O que muda imediatamente?
- O que muda no futuro?
- Qual variavel e afetada?

### Passo 4: Criar Assets Necessarios
- Dialogos diferentes por opcao
- Expressoes diferentes dos personagens
- Cenas alternativas se necessario

---

## EXEMPLO DETALHADO

### Cena 3.3 - Conversa com Paciente

**Contexto**: Antes do primeiro bloqueio, paciente pergunta "Vai doer?"

**Opcao A - Honesto**:
```
Dialogo: "Voce vai sentir uma picada inicial, depois alivia."
→ Paciente relaxa (confia na honestidade)
→ +10 empatia
→ Procedimento: paciente cooperativo
→ Dra. Costa comenta: "Boa comunicacao"
```

**Opcao B - Tranquilizador**:
```
Dialogo: "Nao se preocupe, vai ficar tudo bem."
→ Paciente ainda nervoso (resposta vaga)
→ +0 (neutro)
→ Procedimento: normal
```

**Opcao C - Tecnico**:
```
Dialogo: "Vou aplicar anestesia local antes do bloqueio."
→ Paciente aliviado (explicacao pratica)
→ +5 tecnica
→ Procedimento: paciente cooperativo
→ Dra. Costa comenta: "Explicacao clara"
```

---

## STATUS ATUAL

### Ramificacoes Mapeadas
- [x] Capitulo 1 - 2 cenas com escolha (6 ramificacoes)
- [x] Capitulo 3 - 2 cenas com escolha (9 ramificacoes)
- [x] Capitulo 4 - 2 cenas com escolha (6 ramificacoes)
- [x] Capitulo 6 - 2 cenas com escolha (6 ramificacoes)
- [ ] Capitulos 5, 7-11 - Pendente mapear

### Total Atual
- **8 cenas** com escolhas definidas
- **27 ramificacoes** mapeadas
- **4 finais** possiveis
- Observacao (2025-12-16): foco atual em definir estilo visual (samples gerados em assets/samples); mapa de ramificacoes permanece o mesmo.

---

## PROXIMOS PASSOS

1. [ ] Mapear escolhas dos capitulos 5, 7-11
2. [ ] Definir dialogos exatos para cada opcao
3. [ ] Identificar assets visuais necessarios por ramificacao
4. [ ] Implementar sistema de variaveis no jogo

---

## PERGUNTAS EM ABERTO

1. Quantas ramificacoes sao gerenciaveis?
2. Cada ramificacao precisa de cutscene propria?
3. Como mostrar visualmente as consequencias?
4. Vale ter finais "ruins" ou so variacoes de sucesso?

---

*Ultima atualizacao: 2025-12-16*
