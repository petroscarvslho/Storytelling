# Templates Base - Prompts Leonardo.ai

## Configuracoes Recomendadas

| Parametro | Valor |
|-----------|-------|
| **Modelo** | Lucid Origin ou Leonardo Diffusion XL |
| **Guidance Scale** | 6-8 |
| **Resolucao** | 768x512 (widescreen) ou 512x512 |
| **Seed fixo** | Usar o MESMO seed para consistencia |

---

## Estrutura Base do Prompt

```
[ESTILO], [CENA/AMBIENTE], [PERSONAGENS/ELEMENTOS], [ILUMINACAO], [DETALHES], [PALETA DE CORES]
```

---

## Negative Prompt Padrao (usar em TODAS as geracoes)

```
blurry, text, watermark, logo, signature, 3D render, photorealistic, high resolution, anti-aliasing, smooth gradients, realistic, photograph, modern UI, out of frame, cropped, deformed, ugly, mutilated
```

---

## Palavras-chave Obrigatorias

Sempre incluir no inicio do prompt:
- `16-bit pixel art`
- `SNES RPG style`
- `limited color palette`
- `visible pixels`

---

## Paleta de Cores do Projeto

| Elemento | Cor Hex | Uso |
|----------|---------|-----|
| Outline | #1e293b | Contornos |
| Floor | #f8fafc | Pisos claros |
| Wall | #cbd5e1 | Paredes neutras |
| Medical Blue | #93c5fd | Camas, equipamentos |
| Accent Red | #f87171 | Alertas, urgencia |
| ECG Green | #22c55e | Monitores |
| SpO2 Cyan | #06b6d4 | Oximetria |
| Wood | #e7d5c0 | Mobilia |

---

## Dicas de Consistencia

1. **Seed fixo** - Usar o MESMO seed para cenas do mesmo capitulo
2. **Character Reference** - Ativar no Leonardo.ai para personagens
3. **Gerar 4 variacoes** - Escolher a melhor como referencia
4. **Style Reference** - Usar uma cena aprovada como referencia de estilo

---

## Categorias de Prompts

Ver arquivos especificos:
- `ambientes.md` - Cenarios do hospital
- `personagens.md` - Sprites de personagens
- `cutscenes.md` - Cenas narrativas
- `equipamentos.md` - Itens e equipamentos
