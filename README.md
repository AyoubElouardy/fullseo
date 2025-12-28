<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Universo Digital - Explorando la Tecnología y el Conocimiento</title>
    <style>
        /* Reset y configuración global */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            height: 100%;
            width: 100%;
            font-family: 'Arial', 'Helvetica', sans-serif;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* Navegación fija */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(20, 20, 40, 0.95);
            padding: 15px 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            background: linear-gradient(45deg, #6a11cb, #2575fc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 16px;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 8px 15px;
            border-radius: 20px;
        }

        .nav-links a:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
        }

        /* Sección Hero - Ocupa toda la pantalla */
        .hero {
            height: 100vh;
            width: 100%;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
                        url('https://images.unsplash.com/photo-1519681393784-d120267933ba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .hero-content {
            max-width: 800px;
            animation: fadeIn 1.5s ease-out;
        }

        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 30px;
            line-height: 1.6;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(45deg, #6a11cb, #2575fc);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-size: 18px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(106, 17, 203, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(106, 17, 203, 0.6);
        }

        /* Secciones de contenido - Cada una ocupa 100vh */
        .section {
            min-height: 100vh;
            width: 100%;
            padding: 100px 20px;
            display: flex;
            align-items: center;
        }

        .section:nth-child(even) {
            background: #f8f9fa;
        }

        .section-container {
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }

        /* Sección Sobre Nosotros */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text h2 {
            font-size: 3rem;
            margin-bottom: 25px;
            color: #2c3e50;
        }

        .about-text p {
            font-size: 1.2rem;
            line-height: 1.8;
            color: #555;
            margin-bottom: 20px;
        }

        .about-image {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
            height: 500px;
            background: url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
        }

        /* Sección Servicios */
        .services-container {
            text-align: center;
        }

        .services-container h2 {
            font-size: 3rem;
            margin-bottom: 60px;
            color: #2c3e50;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .service-card {
            background: white;
            border-radius: 15px;
            padding: 40px 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
            border-top: 5px solid #6a11cb;
        }

        .service-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .service-icon {
            font-size: 50px;
            margin-bottom: 25px;
        }

        .service-card h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #2c3e50;
        }

        .service-card p {
            color: #666;
            line-height: 1.7;
        }

        /* Sección Galería */
        .gallery-container h2 {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 60px;
            color: #2c3e50;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
        }

        .gallery-item {
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Sección Estadísticas */
        .stats-section {
            background: linear-gradient(rgba(20, 20, 40, 0.9), rgba(20, 20, 40, 0.9)),
                        url('https://images.unsplash.com/photo-1517077304055-6e89abbf09b0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80');
            background-size: cover;
            background-attachment: fixed;
            color: white;
            text-align: center;
        }

        .stats-container h2 {
            font-size: 3rem;
            margin-bottom: 60px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
        }

        .stat-item h3 {
            font-size: 4rem;
            margin-bottom: 15px;
            color: #6a11cb;
        }

        .stat-item p {
            font-size: 1.3rem;
            opacity: 0.9;
        }

        /* Sección Equipo */
        .team-container h2 {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 60px;
            color: #2c3e50;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }

        .team-card {
            text-align: center;
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
        }

        .team-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 25px;
            overflow: hidden;
            border: 5px solid #f0f0f0;
        }

        .team-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .team-card h3 {
            font-size: 1.6rem;
            margin-bottom: 10px;
            color: #2c3e50;
        }

        .team-card p {
            color: #6a11cb;
            margin-bottom: 20px;
            font-weight: 500;
        }

        /* Sección Contacto */
        .contact-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-container h2 {
            font-size: 3rem;
            margin-bottom: 60px;
            text-align: center;
            color: #2c3e50;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 60px;
        }

        .contact-info {
            background: linear-gradient(45deg, #6a11cb, #2575fc);
            color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(106, 17, 203, 0.3);
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 30px;
        }

        .contact-details {
            margin-bottom: 40px;
        }

        .contact-details p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .contact-details i {
            margin-right: 15px;
            font-size: 1.2rem;
        }

        .social-links {
            display: flex;
            gap: 20px;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            font-size: 1.3rem;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: white;
            color: #6a11cb;
            transform: translateY(-5px);
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 25px;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #6a11cb;
            box-shadow: 0 0 0 3px rgba(106, 17, 203, 0.1);
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }

        .submit-btn {
            background: linear-gradient(45deg, #6a11cb, #2575fc);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(106, 17, 203, 0.4);
        }

        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(106, 17, 203, 0.6);
        }

        /* Footer */
        footer {
            background: #1a1a2e;
            color: white;
            padding: 60px 20px 30px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 50px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: #6a11cb;
        }

        .footer-column p {
            line-height: 1.7;
            opacity: 0.8;
            margin-bottom: 20px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 15px;
        }

        .footer-links a {
            color: #ddd;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-links a:hover {
            color: #6a11cb;
            padding-left: 10px;
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .floating {
            animation: float 5s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
                background: none;
                border: none;
                color: white;
                font-size: 28px;
                cursor: pointer;
            }
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .section {
                padding: 80px 20px;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-text h2,
            .services-container h2,
            .gallery-container h2,
            .stats-container h2,
            .team-container h2,
            .contact-container h2 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .cta-button {
                padding: 12px 30px;
                font-size: 16px;
            }
            
            .service-card,
            .team-card {
                padding: 30px 20px;
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Estilos para scroll personalizado */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(45deg, #6a11cb, #2575fc);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(45deg, #5a0cb9, #1c68e8);
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <!-- Navegación -->
    <nav>
        <div class="nav-container">
            <div class="logo">UniversoDigital</div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#galeria">Galería</a></li>
                <li><a href="#estadisticas">Estadísticas</a></li>
                <li><a href="#equipo">Equipo</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Sección Hero -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Explorando el Futuro Digital</h1>
            <p>Descubre un universo de posibilidades donde la tecnología y la creatividad se fusionan para crear experiencias extraordinarias. Impulsamos la innovación y transformamos ideas en realidades digitales.</p>
            <a href="#nosotros" class="cta-button">Comenzar Aventura <i class="fas fa-arrow-right"></i></a>
        </div>
    </section>

    <!-- Sección Nosotros -->
    <section class="section" id="nosotros">
        <div class="section-container">
            <div class="about-content">
                <div class="about-text">
                    <h2>Nuestra Historia y Misión</h2>
                    <p>Fundada en 2015, nuestra empresa ha estado a la vanguardia de la revolución digital, ayudando a organizaciones de todos los tamaños a navegar por el complejo panorama tecnológico actual.</p>
                    <p>Creemos en el poder transformador de la tecnología cuando se combina con una visión estratégica y un enfoque centrado en las personas. Nuestro equipo multidisciplinario reúne experiencia en desarrollo de software, diseño UX/UI, análisis de datos y estrategia digital.</p>
                    <p>Hemos completado más de 500 proyectos exitosos para clientes en 15 países diferentes, siempre manteniendo nuestro compromiso con la excelencia, la innovación y la satisfacción del cliente.</p>
                    <a href="#contacto" class="cta-button">Conoce Más</a>
                </div>
                <div class="about-image"></div>
            </div>
        </div>
    </section>

    <!-- Sección Servicios -->
    <section class="section" id="servicios">
        <div class="section-container">
            <div class="services-container">
                <h2>Nuestros Servicios</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-code"></i>
                        </div>
                        <h3>Desarrollo Web</h3>
                        <p>Creación de sitios web y aplicaciones personalizadas utilizando las tecnologías más modernas y eficientes. Desarrollamos soluciones escalables que se adaptan a tus necesidades específicas.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-paint-brush"></i>
                        </div>
                        <h3>Diseño UI/UX</h3>
                        <p>Diseños centrados en el usuario que combinan estética y funcionalidad. Investigamos, prototipamos y testeamos para crear experiencias digitales intuitivas y memorables.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <h3>Marketing Digital</h3>
                        <p>Estrategias integrales de marketing online para aumentar tu visibilidad, generar leads y maximizar el retorno de inversión. Desde SEO hasta campañas publicitarias en redes sociales.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-cloud"></i>
                        </div>
                        <h3>Soluciones Cloud</h3>
                        <p>Migración, implementación y gestión de infraestructuras en la nube. Optimizamos tus recursos tecnológicos para mejorar la eficiencia y reducir costos operativos.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-mobile-alt"></i>
                        </div>
                        <h3>Apps Móviles</h3>
                        <p>Desarrollo de aplicaciones nativas e híbridas para iOS y Android. Creamos soluciones móviles que ofrecen experiencias fluidas y de alto rendimiento.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Ciberseguridad</h3>
                        <p>Protección integral de tus activos digitales. Evaluamos vulnerabilidades, implementamos medidas de seguridad y monitoreamos amenazas en tiempo real.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Galería -->
    <section class="section" id="galeria">
        <div class="section-container">
            <div class="gallery-container">
                <h2>Nuestros Proyectos</h2>
                <div class="gallery-grid">
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 1">
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1545235617-9465d2a55698?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 2">
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 3">
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 4">
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1542744095-fcf48d80b0fd?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 5">
                    </div>
                    <div class="gallery-item">
                        <img src="https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Proyecto 6">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Estadísticas -->
    <section class="section stats-section" id="estadisticas">
        <div class="section-container">
            <div class="stats-container">
                <h2>En Números</h2>
                <div class="stats-grid">
                    <div class="stat-item">
                        <h3 class="floating">500+</h3>
                        <p>Proyectos Completados</p>
                    </div>
                    <div class="stat-item">
                        <h3 class="floating">15</h3>
                        <p>Países Alcanzados</p>
                    </div>
                    <div class="stat-item">
                        <h3 class="floating">98%</h3>
                        <p>Clientes Satisfechos</p>
                    </div>
                    <div class="stat-item">
                        <h3 class="floating">50+</h3>
                        <p>Expertos en Equipo</p>
                    </div>
                    <div class="stat-item">
                        <h3 class="floating">24/7</h3>
                        <p>Soporte Disponible</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Equipo -->
    <section class="section" id="equipo">
        <div class="section-container">
            <div class="team-container">
                <h2>Nuestro Equipo</h2>
                <div class="team-grid">
                    <div class="team-card">
                        <div class="team-photo">
                            <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="CEO">
                        </div>
                        <h3>Carlos Méndez</h3>
                        <p>CEO & Fundador</p>
                        <p>15 años de experiencia en tecnología y liderazgo empresarial.</p>
                    </div>
                    <div class="team-card">
                        <div class="team-photo">
                            <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="CTO">
                        </div>
                        <h3>Ana Rodríguez</h3>
                        <p>Directora de Tecnología</p>
                        <p>Especialista en arquitecturas escalables y soluciones innovadoras.</p>
                    </div>
                    <div class="team-card">
                        <div class="team-photo">
                            <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Diseñadora">
                        </div>
                        <h3>Laura Fernández</h3>
                        <p>Directora de Diseño</p>
                        <p>Premiada diseñadora con enfoque en experiencias centradas en el usuario.</p>
                    </div>
                    <div class="team-card">
                        <div class="team-photo">
                            <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Desarrollador">
                        </div>
                        <h3>David López</h3>
                        <p>Lead Developer</p>
                        <p>Experto en JavaScript, React y arquitecturas de microservicios.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Contacto -->
    <section class="section" id="contacto">
        <div class="section-container">
            <div class="contact-container">
                <h2>Contáctanos</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <h3>Información de Contacto</h3>
                        <div class="contact-details">
                            <p><i class="fas fa-map-marker-alt"></i> Av. Innovación 123, Madrid, España</p>
                            <p><i class="fas fa-phone"></i> +34 912 345 678</p>
                            <p><i class="fas fa-envelope"></i> info@universodigital.com</p>
                            <p><i class="fas fa-clock"></i> Lunes a Viernes: 9:00 - 18:00</p>
                        </div>
                        <h3>Síguenos</h3>
                        <div class="social-links">
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-linkedin-in"></i></a>
                            <a href="#"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                    <div class="contact-form">
                        <form id="formContacto">
                            <input type="text" placeholder="Tu nombre completo" required>
                            <input type="email" placeholder="Tu correo electrónico" required>
                            <input type="text" placeholder="Asunto" required>
                            <textarea placeholder="Tu mensaje..." required></textarea>
                            <button type="submit" class="submit-btn">Enviar Mensaje <i class="fas fa-paper-plane"></i></button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>UniversoDigital</h3>
                <p>Transformamos ideas en realidades digitales. Creamos soluciones tecnológicas innovadoras que impulsan el crecimiento empresarial y mejoran la experiencia del usuario.</p>
            </div>
            <div class="footer-column">
                <h3>Enlaces Rápidos</h3>
                <ul class="footer-links">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Sobre Nosotros</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#equipo">Nuestro Equipo</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Servicios</h3>
                <ul class="footer-links">
                    <li><a href="#servicios">Desarrollo Web</a></li>
                    <li><a href="#servicios">Diseño UI/UX</a></li>
                    <li><a href="#servicios">Marketing Digital</a></li>
                    <li><a href="#servicios">Apps Móviles</a></li>
                    <li><a href="#servicios">Consultoría TI</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Suscríbete</h3>
                <p>Recibe las últimas noticias y tendencias tecnológicas directamente en tu correo.</p>
                <form class="subscribe-form">
                    <input type="email" placeholder="Tu correo electrónico" style="width:100%; padding:10px; margin-bottom:15px; border-radius:5px; border:none;">
                    <button type="submit" class="submit-btn" style="padding:10px 25px;">Suscribirse</button>
                </form>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 UniversoDigital. Todos los derechos reservados. | <a href="#" style="color:#6a11cb;">Política de Privacidad</a> | <a href="#" style="color:#6a11cb;">Términos de Servicio</a></p>
        </div>
    </footer>

    <script>
        // Menú móvil
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.querySelector('.nav-links').style.display = 
                document.querySelector('.nav-links').style.display === 'flex' ? 'none' : 'flex';
        });

        // Formulario de contacto
        document.getElementById('formContacto').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('¡Gracias por tu mensaje! Te contactaremos pronto.');
            this.reset();
        });

        // Efecto de aparición al hacer scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Aplicar observador a elementos
        document.querySelectorAll('.service-card, .team-card, .stat-item, .gallery-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            observer.observe(el);
        });

        // Cambiar estilo del nav al hacer scroll
        window.addEventListener('scroll', function() {
            const nav = document.querySelector('nav');
            if (window.scrollY > 100) {
                nav.style.background = 'rgba(20, 20, 40, 0.98)';
                nav.style.padding = '10px 0';
            } else {
                nav.style.background = 'rgba(20, 20, 40, 0.95)';
                nav.style.padding = '15px 0';
            }
        });

        // Contador animado para estadísticas
        function animateCounter(element, target, duration) {
            let start = 0;
            const increment = target / (duration / 16); // 60fps
            const timer = setInterval(() => {
                start += increment;
                if (start >= target) {
                    element.textContent = target + (element.textContent.includes('+') ? '+' : '');
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(start) + (element.textContent.includes('+') ? '+' : '');
                }
            }, 16);
        }

        // Iniciar contadores cuando la sección de estadísticas sea visible
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    document.querySelectorAll('.stat-item h3').forEach(stat => {
                        const text = stat.textContent;
                        const value = parseInt(text);
                        if (!isNaN(value)) {
                            stat.textContent = '0' + (text.includes('+') ? '+' : '');
                            setTimeout(() => animateCounter(stat, value, 2000), 300);
                        }
                    });
                    statsObserver.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });

        statsObserver.observe(document.querySelector('#estadisticas'));
    </script>
</body>
</html>
