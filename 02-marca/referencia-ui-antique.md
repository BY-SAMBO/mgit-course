# Florécer — Referencia de Diseño UI
## Línea Antique · Jardín de Emociones

> Documento condensado para desarrollo de interfaces con estética paralela al manual de marca.
> Fuente: `manual-antique.html` (512KB → este documento ~15KB)

---

## 1. Concepto Central

Florécer no es una floristerÃ­a. Es una experiencia de bienestar sensorial que une flores, infusiones botánicas y emociones.

**Principio rector:** La marca controla su entorno para comunicar. No se adapta — lo transforma. Cada color de fondo es una decisión de marca.

**Frase de lÃ­nea:** *"Cada flor lleva un sentir."*
**Variantes:** *"Botánica del alma."* · *"Flores que hablan lo que sientes."* · *"Un herbario de emociones."*

**Personalidad:** Como una amiga sofisticada y cálida que siempre sabe hacer que un momento ordinario se sienta especial. Elegante sin ser frÃ­a, natural sin ser rústica, emocional sin ser frágil.

**Arquetipos:** El Amante (primario) · El Cuidador (secundario) · El Mago (terciario)

---

## 2. Tokens de Diseño

### 2.1 Paleta Emocional (8 colores)

```css
:root {
  /* — Emociones — */
  --ternura:     #C4897B;  /* Amor propio, Suavidad     · Rosa de jardÃ­n    */
  --calma:       #C9A36A;  /* Serenidad, Introspección  · Manzanilla        */
  --arraigo:     #5B6B4A;  /* Estabilidad, Presencia    · Romero            */
  --melancolia:  #7A8B9A;  /* Nostalgia, Quietud        · Lavanda           */
  --fuerza:      #B5654A;  /* Determinación, Coraje     · Jengibre en flor  */
  --paz:         #F0E6D4;  /* Silencio, Descanso        · JazmÃ­n            */
  --misterio:    #5C3A4E;  /* Intuición, Lo sagrado     · Damiana           */
  --alegria:     #D4A853;  /* Gratitud, Plenitud        · Caléndula         */

  /* — Neutros (grises cálidos) — */
  --white:       #FFFFFF;
  --gray-50:     #F2EDE5;
  --gray-100:    #EDE6DC;
  --gray-200:    #DDD5C8;
  --gray-400:    #B0A598;
  --gray-500:    #8A7E72;
  --gray-700:    #5A4E42;
  --gray-900:    #3A2E24;
}
```

### 2.2 Fondos Suaves para UI (versiones tint de cada emoción)

Usados en posts de IG y aplicables como fondos de cards/secciones:

```css
:root {
  --bg-ternura:    #F9F0ED;
  --bg-calma:      #F7F1E8;
  --bg-arraigo:    #EDE8DF;
  --bg-melancolia: #E8E4E0;
  --bg-fuerza:     #F2EAE4;
  --bg-paz:        #F5F0E8;
  --bg-misterio:   #E8E0E5;
  --bg-alegria:    #F5EDE0;
}
```

### 2.3 Gradientes de Sobre (dirección emocional)

```css
--grad-alegria:  linear-gradient(160deg, #E8C060 0%, #D4A853 45%, #A8793A 100%);
--grad-ternura:  linear-gradient(150deg, #D9A090 0%, #C4897B 50%, #9E6A5F 100%);
--grad-calma:    linear-gradient(155deg, #D8B880 0%, #C9A36A 50%, #A07E40 100%);
--grad-misterio: linear-gradient(145deg, #7A4A65 0%, #5C3A4E 50%, #3A2232 100%);
```

### 2.4 Combinaciones por Momento

| Momento        | Uso                      | Colores                          |
|----------------|--------------------------|----------------------------------|
| Despertar      | Mañanas, energÃ­a         | Paz + AlegrÃ­a + Arraigo          |
| Introspección  | Atardecer, journaling    | MelancolÃ­a + Misterio + Calma   |
| Descanso       | Noche, sueño             | MelancolÃ­a + Paz + Ternura      |
| Celebración    | Logros, gratitud         | Fuerza + AlegrÃ­a + Calma        |
| Sanación       | Autocuidado, duelo suave | Ternura + Arraigo + Paz          |

