# Arvore de Ramificacoes Narrativas

## CONCEITO

O jogo tem escolhas que afetam:
1. **Dialogos** - O que personagens falam depois
2. **Resultados** - Sucesso/falha dos procedimentos
3. **Relacionamentos** - Como NPCs tratam o jogador
4. **Desbloqueios** - Badges, equipamentos, casos

---

## ESTRUTURA DE DECISAO

```
[SITUACAO]
    |
    ├── Escolha A → Consequencia A
    │       |
    │       └── Ramificacao A1, A2...
    |
    ├── Escolha B → Consequencia B
    │       |
    │       └── Ramificacao B1, B2...
    |
    └── Escolha C → Consequencia C
            |
            └── Ramificacao C1, C2...
```

---

## CAPITULO 1: PRIMEIRO DIA

### Cena 1.2 - Recepcao
```
[Recepcionista pergunta se precisa de ajuda]
    |
    ├── "Sim, estou perdido"
    │       → Recepcionista guia ate o vestiario
    │       → +Relacao com staff
    │       → Dialogo amigavel depois
    |
    ├── "Nao, obrigado"
    │       → Encontra caminho sozinho
    │       → Neutro
    |
    └── "Onde fica o Dr. Silva?"
            → Recepcionista indica direcao
            → Conhece Dr. Silva primeiro
            → Dialogo diferente no encontro
```

### Cena 1.3 - Encontro com Chefe
```
[Dr. Silva pergunta: "Por que escolheu anestesia?"]
    |
    ├── "Gosto de procedimentos tecnicos"
    │       → Dr. Silva aprova
    │       → +Respeito do mentor
    │       → Dicas extras em procedimentos
    |
    ├── "Quero ajudar pacientes sem dor"
    │       → Dr. Silva sorri
    │       → +Empatia
    │       → Dialogos sobre humanizacao
    |
    └── "Ainda estou descobrindo"
            → Dr. Silva entende
            → Neutro
            → Historia de descoberta
```

---

## CAPITULO 3: PRIMEIRO BLOQUEIO

### Cena 3.3 - Conversa com Paciente
```
[Paciente pergunta: "Vai doer?"]
    |
    ├── "Voce vai sentir uma picada inicial, depois alivia"
    │       → Paciente relaxa (honestidade)
    │       → +Confianca
    │       → Procedimento mais facil
    |
    ├── "Nao se preocupe, vai ficar tudo bem"
    │       → Paciente ainda nervoso
    │       → Neutro
    │       → Procedimento normal
    |
    └── "Vou aplicar anestesia local antes"
            → Paciente aliviado (tecnico)
            → +Profissionalismo
            → Paciente cooperativo
```

### Minigame - Resultado
```
[SUPRACLAVICULAR - Resultado]
    |
    ├── SUCESSO (3 estrelas)
    │       → Dra. Costa: "Excelente tecnica!"
    │       → +100 XP
    │       → Badge "Primeiro Bloqueio Perfeito"
    │       → Proximo caso mais complexo
    |
    ├── SUCESSO (1-2 estrelas)
    │       → Dra. Costa: "Bom trabalho, pratique mais"
    │       → +50 XP
    │       → Caso similar para pratica
    |
    └── FALHA (complicacao)
            → Dra. Costa assume
            → Cena de aprendizado
            → -30 XP
            → Tutorial extra obrigatorio
            → Dialogo de apoio da equipe
```

---

## CAPITULO 4: URGENCIA NA MADRUGADA

### Cena 4.3 - Briefing Rapido
```
[Enf. Maria: "Precisa de acesso central, rapido!"]
    |
    ├── "Estou pronto, vamos la"
    │       → Timer normal
    │       → Confianca demonstrada
    |
    ├── "Preciso de mais informacoes"
    │       → +30 segundos no timer
    │       → Info extra sobre paciente
    │       → Mais preparado
    |
    └── "Chame o supervisor"
            → Dr. Senior aparece
            → Supervisao durante procedimento
            → -Autonomia mas +Seguranca
            → Menos XP no final
```

### Minigame - Complicacao
```
[ACESSO VENOSO - Puncao Arterial]
    |
    ├── IDENTIFICAR RAPIDO
    │       → "Sangue pulsatil - arteria!"
    │       → Remover agulha
    │       → Compressao
    │       → Tentar novamente
    │       → -10 XP mas sem dano
    |
    └── NAO IDENTIFICAR
            → Hematoma forma
            → Complicacao
            → -50 XP
            → Cena de resolucao
            → Aprendizado forcado
```

---

## CAPITULO 6: TRAUMA

