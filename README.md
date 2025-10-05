# 🚀 Portafolio Personal - Fernando Villarroel

Portafolio web profesional desarrollado con tecnologías frontend modernas, diseñado para mostrar mis habilidades, proyectos y experiencia como Desarrollador Full Stack.

🌐 **Demo en vivo:** [fernandoavillarroel.github.io](https://fernandoavillarroel.github.io)

---

## 📋 Tabla de Contenidos

- [Descripción](#descripción)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Características Técnicas](#características-técnicas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación](#instalación)
- [Aspectos Destacados del Desarrollo](#aspectos-destacados-del-desarrollo)
- [Responsividad](#responsividad)
- [Optimizaciones](#optimizaciones)
- [Contacto](#contacto)

---

## 📝 Descripción

Portafolio personal de una sola página (SPA - Single Page Application) que presenta mi perfil profesional, habilidades técnicas y proyectos destacados. El diseño implementa principios modernos de UX/UI con animaciones fluidas y un sistema de navegación intuitivo.

---

## 🛠️ Tecnologías Utilizadas

### Frontend Core
- **HTML5**: Estructura semántica y accesible
- **CSS3**: Estilos avanzados con animaciones y efectos visuales
- **JavaScript (Vanilla)**: Interactividad y navegación smooth scroll

### Frameworks y Librerías
- **Bootstrap 5.3.2**: Sistema de grillas responsive y componentes UI
- **Bootstrap Icons 1.11.1**: Iconografía vectorial escalable

### Herramientas de Desarrollo
- **Git**: Control de versiones
- **GitHub Pages**: Hosting y despliegue automático
- **Visual Studio Code**: Entorno de desarrollo

---

## ⚡ Características Técnicas

### 1. Animaciones CSS Personalizadas
Implementación de keyframes avanzados para efectos visuales:
```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

Efectos implementados:

fadeInUp: Entrada progresiva de elementos
float: Animación de flotación continua
gradientShift: Gradiente animado en el fondo

2. Sistema de Navegación Smooth Scroll
Navegación suave entre secciones con JavaScript vanilla:

document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
});


3. Intersection Observer API
Animación de elementos al entrar en el viewport:

const observer = new IntersectionObserver(function(entries) {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.style.animation = 'fadeInUp 1s ease forwards';
        }
    });
}, { threshold: 0.1 });

4. Diseño Glassmorphism
Efectos de vidrio esmerilado con backdrop-filter:
.card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(168, 85, 247, 0.3);
}

5. Sistema de Grillas Responsive
Implementación de Bootstrap Grid System con breakpoints personalizados:

Desktop (lg): 3 columnas para proyectos
Tablet (md): 2 columnas
Mobile (sm): 1 columna

6. Gradientes Dinámicos
Gradientes animados en CSS con múltiples colores:

body {
    background: linear-gradient(-45deg, #1a1a2e, #16213e, #0f3460, #1a1a2e);
    background-size: 400% 400%;
    animation: gradientShift 15s ease infinite;
}
📁 Estructura del Proyecto

Mi-Portafolio/
│
├── index.html              # Archivo principal HTML
├── IMG_5159.PNG           # Imagen de perfil
├── Screenshot_659.png     # Captura proyecto FONAVI
└── README.md              # Documentación del proyecto
Arquitectura del HTML
El proyecto está estructurado en secciones semánticas:

<nav>: Barra de navegación fija con colapso responsive
Hero Section: Presentación principal con imagen de perfil animada
About Section: Grid de 2 columnas con habilidades técnicas y blandas
Projects Section: Cards de proyectos con badges de tecnologías
Contact Section: Tarjetas de contacto y formulario
<footer>: Redes sociales y copyright


🚀 Instalación
Clonar el repositorio
git clone https://github.com/FernandoAVillarroel/fernandoavillarroel.github.io.git
cd fernandoavillarroel.github.io
Visualización local

 Live Server (VS Code)
# Instalar extensión Live Server
   # Click derecho en index.html > Open with Live Server

💡 Aspectos Destacados del Desarrollo
1. Diseño Mobile-First
El portafolio fue desarrollado siguiendo la metodología Mobile-First, asegurando una experiencia óptima en dispositivos móviles antes de escalar a pantallas más grandes.
2. Accesibilidad (a11y)

Etiquetas semánticas HTML5
Atributos alt en todas las imágenes
Contraste de colores según WCAG 2.1
Navegación por teclado funcional

3. Performance

CSS minificado en línea
Carga de Bootstrap desde CDN con caché
Imágenes optimizadas
Lazy loading con Intersection Observer

4. SEO Básico

Meta tags descriptivos
Estructura semántica
URLs amigables

5. Cross-Browser Compatibility
Probado y funcional en:

Chrome 90+
Firefox 88+
Safari 14+
Edge 90+


📱 Responsividad
Breakpoints implementados
css/* Mobile */
@media (max-width: 768px) {
    .hero-title { font-size: 2.5rem; }
    .profile-img { width: 200px; height: 200px; }
}

/* Tablet */
@media (min-width: 768px) and (max-width: 992px) {
    /* Estilos para tablets */
}

/* Desktop */
@media (min-width: 992px) {
    /* Estilos para desktop */
}
Grid System

col-12: 100% en móvil
col-md-6: 50% en tablet
col-lg-4: 33.33% en desktop


⚙️ Optimizaciones
CSS

Uso de variables CSS para colores consistentes
Pseudo-elementos para efectos visuales (evita DOM extra)
Transiciones hardware-accelerated con transform y opacity

JavaScript

Event delegation para mejor performance
Uso de IntersectionObserver en lugar de scroll listeners
Debouncing en eventos de scroll

Carga de Recursos

Bootstrap desde CDN de Cloudflare
Iconos vectoriales (SVG) en lugar de fuentes icon-fonts
Imágenes en formato optimizado


🎨 Paleta de Colores
css/* Colores principales */
--primary-gradient: linear-gradient(45deg, #a855f7, #ec4899);
--dark-bg: #1a1a2e;
--secondary-bg: #16213e;
--accent: #0f3460;
--text-primary: #e0e0e0;
--text-muted: #b0b0b0;

📬 Contacto

Portfolio: fernandoavillarroel.github.io
LinkedIn: Fernando Villarroel
GitHub: @FernandoAVillarroel
Email: agustinvillarroel17@gmail.com


📄 Licencia
Este proyecto está bajo la Licencia MIT. Puedes usarlo como referencia para tu propio portafolio.