**Regla:** Máximo 2-3 colores emocionales por pieza/vista.

---

## 3. TipografÃ­a

### 3.1 Fuentes

```css
--font-sans:   'Inter', -apple-system, sans-serif;
--font-serif:  'EB Garamond', serif;
--font-detail: 'Cormorant', serif;
```

**Google Fonts import:**
```
EB Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500
Inter:wght@300;400;500
Cormorant:ital,wght@0,300;0,400;0,700;1,300;1,400
```

### 3.2 Tres Voces

| Voz | Fuente | Rol |
|-----|--------|-----|
| **Funcional** (interfaz) | Inter Light 300 | Body, navegación, labels, info técnica |
| **Emocional** | EB Garamond Italic | Nombres de emoción, frases de marca, tÃ­tulos de sección |
| **Botánica** | Cormorant Light Italic | Anotaciones de placa, ingredientes, notas de herbario |

### 3.3 Escala TipográfÃ­ca

| Elemento | Fuente | Peso | Tamaño | Extras |
|----------|--------|------|--------|--------|
| Logotipo | Cormorant | 700 Bold | 3.5rem | uppercase, tracking 0.08em |
| Nombre de emoción | EB Garamond | Italic | 2.2–2.8rem | — |
| TÃ­tulo de sección (h2 inner) | EB Garamond | Regular 400 | 2.2rem | line-height 1.2 |
| Etiqueta de sección (h2 outer) | Inter | Regular 400 | 0.75rem | uppercase, tracking 0.25em, gray-500 |
| Subtítulo (h3) | Inter | Medium 500 | 0.7rem | uppercase, tracking 0.15em, gray-700 |
| Cuerpo (p) | Inter | Light 300 | 1rem | line-height 1.8, max-width 640px, gray-700 |
| Lead / intro | EB Garamond | Italic | 1.3rem | line-height 1.6, gray-700 |
| Blockquote | EB Garamond | Italic | 1.5rem | line-height 1.5, max-width 540px, gray-900 |
| Lista (li) | Inter | Light 300 | 0.95rem | gray-700 |
| Anotación botánica | Cormorant | Light 300 Italic | 0.8–1.1rem | gray-500 |
| Nav links | Inter | Regular 400 | 0.62rem | uppercase, tracking 0.07em |
| Nav brand | Cormorant | Bold 700 | 1.15rem | uppercase, tracking 0.06em |
| Cover tagline | Inter | Regular 400 | 0.7rem | uppercase, tracking 0.2em |

---

## 4. Layout y Espaciado

### 4.1 Estructura Global

```css
body {
  font-family: var(--font-sans);
  color: var(--gray-900);
  background: var(--white);
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
}

html { scroll-behavior: smooth; font-size: 16px; }
```

### 4.2 Contenedor Principal

```css
section {
  padding: 6rem 2rem;
  max-width: 880px;
  margin: 0 auto;
}
```

### 4.3 Navegación

```css
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  height: 52px;
  padding: 0 2rem;
  gap: 1.2rem;
  z-index: 100;
  background: rgba(255,255,255,0.92);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--gray-200);
  display: flex;
  align-items: center;
}
```

- Brand: Cormorant 700, 1.15rem, uppercase, tracking 0.06em
- Breadcrumb: 0.65rem, tracking 0.07em, separador opacity 0.35
- Links: 0.62rem, tracking 0.07em, uppercase, gray-500 → gray-900 hover
- Separador vertical: 1px × 20px, gray-200

### 4.4 Divisor de Sección

```css
.section-divider {
  width: 100%;
  height: 1px;
  background: var(--gray-200);
  max-width: 880px;
  margin: 0 auto;
}
```

### 4.5 Breakpoints Responsivos

| Breakpoint | Cambios clave |
|------------|--------------|
| **≤768px** | Grids → 2 cols, section padding 4rem 1.5rem, cover-line 2rem, section-title 1.6rem |
| **≤480px** | Grids → 2 cols mÃ­nimo, gap reducido a 0.5rem |

---

## 5. Componentes UI

### 5.1 Swatch de Color (Paleta)

