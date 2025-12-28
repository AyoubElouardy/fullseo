<!DOCTYPE html>
<html lang="es">
<head>
    <!-- Metadatos esenciales para SEO -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página web optimizada para SEO con las mejores prácticas de posicionamiento en buscadores. Ofrecemos soluciones digitales efectivas.">
    <meta name="keywords" content="SEO, posicionamiento web, optimización, buscadores, marketing digital">
    <meta name="author" content="Tu Empresa">
    <meta name="robots" content="index, follow">
    
    <!-- Open Graph para redes sociales -->
    <meta property="og:title" content="Página Web Full SEO - Mejores Prácticas">
    <meta property="og:description" content="Plantilla web completamente optimizada para SEO con técnicas avanzadas de posicionamiento.">
    <meta property="og:image" content="https://ejemplo.com/imagen-seo.jpg">
    <meta property="og:url" content="https://ejemplo.com">
    <meta property="og:type" content="website">
    
    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Página Web Full SEO - Mejores Prácticas">
    <meta name="twitter:description" content="Plantilla web completamente optimizada para SEO con técnicas avanzadas de posicionamiento.">
    <meta name="twitter:image" content="https://ejemplo.com/imagen-seo.jpg">
    
    <!-- Schema.org markup para rich snippets -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebSite",
      "name": "Página Web Full SEO",
      "description": "Plantilla web completamente optimizada para SEO",
      "url": "https://ejemplo.com",
      "potentialAction": {
        "@type": "SearchAction",
        "target": "https://ejemplo.com/buscar?q={search_term_string}",
        "query-input": "required name=search_term_string"
      }
    }
    </script>
    
    <!-- Canonical URL -->
    <link rel="canonical" href="https://ejemplo.com">
    
    <!-- Favicon y iconos -->
    <link rel="icon" type="image/x-icon" href="favicon.ico">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    
    <!-- Título optimizado para SEO -->
    <title>Página Web Full SEO - Mejores Prácticas de Optimización | Tu Empresa</title>
    
    <!-- CSS optimizado y minificado -->
    <style>
        /* Reset CSS básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* Estilos generales */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        /* Contenedor principal */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Encabezado */
        header {
            background-color: #2c3e50;
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .logo span {
            color: #3498db;
        }
        
        /* Navegación */
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav li {
            margin-left: 1.5rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: #3498db;
        }
        
        /* Menú móvil */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero section */
        .hero {
            background: linear-gradient(135deg, #3498db 0%, #2c3e50 100%);
            color: white;
            padding: 4rem 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .cta-button {
            display: inline-block;
            background-color: #e74c3c;
            color: white;
            padding: 0.8rem 1.8rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .cta-button:hover {
            background-color: #c0392b;
        }
        
        /* Secciones de contenido */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: #2c3e50;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }
        
        .section-title p {
            color: #7f8c8d;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Tarjetas de servicios */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background-color: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: #3498db;
            margin-bottom: 1rem;
        }
        
        .service-card h3 {
            margin-bottom: 1rem;
            color: #2c3e50;
        }
        
        /* Optimizaciones SEO destacadas */
        .seo-features {
            background-color: #f1f8ff;
        }
        
        .features-list {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .feature-item {
            margin-bottom: 2rem;
            padding-left: 2.5rem;
            position: relative;
        }
        
        .feature-item:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #27ae60;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        /* Footer */
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h3 {
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            color: #3498db;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section li {
            margin-bottom: 0.7rem;
        }
        
        .footer-section a {
            color: #ecf0f1;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: #3498db;
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #34495e;
            color: #bdc3c7;
            font-size: 0.9rem;
        }
        
        /* Estilos responsivos */
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: #2c3e50;
                flex-direction: column;
                padding: 1rem 0;
            }
            
            nav.active ul {
                display: flex;
            }
            
            nav li {
                margin: 0;
                text-align: center;
                padding: 0.8rem 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            section {
                padding: 3rem 0;
            }
        }
        
        /* Mejoras de accesibilidad */
        .sr-only {
            position: absolute;
            width: 1px;
            height: 1px;
            padding: 0;
            margin: -1px;
            overflow: hidden;
            clip: rect(0, 0, 0, 0);
            white-space: nowrap;
            border: 0;
        }
        
        /* Enfoque para navegación por teclado */
        a:focus, button:focus {
            outline: 3px solid #3498db;
            outline-offset: 2px;
        }
        
        /* Optimizaciones de rendimiento */
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <!-- Encabezado con navegación -->
    <header>
        <div class="container header-container">
            <div class="logo">Web<span>SEO</span></div>
            
            <nav id="main-nav">
                <div class="menu-toggle" id="menu-toggle" aria-label="Abrir menú" role="button" tabindex="0">
                    ☰
                </div>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#servicios">Servicios SEO</a></li>
                    <li><a href="#optimizaciones">Optimizaciones</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Contenido principal -->
    <main>
        <!-- Sección Hero -->
        <section class="hero" id="inicio">
            <div class="container">
                <h1>Página Web Full SEO - Optimización Total para Motores de Búsqueda</h1>
                <p>Implementamos todas las mejores prácticas de SEO técnico, on-page y off-page para maximizar tu visibilidad en los resultados de búsqueda y atraer tráfico cualificado.</p>
                <a href="#servicios" class="cta-button">Descubre nuestras soluciones SEO</a>
            </div>
        </section>

        <!-- Sección de servicios SEO -->
        <section id="servicios">
            <div class="container">
                <div class="section-title">
                    <h2>Servicios SEO Especializados</h2>
                    <p>Ofrecemos soluciones integrales de posicionamiento web que cubren todos los aspectos del SEO moderno.</p>
                </div>
                
                <div class="services-grid">
                    <article class="service-card">
                        <div class="service-icon">🔍</div>
                        <h3>SEO Técnico</h3>
                        <p>Optimización de la estructura del sitio, velocidad de carga, indexabilidad, y solución de problemas técnicos que afectan al posicionamiento.</p>
                    </article>
                    
                    <article class="service-card">
                        <div class="service-icon">✍️</div>
                        <h3>SEO On-Page</h3>
                        <p>Optimización de contenido, etiquetas HTML, estructura de URLs, y elementos internos para maximizar la relevancia para palabras clave objetivo.</p>
                    </article>
                    
                    <article class="service-card">
                        <div class="service-icon">📈</div>
                        <h3>SEO Off-Page</h3>
                        <p>Estrategias de link building, gestión de reputación online, y creación de autoridad de dominio para mejorar la clasificación en buscadores.</p>
                    </article>
                </div>
            </div>
        </section>

        <!-- Sección de optimizaciones implementadas -->
        <section class="seo-features" id="optimizaciones">
            <div class="container">
                <div class="section-title">
                    <h2>Optimizaciones SEO Implementadas</h2>
                    <p>Esta página web incluye todas las mejores prácticas de SEO que garantizan un posicionamiento óptimo en los motores de búsqueda.</p>
                </div>
                
                <div class="features-list">
                    <div class="feature-item">
                        <h3>Estructura HTML5 Semántica</h3>
                        <p>Uso de etiquetas semánticas como &lt;header&gt;, &lt;nav&gt;, &lt;main&gt;, &lt;section&gt;, &lt;article&gt; y &lt;footer&gt; para mejorar la comprensión del contenido por parte de los motores de búsqueda.</p>
                    </div>
                    
                    <div class="feature-item">
                        <h3>Metaetiquetas Optimizadas</h3>
                        <p>Title y description únicos y relevantes, etiquetas Open Graph para redes sociales, y meta robots configuradas correctamente.</p>
                    </div>
                    
                    <div class="feature-item">
                        <h3>URL Canónica y Schema Markup</h3>
                        <p>Implementación de URL canónica para evitar contenido duplicado y microdatos Schema.org para rich snippets en los resultados de búsqueda.</p>
                    </div>
                    
                    <div class="feature-item">
                        <h3>Rendimiento y Velocidad</h3>
                        <p>Código CSS optimizado y minimizado, imágenes responsivas, y estructura de carga eficiente para tiempos de carga rápidos.</p>
                    </div>
                    
                    <div class="feature-item">
                        <h3>Diseño Responsive y Mobile-First</h3>
                        <p>Adaptación perfecta a todos los dispositivos, esencial para el SEO móvil y la experiencia de usuario.</p>
                    </div>
                    
                    <div class="feature-item">
                        <h3>Accesibilidad Web</h3>
                        <p>Navegación por teclado, contraste de colores adecuado, y etiquetas ARIA para usuarios con discapacidades.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Pie de página -->
    <footer id="contacto">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>WebSEO</h3>
                    <p>Especialistas en optimización para motores de búsqueda y posicionamiento web. Implementamos estrategias SEO efectivas y medibles.</p>
                </div>
                
                <div class="footer-section">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#servicios">Servicios SEO</a></li>
                        <li><a href="#optimizaciones">Optimizaciones</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Contacto</h3>
                    <ul>
                        <li>Email: info@webseo.com</li>
                        <li>Teléfono: +34 123 456 789</li>
                        <li>Dirección: Calle SEO, 123, Madrid</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 WebSEO. Todos los derechos reservados. | <a href="/politica-privacidad">Política de Privacidad</a> | <a href="/mapa-del-sitio">Mapa del Sitio</a></p>
                <!-- Mapa del sitio para SEO -->
                <span class="sr-only">
                    <a href="/sitemap.xml">Mapa del sitio XML</a>
                </span>
            </div>
        </div>
    </footer>

    <!-- JavaScript optimizado para SEO -->
    <script>
        // Menú móvil
        document.addEventListener('DOMContentLoaded', function() {
            const menuToggle = document.getElementById('menu-toggle');
            const nav = document.getElementById('main-nav');
            
            menuToggle.addEventListener('click', function() {
                nav.classList.toggle('active');
            });
            
            // Cerrar menú al hacer clic en un enlace (móvil)
            const navLinks = document.querySelectorAll('nav a');
            navLinks.forEach(link => {
                link.addEventListener('click', () => {
                    nav.classList.remove('active');
                });
            });
            
            // Navegación suave
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if(targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if(targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // Lazy loading para imágenes (ejemplo)
            const images = document.querySelectorAll('img[data-src]');
            const imageOptions = {
                threshold: 0,
                rootMargin: '0px 0px 50px 0px'
            };
            
            const imageObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if(entry.isIntersecting) {
                        const img = entry.target;
                        img.src = img.getAttribute('data-src');
                        img.removeAttribute('data-src');
                        observer.unobserve(img);
                    }
                });
            }, imageOptions);
            
            images.forEach(img => imageObserver.observe(img));
        });
        
        // Registro del Service Worker para PWA (opcional)
        if('serviceWorker' in navigator) {
            window.addEventListener('load', () => {
                navigator.serviceWorker.register('/sw.js').then(() => {
                    console.log('Service Worker registrado correctamente');
                }).catch(error => {
                    console.log('Error al registrar Service Worker:', error);
                });
            });
        }
    </script>
</body>
</html>