### Cena 6.2 - Triagem
```
[Multiplas vitimas chegando]
    |
    ├── Atender Crianca primeiro
    │       → Emocional mas correto?
    │       → Pode atrasar adulto grave
    │       → Ramificacao etica
    |
    ├── Atender Adulto grave primeiro
    │       → Protocolo correto
    │       → Crianca espera
    │       → Enfermeira cuida
    |
    └── Pedir ajuda para dividir
            → Chama colega
            → Trabalho em equipe
            → +Relacao com Dr. Pedro
```

### FAST - Resultado
```
[FAST POSITIVO encontrado]
    |
    ├── RELATAR IMEDIATAMENTE
    │       → Cirurgia de emergencia
    │       → Salva paciente
    │       → +100 XP
    │       → Badge "Trauma Ready"
    |
    ├── PEDIR CONFIRMACAO
    │       → Atraso de 2 minutos
    │       → Paciente estavel ainda
    │       → +50 XP (cauteloso)
    |
    └── NAO IDENTIFICAR (erro)
            → Piora do paciente
            → Colega identifica
            → Cena de aprendizado
            → -50 XP
```

---

## SISTEMA DE CONSEQUENCIAS

### Variaveis Trackeadas

```javascript
// Exemplo de variaveis
gameState = {
  relacionamentos: {
    drSilva: 0,      // -100 a +100
    draCosta: 0,
    drPedro: 0,
    enfMaria: 0,
    pacientes: 0
  },
  reputacao: {
    tecnica: 0,      // Habilidade em procedimentos
    empatia: 0,      // Relacao com pacientes
    lideranca: 0,    // Tomada de decisao
    trabalhoEquipe: 0
  },
  escolhas: {
    cap1_recepcao: null,
    cap1_motivacao: null,
    cap3_paciente: null,
    // ... todas as escolhas
  },
  consequencias: {
    tutorialExtra: false,
    supervisaoObrigatoria: false,
    casoEspecialDesbloqueado: false
  }
}
```

### Como Afeta o Jogo

| Variavel | Efeito no Jogo |
|----------|----------------|
| draCosta > 50 | Dicas extras em bloqueios |
| drSilva > 50 | Casos mais complexos liberados |
| empatia > 30 | Pacientes mais cooperativos |
| tecnica > 50 | Menos erros aleatorios |
| trabalhoEquipe > 30 | Ajuda disponivel em emergencias |

---

## FINAIS POSSIVEIS

### Final A - Excelencia
```
Requisitos:
- tecnica > 80
- empatia > 60
- Todos os badges de maestria
- Zero complicacoes graves

Cena: Formatura com honras, convite para fellowship
```

### Final B - Competente
```
Requisitos:
- tecnica > 50
- Maioria dos procedimentos ok
- Algumas complicacoes resolvidas

Cena: Formatura normal, aprovado no programa
```

### Final C - Crescimento
```
Requisitos:
- Muitas falhas mas persistencia
- Aprendizado demonstrado
- Melhora ao longo do jogo

Cena: Formatura com discurso sobre aprender com erros
```

### Final D - Especialista em Relacoes
```
Requisitos:
- empatia > 80
- trabalhoEquipe > 70
- Todos os relacionamentos positivos

Cena: Reconhecido pela equipe e pacientes
```

---

## COMO ADICIONAR NOVAS RAMIFICACOES

### Template

```
## CAPITULO X: [NOME]

### Cena X.Y - [Descricao]
```
[SITUACAO/PERGUNTA]
    |
    ├── "[Escolha 1]"
    │       → [Consequencia imediata]
    │       → [Efeito em variavel]
    │       → [Ramificacao futura]
    |
    ├── "[Escolha 2]"
    │       → [Consequencia imediata]
    │       → [Efeito em variavel]
    │       → [Ramificacao futura]
    |
    └── "[Escolha 3]"
            → [Consequencia imediata]
            → [Efeito em variavel]
            → [Ramificacao futura]
```

---

## CONTAGEM ATUAL

| Capitulo | Cenas com Escolha | Total Ramificacoes |
|----------|------------------|-------------------|
| 1 | 2 | 6 |
| 3 | 2 | 9 |
| 4 | 2 | 6 |
| 6 | 2 | 6 |
| **Total** | **8** | **27** |

*Expandir conforme necessario*

---

## NOTAS

- Cada escolha deve ter 2-4 opcoes
- Sempre ter uma opcao "neutra"
- Consequencias podem ser imediatas ou futuras
- Algumas escolhas afetam multiplos capitulos
- Finais sao combinacao de todas as escolhas