```css
.palette-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2.5rem 2rem;
}

.swatch-color {
  width: 100%;
  aspect-ratio: 1;
  border-radius: 50%;
  transition: transform 0.3s;
}
.swatch-color:hover { transform: scale(1.08); }

.swatch-name {     /* EB Garamond italic, 1.05rem, gray-900 */  }
.swatch-emotion {  /* Inter, 0.7rem, tracking 0.08em, gray-700 */ }
.swatch-flower {   /* Cormorant italic, 0.8rem, gray-500 */      }
```

### 5.2 Combo de Colores (Momento)

```css
.combo {
  display: flex;
  align-items: center;
  margin-bottom: 1px;
  background: var(--gray-50);
}
.combo-colors { display: flex; height: 64px; }
.combo-colors span { width: 64px; height: 64px; }
.combo-name { /* EB Garamond italic, 1rem */ }
.combo-use  { /* Inter, 0.8rem, weight 300 */ }
```

### 5.3 Lámina Botánica (Plate Card)

```css
.plate-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
}

.plate-card {
  aspect-ratio: 1;
  position: relative;
  overflow: hidden;
  transition: transform 0.4s ease;
}
.plate-card:hover { transform: scale(1.02); }
```

**Capas internas:**
- SVG botánico (position absolute, inset 0, 100%)
- `.plate-brand` — top 14px left 14px, EB Garamond 0.95rem weight 500
- `.plate-emotion` — bottom 30px left 14px, Inter 0.55rem uppercase tracking 0.15em
- `.plate-meta` — bottom 14px left 14px, Cormorant italic 0.55rem

**Regla tonal:** fondos oscuros (misterio) → clase `.light` → textos blancos con opacity.

### 5.4 Card de Empaque (Pack Display)

```css
.pack-display { display: flex; gap: 2.5rem; flex-wrap: wrap; justify-content: center; }

.pack-front {
  width: 280px;
  height: 390px;
  border-radius: 6px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 16px 48px rgba(0,0,0,0.12);
}
```

**Capas:**
1. Fondo gradiente emocional
2. Imagen botánica (PNG float o JPG cover)
3. Textos: marca arriba, producto + peso abajo

### 5.5 Sobre Individual

```css
.sobre-front {
  width: 190px;
  height: 230px;
  border-radius: 3px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 16px 48px rgba(0,0,0,0.18);
}
```

**Sistema de capas (z-index):**
0. `bg-foto` — imagen de fondo
1. `color-overlay` — tinte emocional, mix-blend-mode: multiply
2. `botanical` — ilustración SVG
4. `text` — marca + nombre + peso

**Dos tratamientos visuales:**
- **A (PNG sin fondo):** Flor acuarela/óleo flotando sobre gradiente emocional (145-160deg)
- **B (JPG con fondo):** FotografÃ­a botánica full-cover + tinte multiply del color emocional

### 5.6 Etiqueta Envolvente

```css
.etiqueta-wrap {
  max-width: 760px;
  height: 200px;
  border-radius: 4px;
  position: relative;
  overflow: hidden;
}
```

**Tres paneles:** left 33.33% · center 33.34% · right 33.33%
GuÃ­as de pliegue: lÃ­neas punteadas blancas a 33.33% y 66.66%.

### 5.7 Tabla de Especificaciones

```css
.spec-table { width: 100%; border-collapse: collapse; }
.spec-table th {
  font-size: 0.65rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--gray-500);
  text-align: left;
  padding: 0.75rem 1rem;
  border-bottom: 1px solid var(--gray-200);
}
.spec-table td {
  font-size: 0.9rem;
  font-weight: 300;
  padding: 0.75rem 1rem;
  border-bottom: 1px solid var(--gray-100);
  color: var(--gray-700);
}
```

### 5.8 Grid Do / Don't

```css
.dodont-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--gray-200); }
.dodont-item { padding: 1.5rem; background: var(--white); }
/* ✓ check = color arraigo (#5B6B4A) */
/* ✗ cross = color fuerza (#B5654A) */
```

### 5.9 Grid de Personalidad

```css
.personality-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--gray-200); }
/* strong: EB Garamond italic 1.1rem */
```

### 5.10 Mockup Visual

