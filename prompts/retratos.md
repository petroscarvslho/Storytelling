# Prompts de Retratos - Visual Novel

## CONFIGURACOES

- **Modelo**: Lucid Origin ou Leonardo Diffusion XL
- **Resolucao**: 512x512 ou 512x768 (vertical)
- **Guidance**: 7-8
- **Seed fixo**: Usar MESMO seed para todas expressoes do mesmo personagem

## NEGATIVE PROMPT PADRAO

```
blurry, text, watermark, logo, 3D render, photorealistic, full body, legs, feet, background scenery, multiple characters, deformed face, extra limbs
```

---

## ESTRUTURA DO PROMPT

```
16-bit pixel art portrait, [PERSONAGEM], [ROUPA], [EXPRESSAO], bust shot, facing viewer, simple gradient background, visual novel style, SNES RPG character portrait, clean lines, vibrant colors
```

---

## PROTAGONISTA - Dr. Residente

### Base
```
16-bit pixel art portrait, young male doctor in his late 20s, short dark hair, light blue medical scrubs, stethoscope around neck, hospital ID badge, bust shot, facing viewer, simple blue gradient background, visual novel style, SNES RPG character portrait
```

### Expressoes (mesmo seed, mudar apenas expressao)
| Expressao | Adicionar ao prompt |
|-----------|---------------------|
| Neutro | neutral calm expression |
| Feliz | happy smiling expression |
| Preocupado | worried concerned expression |
| Surpreso | surprised shocked expression |
| Determinado | determined confident expression |
| Cansado | tired exhausted expression |

---

## MENTORES

### Dra. Costa (Especialista em Bloqueios)
```
16-bit pixel art portrait, female doctor in her 40s, brown hair in ponytail, green surgical scrubs, kind patient expression, bust shot, facing viewer, simple green gradient background, visual novel style, SNES RPG mentor character
```

### Dr. Silva (Chefe da Anestesia)
```
16-bit pixel art portrait, senior male doctor in his 50s, short gray hair, dark blue scrubs, serious professional expression, bust shot, facing viewer, simple dark blue gradient background, visual novel style, SNES RPG authority figure
```

### Dr. Ferreira (Intensivista)
```
16-bit pixel art portrait, male doctor in his 40s, short beard, glasses, white coat over scrubs, thoughtful expression, bust shot, facing viewer, simple neutral gradient background, visual novel style, SNES RPG wise character
```

---

## COLEGAS

### Dr. Pedro (Residente Veterano)
```
16-bit pixel art portrait, male doctor in his early 30s, tall appearance, blue scrubs, competitive friendly expression, bust shot, facing viewer, simple blue gradient background, visual novel style, SNES RPG rival character
```

### Dra. Ana (Colega de Turma)
```
16-bit pixel art portrait, young female doctor in her late 20s, short hair, pink scrubs, friendly supportive expression, bust shot, facing viewer, simple pink gradient background, visual novel style, SNES RPG friend character
```

---

## EQUIPE

### Enf. Maria (Enfermeira Experiente)
```
16-bit pixel art portrait, female nurse in her 50s, graying hair, colorful scrubs, maternal caring expression, bust shot, facing viewer, simple warm gradient background, visual novel style, SNES RPG helper character
```

### Tec. Joao (Tecnico de Enfermagem)
```
16-bit pixel art portrait, young male nursing technician in his 20s, short hair, light green scrubs, helpful eager expression, bust shot, facing viewer, simple green gradient background, visual novel style, SNES RPG support character
```

---

## PACIENTES - TIPOS

### Paciente Calmo (Homem)
```
16-bit pixel art portrait, middle-aged male patient, hospital gown, calm slightly nervous expression, bust shot, facing viewer, simple light blue gradient background, visual novel style, SNES RPG NPC
```

### Paciente Ansioso (Mulher)
```
16-bit pixel art portrait, adult female patient in her 30s, hospital gown, worried anxious expression, bust shot, facing viewer, simple light gradient background, visual novel style, SNES RPG NPC
```

### Paciente Idoso
```
16-bit pixel art portrait, elderly male patient, white hair, hospital gown, wise gentle expression, bust shot, facing viewer, simple warm gradient background, visual novel style, SNES RPG NPC
```

### Paciente Crianca
```
16-bit pixel art portrait, young child patient around 8 years old, colorful hospital gown, curious innocent expression, holding stuffed toy, bust shot, facing viewer, simple cheerful gradient background, visual novel style
```

---

## FAMILIARES

### Familiar Preocupado (Homem)
```
16-bit pixel art portrait, adult man in casual clothes, holding flowers, worried expression, bust shot, facing viewer, simple neutral gradient background, visual novel style, SNES RPG NPC
```

### Familiar Preocupado (Mulher)
```
16-bit pixel art portrait, adult woman in casual clothes, purse, anxious teary expression, bust shot, facing viewer, simple neutral gradient background, visual novel style, SNES RPG NPC
```

---

## VARIACOES DE EXPRESSAO

Para cada personagem principal, gerar 6 expressoes:

1. **Neutro** - `neutral calm expression`
2. **Feliz** - `happy smiling expression`
3. **Triste/Preocupado** - `sad worried expression`
4. **Surpreso** - `surprised shocked expression`
5. **Bravo/Serio** - `angry serious expression`
6. **Pensativo** - `thoughtful pondering expression`

---

## DICAS DE CONSISTENCIA

1. **Seed fixo** por personagem (anotar o seed que funcionou)
2. **Character Reference** do Leonardo.ai para manter consistencia
3. **Mesma resolucao** para todos (512x512 ou 512x768)
4. **Mesmo fundo** por personagem (gradiente simples)
5. Gerar todas expressoes de um personagem antes de passar pro proximo
