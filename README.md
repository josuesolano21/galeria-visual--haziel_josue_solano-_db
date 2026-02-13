# 🐉 Galería Visual DBZ - Dragon Ball Z

**Autor:** Haziel Josue Solano  
**Proyecto:** Galería Visual - Transferencia del Conocimiento  
**Año:** 2025

---

# Descripción del Proyecto

Esta es una galería web estática que exhibe 20 personajes icónicos de Dragon Ball Z con un diseño moderno y dinámico. El proyecto implementa técnicas avanzadas de CSS incluyendo gradientes, transparencias, animaciones y efectos visuales inspirados en la energía Ki del anime.

La galería presenta renders de alta calidad de héroes, villanos y guerreros legendarios con una interfaz responsiva que se adapta a cualquier dispositivo, desde móviles hasta pantallas grandes.

**Objetivo principal:** Demostrar dominio de propiedades visuales CSS mediante la creación de una interfaz atractiva, accesible y mantenible, aplicando conceptos de diseño moderno y buenas prácticas de desarrollo web.

---

# 🚀 Demo en Vivo

**GitHub Pages:** [Ver galería en vivo](https://josuesolano21.github.io/galeria-visual--haziel_josue_solano-_db/)

---

## Instrucciones para Ver en Local

**Requisitos previos:**

- Navegador web moderno (Chrome, Firefox, Edge, Safari)
- Editor de código (opcional: VS Code, Sublime Text)

**Pasos de instalación:**

1. Clonar el repositorio

```bash
git clone https://github.com/josuesolano21/galeria-visual--haziel_josue_solano-_db.git
```

2. Navegar al directorio del proyecto

```bash
cd galeria-visual-haziel_josue_solano
```

3. Abrir el proyecto (elige una opción)
   - Hacer doble clic en `index.html`
   - Usar Live Server en VS Code
   - Desde terminal:

     ```bash
     # Windows
     start index.html

     # macOS
     open index.html

     # Linux
     xdg-open index.html
     ```

---

## Estructura del Proyecto

```
galeria-visual-haziel_josue_solano
│
├── index.html              # Estructura HTML principal
├── style.css               # Estilos CSS con comentarios detallados
├── README.md               # Este archivo
│
└── galeria/
    └── imagenes/
        ├── goku_normal.webp
        ├── vegeta_normal.webp
        ├── picolo_normal.webp
        ├── Freezer.webp
        ├── Bardock_Artwork.webp
        ├── Androide_16.webp
        ├── Beerus_DBS_Broly_Artwork.webp
        ├── Androide_18_Artwork.webp
        ├── Tenshinhan_Universo7.webp
        ├── celula.webp
        ├── gohan.webp
        ├── Gran_Kaio-shin_Artwork.webp
        ├── dodoria.webp
        ├── Grand_priest.webp
        ├── Jiren.webp
        ├── Toppo.webp
        ├── Raditz_artwork_Dokkan.webp
        ├── roshi.webp
        ├── Whis_DBS_Broly_Artwork.webp
        └── Dispo_render.webp
```

---

## Decisiones de Diseño

Aquí explico las decisiones técnicas y estéticas que tomé para construir esta galería, incluyendo la selección de colores, el uso de gradientes y cómo optimicé las imágenes para que se vean perfectas.

**1. Paleta de Colores**

La paleta fue seleccionada para reflejar la energía y dinamismo característicos de Dragon Ball Z. Cada color tiene un propósito específico:

**Colores principales:**

- **Dorado/Amarillo (#ffd700, #ffb347):** Representa el Super Saiyajin, la transformación más icónica de la serie. Este color transmite poder y energía.
- **Naranja (#ff8c00, #ff6b00):** Simboliza la energía Ki y el aura de batalla que rodea a los guerreros durante el combate.
- **Azul (#4a9eff, #3b82f6):** Evoca el Kamehameha y otras técnicas energéticas. El azul también aporta balance visual y profundidad.
- **Grises oscuros (#1a1a1a, #2a2a2a):** Fondo neutro que permite resaltar los personajes sin distraer la atención. El uso de grises en lugar de negro puro mejora el contraste.

**Por qué esta combinación funciona:**

Esta paleta crea un contraste dramático entre el fondo oscuro y los elementos brillantes, simulando la estética del anime donde los guerreros emiten auras de energía luminosa. Los tonos cálidos (dorado/naranja) transmiten acción y poder, mientras que el azul añade profundidad y equilibrio visual. El fondo oscuro hace que las imágenes de los personajes destaquen sin competir por atención.

**2. Gradientes y su Propósito**

Los gradientes son fundamentales en este diseño porque simulan el flujo de energía característico de Dragon Ball Z.

**Header Principal:**

```css
background: linear-gradient(180deg, #2a2a2a 0%, #3a2510 50%, #2a2a2a 100%);
```

Este gradiente vertical crea profundidad y dirige la atención hacia el título. La transición de gris a marrón oscuro y de vuelta a gris simula un amanecer o un resplandor de energía emanando desde el centro.

**Banner Promocional:**

```css
background: linear-gradient(135deg, #2563eb, #3b82f6, #60a5fa);
```

Un gradiente azul vibrante en diagonal (135 grados) que destaca el contenido promocional. La dirección diagonal ascendente guía el ojo naturalmente y transmite dinamismo. Este banner usa tonos azules más claros para contrastar con el fondo oscuro general.

**Título con Gradiente Animado:**

```css
background: linear-gradient(135deg, #ffd700 0%, #ff8c00 50%, #4a9eff 100%);
animation: rainbowShift 5s ease infinite;
```

Este es el gradiente más complejo. Simula el aura multicolor de transformaciones poderosas como el Ultra Instinto. El movimiento constante (animation) capta la atención y añade vida al diseño. Los tres colores representan diferentes etapas de poder: dorado (Super Saiyajin), naranja (energía máxima), azul (técnicas divinas).

**Overlay de Cards (al hacer hover):**

```css
background: linear-gradient(
  135deg,
  rgba(255, 215, 0, 0.35) 0%,
  rgba(255, 140, 0, 0.25) 50%,
  rgba(74, 158, 255, 0.35) 100%
);
```

Utiliza transparencias (rgba) para crear una capa de color que envuelve al personaje sin ocultarlo. Este efecto simula el aura Ki activándose cuando el usuario interactúa con la card. La transición de colores sugiere energía fluyendo alrededor del guerrero.

**3. Optimización de Imágenes**

Este fue uno de los desafíos más importantes del proyecto. Las imágenes son renders (personajes extraídos sin fondo) y necesitaban verse completos sin zoom excesivo.

**Técnicas aplicadas:**

**object-fit: contain**
Esta propiedad es crucial. A diferencia de `object-fit: cover` que recorta la imagen para llenar el espacio, `contain` mantiene las proporciones originales y muestra el render completo. Esto evita que se corten las cabezas, brazos o detalles importantes de los personajes.

**Padding interno (20px)**
Agregué padding alrededor de cada imagen para crear espacio respiratorio. Esto evita que los renders se peguen a los bordes de las cards y les da un marco visual natural. El espacio en blanco (bueno, en gris oscuro) es tan importante como el contenido.

**Background con gradiente radial:**

```css
background: radial-gradient(circle, #2a2a2a 0%, #1a1a1a 100%);
```

El fondo de cada imagen tiene un gradiente radial que va del centro hacia los bordes, creando un efecto de spotlight. Esto hace que los personajes parezcan estar iluminados desde atrás, añadiendo profundidad sin distraer.

**Altura fija responsiva:**

```css
height: 350px; /* Desktop */
height: 280px; /* Tablet */
height: 320px; /* Mobile */
```

Mantener una altura consistente en todas las cards crea armonía visual en el grid. La altura varía según el dispositivo para aprovechar mejor el espacio de pantalla disponible. En móviles la altura es mayor porque la pantalla es vertical.

**4. Animaciones y Efectos Dinámicos**

Las animaciones añaden vida y modernidad al diseño, pero deben usarse con moderación para no abrumar.

**Entrada Progresiva (Efecto Cascada):**

```css
animation: fadeInScale 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275) backwards;
animation-delay:
  0.05s,
  0.1s,
  0.15s... (hasta 1s para 20 cards);
```

Cada card aparece secuencialmente con un pequeño delay entre ellas. Este efecto crea una experiencia de carga dinámica y profesional. La función `cubic-bezier` personalizada crea un movimiento con un ligero rebote al final (elastic easing), haciendo que las cards "aterricen" suavemente.

**Hover 3D:**

```css
transform: translateY(-15px) rotateX(5deg) scale(1.02);
```

Cuando pasas el mouse sobre una card, esta se eleva 15px, rota ligeramente en el eje X (efecto 3D) y aumenta su tamaño un 2%. Este feedback visual inmediato le dice al usuario que el elemento es interactivo. La rotación sutil añade profundidad sin ser mareante.

**Partículas de Energía en el Fondo:**

```css
animation: energyPulse 15s ease-in-out infinite;
```

El fondo tiene puntos de luz que pulsan sutilmente durante 15 segundos en loop infinito. Estos "pulsos" son tan lentos que casi no se notan conscientemente, pero añaden vida al diseño. Es un detalle sutil que evita que la página se sienta completamente estática.

**5. Accesibilidad y Legibilidad**

Un buen diseño no solo debe verse bien, sino ser usable y accesible para todos.

**Contraste de Texto:**

Todos los textos cumplen con las pautas WCAG (Web Content Accessibility Guidelines):

- Títulos dorados sobre fondo oscuro: Ratio de contraste mayor a 7:1 (AAA)
- Descripciones en gris claro: Ratio mayor a 4.5:1 (AA)
- Text-shadow mejora la separación del texto del fondo

**Uso de Transparencias (rgba):**

```css
background: rgba(20, 20, 20, 0.9);
```

Las capas semitransparentes permiten ver sutilmente lo que hay detrás sin bloquear completamente el fondo. Esto mantiene el contexto visual mientras asegura que el texto sea perfectamente legible. El valor 0.9 (90% de opacidad) es suficiente para la legibilidad sin ser opaco al 100%.

**Text-shadow para Legibilidad:**

```css
text-shadow:
  0 0 15px rgba(255, 215, 0, 0.9),
  0 2px 4px rgba(0, 0, 0, 0.8);
```

Las sombras de texto tienen doble propósito: añaden el efecto de "glow" característico de DBZ y mejoran la legibilidad al crear separación entre el texto y cualquier elemento de fondo. La primera sombra es el glow luminoso, la segunda es una sombra oscura tradicional.

---

##Tecnologías Utilizadas

- **HTML5:** Estructura semántica con etiquetas apropiadas (header, main, footer, section)
- **CSS3:** Estilos avanzados incluyendo:
  - Gradientes lineales y radiales
  - Animaciones con @keyframes
  - Transformaciones 2D y 3D
  - Transparencias con rgba
  - Filtros (blur, brightness, contrast)
  - Transiciones suaves
- **CSS Grid:** Sistema de layout responsivo con auto-fill y minmax
- **Flexbox:** Para alineación y distribución interna de elementos
- **Media Queries:** Diseño adaptativo para móvil, tablet y desktop

---

# Características Principales

**Interfaz Visual:**

- Diseño moderno inspirado en la estética energética de Dragon Ball Z
- Efectos de hover con transformaciones 3D en las cards
- Animaciones suaves y fluidas que no afectan el rendimiento
- Gradientes dinámicos con colores vibrantes y llamativos
- Efecto de partículas de energía en el fondo

**Diseño Responsive:**

- Adaptable a dispositivos móviles, tablets y escritorio
- Grid flexible que reorganiza automáticamente las columnas
- Imágenes optimizadas con diferentes tamaños según el dispositivo
- Tipografía que escala proporcionalmente
- Touch-friendly: elementos suficientemente grandes para tocar en móvil

**Accesibilidad:**

- Contraste de color cumple estándares WCAG AA
- Etiquetas semánticas HTML5 para screen readers
- Atributo alt en todas las imágenes
- Navegación por teclado funcional
- Sin dependencia de color único para transmitir información

**Efectos Visuales:**

- Partículas de energía animadas en el fondo
- Overlay de aura colorida al hacer hover
- Texto con efecto de brillo (glow) dorado
- Entrada progresiva con efecto cascada
- Sombras múltiples para profundidad

---

# Requerimientos Cumplidos

**Estructura del Proyecto:**

- [x] Repositorio en GitHub con nombre descriptivo
- [x] README.md completo con todas las secciones solicitadas
- [x] Publicado en GitHub Pages
- [x] URL pública accesible

**Contenido de la Galería:**

- [x] 20 personajes de Dragon Ball Z exhibidos
- [x] Cada item incluye imagen, título y descripción
- [x] Organización clara y visualmente atractiva
- [x] Recursos gráficos suministrados utilizados correctamente

**Implementación CSS (obligatorio):**

- [x] Paleta de colores definida y utilizada consistentemente
- [x] Gradientes implementados en al menos dos secciones (header y banner)
- [x] Imágenes como background con propiedades correctamente configuradas
- [x] Transparencias (rgba) utilizadas para overlays y capas
- [x] Contraste suficiente entre texto y fondo (WCAG AA/AAA)

**Documentación del Código:**

- [x] CSS con comentarios explicativos detallados
- [x] HTML estructurado y con comentarios
- [x] README con sección "Decisiones de diseño" extensa
- [x] Cada decisión técnica justificada
- [x] Commits con mensajes descriptivos y claros

# Notas de Desarrollo

**Desafíos que enfrenté:**

1. **Zoom excesivo en imágenes:** Al principio usaba `object-fit: cover` que recortaba los renders. Lo solucioné cambiando a `object-fit: contain` con padding, lo que muestra los personajes completos sin distorsión.

2. **Contraste insuficiente en textos:** Los textos sobre fondos complejos eran difíciles de leer. Añadí múltiples capas de text-shadow y fondos semitransparentes para mejorar la legibilidad sin sacrificar el diseño.

3. **Animaciones que afectaban el rendimiento:** Las animaciones iniciales eran demasiadas y ralentizaban el navegador. Optimicé usando `will-change`, reduciendo el número de animaciones simultáneas y usando `cubic-bezier` más eficientes.

4. **Grid que no se adaptaba bien en móvil:** El grid automático creaba columnas muy estrechas en móviles. Solucioné usando media queries con una sola columna para pantallas pequeñas.

**Aprendizajes clave:**

- La importancia de `object-fit: contain` para mantener proporciones de imágenes irregulares (renders)
- Cómo balancear efectos visuales llamativos con rendimiento y usabilidad
- El uso estratégico de transparencias (rgba) para crear profundidad sin perder legibilidad
- Animaciones secuenciales con nth-child crean experiencias más dinámicas que cargas instantáneas
- Los comentarios extensos en CSS facilitan muchísimo el mantenimiento futuro
- La documentación clara es tan importante como el código mismo

# Autor

_Haziel Josue Solano_

- Email: josues230@hotmail.com
- Proyecto: Galería Visual DBZ

⭐ Si te gustó este proyecto, dale una estrella en GitHub!⭐

---

_Última actualización: Diciembre 2025_
brrrrr
prueba 3
wawa