```css
.mockup {
  border: 1px solid var(--gray-200);
  border-radius: 0;
  overflow: hidden;
}
.mockup-visual {
  min-height: 300px;
  padding: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### 5.11 Grid de Instagram

```css
.ig-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2px;
  max-width: 420px;
}
.ig-post {
  aspect-ratio: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 1rem;
}
```

### 5.12 Flat Stage (escenario producto)

```css
.flat-stage {
  background: var(--gray-50);
  border-radius: 12px;
  padding: 2.5rem;
  text-align: center;
}
```

### 5.13 Full Band (sección ancha)

```css
.full-band {
  max-width: 100%;
  padding: 5rem 2rem;
}
```

---

## 6. Ilustración Botánica (SVG)

### 6.1 Estilo General

- **Técnica:** Grabado botánico / xilografÃ­a de lÃ­nea fina
- **Stroke:** solo trazo, nunca relleno sólido
- `stroke-linecap: round` siempre
- Fondos claros → trazo oscuro (#3A2E24 range, opacity 0.7-0.85)
- Fondos oscuros → trazo claro (#E8D8D0, opacity 0.7)
- ViewBox estándar: `0 0 200 200`

### 6.2 Plantas por Emoción

| Emoción | Planta | Estilo SVG | Stroke |
|---------|--------|------------|--------|
| Ternura | Rosa de jardÃ­n | CÃ­rculos concéntricos centro, pétalos elÃ­pticos, tallo con hojas, capullos | #3A2018 / 0.85 |
| Calma | Manzanilla | 3 tallos, flores tipo margarita (7 pétalos c/u), hojas compuestas | #3A2818 / 0.8 |
| Arraigo | Romero | Tallo central, hojas pareadas pequeñas, brotes arriba, raÃ­ces en base | #1A2010 / 0.75 |
| MelancolÃ­a | Lavanda | 3 tallos, racimos elÃ­pticos apilados, hojas compuestas | #1A2030 / 0.8 |
| Fuerza | Jengibre en flor | Tallo grueso, flor grande con pétalos elÃ­pticos anidados, hojas dramáticas | #2A1008 / 0.8 |
| Paz | JazmÃ­n | Tallo curvo tipo enredadera, flores de 5 pétalos, hojas pequeñas | #5A4A38 / 0.7 |
| Misterio | Damiana | Tallo central, flor radial 6 pétalos, halo circular, puntos constelación | #E8D8D0 / 0.7 |
| AlegrÃ­a | Caléndula | 2 tallos, margarita grande (9 pétalos), brote secundario, rayos solares | #2A1E08 / 0.8 |

### 6.3 Regla de Contraste en Láminas

- **La planta como protagonista absoluta** — cubre 70-80% de la superficie
- Fondo: color emocional sólido
- Marca "Florécer" top-left, Cormorant 700 Bold uppercase
- Emoción + flor bottom-left
- Máximo 1-2 tintas sobre cartulina teñida

---

## 7. Logotipo

### 7.1 Especificaciones

```
Fuente:    Cormorant 700 Bold
Caja:      UPPERCASE siempre
Tracking:  0.08–0.1em
Color:     Blanco (#FFF) sobre entorno botánico/color
           Oscuro (#3A2E24 / gray-900) sobre fondos claros
           Color emocional sobre fondos neutros
```

### 7.2 Versiones

| Versión | Color | Uso |
|---------|-------|-----|
| Principal | Blanco #FFFFFF | Sobre fotografÃ­a botánica y empaque |
| Oscura | Gray-900 #3A2E24 | Sobre fondos claros |
| Emocional | Color emocional variable | Sobre fondos neutros |
| Neutro | #171717 | Usos institucionales |

### 7.3 Reglas

- Solo Cormorant 700 Bold, siempre uppercase
- Tracking 0.08–0.1em
- Espacio mÃ­nimo = altura de la "F" en los 4 lados
- Tamaño mÃ­nimo: digital 18px, impresión 8mm
- **Prohibido:** estirar, rotar, delinear, aplicar gradiente, sombras agresivas

### 7.4 Dinamismo Cromático

El logotipo vive dentro de su entorno. Funciona sobre cualquier fondo botánico — fotografÃ­a, óleo, acuarela, o color sólido emocional. El blanco crea un efecto de embossado suave.

---

## 8. Dirección de Arte

### 8.1 FotografÃ­a

**Principios:**

| Principio | Directriz |
|-----------|-----------|
| **Luz** | Natural, hora dorada, difusa |
| **Color** | Cada sesión teñida por color emocional (dirección de arte, no filtro) |
| **Texturas** | Lino, cerámica, madera, piedra, plantas vivas — nada plástico |
| **Personas** | Manos, perfiles, siluetas, diversidad de piel, expresiones serenas |
| **Composición** | Espacio negativo generoso, asimetrÃ­a intencional, poca profundidad de campo, cenital para flatlay |

**Moods fotográficos:**

| Mood | Descripción | Colores |
|------|-------------|---------|
| Producto | Luz lateral suave, fondo neutro | Calma, Paz |
| Lifestyle | Mujeres luminosas, levemente desaturado | Ternura, AlegrÃ­a |
| Nocturno | Luz de vela, terciopelo, tonos azules | MelancolÃ­a, Misterio |
| Ritual | Manos preparando té, arreglando flores | Arraigo, Fuerza |

### 8.2 Estilo Gráfico

- **Ilustración:** Grabado botánico de lÃ­nea, siempre tono sobre tono
- **IconografÃ­a:** Lineal 1.5px, terminaciones redondeadas, nunca relleno
- **Gradientes:** Solo entre colores emocionales de la misma familia, siempre sutiles
- **Patrones:** Repetición botánica a 5-10% opacidad como textura de fondo
- **Acabado:** Levemente envejecido, como página de herbario que sobrevivió al tiempo

---

## 9. Productos y Colecciones

### 9.1 Arquitectura

```
Florécer (marca paraguas)
├── MembresÃ­a Floral (suscripción semanal de flores)
├── Herbal Blend (tisanas naturales)
└── JardÃ­n de Emociones (capa emocional Antique)
```

### 9.2 Tres Colecciones

| Colección | Emociones | Carácter |
|-----------|-----------|----------|
| **Ritual Espiritual** | Ternura, Misterio, Calma | Lo sagrado, lo Ã­ntimo |
| **Night Garden** | MelancolÃ­a, Paz, Misterio | Lo nocturno, el descanso |
| **Bienestar Botánico** | Arraigo, Fuerza, AlegrÃ­a | Lo vital, lo terrestre |

### 9.3 Catálogo de Tisanas

| Tisana | Emoción | Colección | Formatos |
|--------|---------|-----------|----------|
| Ritual de Amor | Ternura | Ritual Espiritual | 50g, 30g, 10g |
| Sueño Sagrado | Calma | Ritual Espiritual | 50g, 30g, 10g |
| CÃ­rculo Protector | Misterio/Fuerza | Ritual Espiritual | 50g, 30g, 10g |
| Mente Clara | AlegrÃ­a/Arraigo | Ritual Espiritual | 50g, 30g, 10g |
| JardÃ­n de Abundancia | AlegrÃ­a/Fuerza | Ritual Espiritual | 50g, 30g, 10g |
| Aura Limpia | Paz | Ritual Espiritual | 50g, 30g, 10g |
| Sueño del JardÃ­n | MelancolÃ­a | Night Garden | 50g, 30g, 10g |
| Calma Nocturna | Paz | Night Garden | 50g, 30g, 10g |
| EnergÃ­a del JardÃ­n | Fuerza | Bienestar | 50g, 30g, 10g |
| JardÃ­n Digestivo | Arraigo | Bienestar | 50g, 30g, 10g |
| Calma Serena | Calma | Bienestar | 50g, 30g, 10g |
| Abrazo del Vientre | Ternura | Bienestar | 50g, 30g, 10g |

Sub-marca: **Herbal Blend — JardÃ­n de Emociones**
Etiqueta genérica: "Tisana Natural"

### 9.4 Especificaciones de Empaque

| Formato | Dimensiones | Material | Impresión | Acabado |
|---------|-------------|----------|-----------|---------|
| Frente de caja | 8 × 11 cm | Cartulina 350g | CMYK + reserva UV mate | Soft touch |
| Sobre individual | 10 × 12 cm | Papel kraft laminado | CMYK | Sello térmico |
| Etiqueta de tarro | 22 × 8 cm (plano) | Papel algodón 120g | CMYK + relieve seco | Lata ∅7cm × 8cm |

---

## 10. Tono de Voz

### 10.1 Pilares

**Poética** · **Invitacional** · **Emocional** · **Conocedora**

> "Nuestra voz es la de una amiga sabia que sabe de plantas, emociones y rituales."

### 10.2 Taglines

| Contexto | Frase |
|----------|-------|
| Principal | "Un jardÃ­n en cada taza" |
| Extendido | "Flores para tu espacio. Infusiones para tu alma." |
| MembresÃ­a | "Haz que tu semana florezca" |
| Antique | "Cada flor lleva un sentir" |
| Antique alt | "Botánica del alma" · "Un herbario de emociones" |

### 10.3 GuÃ­a Verbal

**SÃ­:** Metáforas botánicas · Segunda persona (tú) · Evocar emociones/sensaciones · Frases poéticas cortas · Invitar/sugerir/inspirar · Hablar de experiencia, no producto · Usar "ritual / momento / jardÃ­n / Botanica / pausa" · Tono elevado pero accesible · Hablar como amiga cercana

**No:** Jerga · Tercera persona · Superlativos vacÃ­os · Mayúsculas gritando · Presión de venta · Precio como ventaja · Sarcasmo · Tono fast-fashion · Reducir a "floristerÃ­a" o "tienda de tés"

### 10.4 Vocabulario de Marca

**Palabras insignia:** Botanica, JardÃ­n, Ritual, Pausa, Alma, Sagrado, Botánico, Despertar, Calma, Abrazo, Aroma, RaÃ­z, Semilla, Pétalo

**Verbos preferidos:** Botanica, Pausar, Respirar, Nutrir, Abrazar, Despertar, Descubrir, Conectar, Cuidar, Transformar, Sanar, Iluminar

**Territorios semánticos:** Naturaleza · Ritual matutino/nocturno · Autocuidado · Espiritualidad suave · Hogar como santuario · Temporadas · Ciclos · Renacimiento

---

## 11. Reglas de Uso

### 11.1 Correcto ✓

- Sistema de color emocional fijo (no inventar colores)
- Grabado botánico de lÃ­nea fina
- Máximo 2-3 colores por pieza
- EB Garamond solo para emociones y frases de marca
- Inter para texto funcional
- Fondos blancos/neutros para documentos
- Cada lámina como pieza autónoma
- "¿Cómo floreces hoy?" como recurso recurrente

### 11.2 Incorrecto ✗

- Colores neón o fuera de paleta
- Más de 3 colores emocionales por pieza
- Ilustraciones de relleno sólido o flat digital
- Mezclar serif/sans sin jerarquÃ­a clara
- Reasignar emociones a colores ya definidos
- Combinar lÃ­nea Antique con filigrana dorada original
- Sombras agresivas o efectos digitales obvios
- Texturas de papel o ruido que ensucien el layout

### 11.3 JerarquÃ­a de Marca

1. **Principal** — Logo original, dorado, rosa polvo → comunicación general
2. **Antique** — JardÃ­n de Emociones → ediciones especiales, contenido emocional
3. **Colección** — Ritual / Night Garden / Bienestar → dentro de lÃ­neas de producto

> "La versión Antique no reemplaza la identidad principal. Es una capa emocional que vive dentro del universo Florécer."

---

## 12. Interacción Recurrente

**Formato "¿Cómo floreces hoy?"**
- 8 opciones emocionales para elegir
- Fondo blanco, tipografÃ­a EB Garamond italic
- Recurso repetible, interactivo, viral
- Aplicable en stories, UI de app, email, punto de venta

---

## 13. Valores Estratégicos

| Pilar | Descripción |
|-------|-------------|
| **Diferenciación premium** | Ediciones especiales coleccionables |
| **Conexión emocional** | El cliente se identifica con la emoción, no solo el producto |
| **Contenido orgánico** | "¿Cómo floreces hoy?" es repetible e interactivo |
| **Escalabilidad** | Nuevas emociones y patrones por temporada |

---

*Documento generado desde `manual-antique.html` · Florécer · Bogotá – Villa Verde, Cundinamarca · 2026*
