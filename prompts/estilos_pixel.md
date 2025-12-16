# Estilos de Pixel Art (Storytelling)

## Modelos/Configuração
- Modelo: Lucid Origin (Leonardo) — usar seed fixo (ex: 424242)
- Guidance: 6-7
- Resolucao: retratos 768x1024; cutscenes mobile 768x1024; desktop 1024x640
- Negative (usar sempre): photorealistic, realistic skin, smooth lighting, smooth gradients, soft focus, depth of field, cinematic lighting, 3D render, watercolor, oil painting, glossy, bloom, text, watermark, logo, signature, modern UI

## Estilo 1 — Clean Limezu (padrão)
```
16-bit pixel art, clean Limezu hospital style, coarse pixel grid, visible pixels, 16-20 color palette, heavy outline, flat shading, no smooth gradients, muted highlights, blocky shading, hospital pastel blues and teals, light grey tiles, soft beige accents
```
Uso: padrão para diálogos e cenas claras.

### Retrato (exemplo)
```
[ESTILO 1], young anesthesiology resident in light blue scrubs, stethoscope, short dark hair, [expressão], bust shot, centered composition, generous headroom, UI-safe margins, transparent background
```
Expressoes: neutral (calm focused), gentle smile, worried expression, surprised expression.

### Cena de diálogo (2 personagens)
```
[ESTILO 1], two characters bust shot facing camera, left: young anesthesiology resident in light blue scrubs and stethoscope, right: mentor in green scrubs and cap, centered composition, generous headroom, UI-safe margins, empty space at bottom for dialogue box
```

### Procedimento raqui
```
[ESTILO 1], operating room, spinal anesthesia scene: patient seated on table, anesthesiologist preparing needle, assistant holding patient, monitors with ECG/SpO2, IV poles, surgical lights, centered composition, extra padding on sides for UI
```

## Estilo 2 — Retro Dither (flashback)
```
16-bit pixel art, SNES/PC-98 style, light dithering for shading, coarse pixel grid, visible pixels, 16-20 color palette, heavy outline, flat shading with dithering, muted highlights, hospital Limezu background
```
Uso: flashbacks/nostalgia.

### Retrato (exemplo)
```
[ESTILO 2], young anesthesiology resident in light blue scrubs, stethoscope, short dark hair, calm expression, bust shot, centered composition, UI-safe margins
```

## Estilo 3 — Late 16-bit Polido (cutscene importante)
```
16-bit pixel art, late SNES style, coarse pixel grid but higher detail, 20-28 color palette, controlled soft manual AA inside pixels, heavy outline, restrained highlights, hospital Limezu background, flat colors, no smooth gradients
```
Uso: cutscenes-chave.

### Briefing com mentora
```
[ESTILO 3], mentor in green scrubs and resident in blue scrubs at hospital meeting room whiteboard with ultrasound diagrams, centered composition, warm overhead light, padding on sides for UI
```

## Variações de iluminação/filtro
- Dramático noturno: adicionar `dramatic night lighting, high contrast, monitors glowing as key light` (usar pontualmente).
- CRT/Scanline: adicionar `subtle crt scanlines, slight vignette` (somente se quiser filtro nostálgico).

## Resoluções recomendadas
- Retratos: 768x1024 (escala inteira para mobile/desktop; usar `image-rendering: pixelated` no jogo).
- Cutscene mobile: 768x1024.
- Cutscene desktop: 1024x640.

## Paleta
- hospital pastel blues and teals
- light grey tiles
- soft beige accents
- Evitar: saturação alta, highlights especulares, gradientes suaves.
