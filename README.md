<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yenny Caraballo - Psicología, Tanatología y Espiritualidad</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #2c3e50;
            background: #f0f8ff;
        }

        header {
            background: white;
            color: #2c3e50;
            padding: 1.5rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 120px;
            width: auto;
            max-width: 100%;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: #81d4fa;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
            font-size: 1.1rem;
        }

        .nav-links a:hover {
            color: #4fc3f7;
        }

        .hero {
            background: linear-gradient(135deg, #e1f5fe 0%, #b3e5fc 100%);
            color: #01579b;
            padding: 4rem 2rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.8;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 3rem 2rem;
        }

        .section {
            background: white;
            margin-bottom: 2rem;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .section:hover {
            transform: translateY(-5px);
        }

        h2 {
            color: #81d4fa;
            margin-bottom: 1.5rem;
            font-size: 2rem;
            border-bottom: 3px solid #b3e5fc;
            padding-bottom: 0.5rem;
        }

        h3 {
            color: #4fc3f7;
            margin: 1.5rem 0 1rem;
            font-size: 1.5rem;
        }

        .education-list, .services-list {
            list-style: none;
            padding-left: 0;
        }

        .education-list li, .services-list li {
            padding: 0.8rem 0;
            padding-left: 2rem;
            position: relative;
        }

        .education-list li:before, .services-list li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #81d4fa;
            font-weight: bold;
            font-size: 1.2rem;
        }

        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .value-card {
            background: linear-gradient(135deg, #f1f8ff 0%, #e3f2fd 100%);
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s;
        }

        .value-card:hover {
            transform: scale(1.05);
        }

        .value-card h4 {
            color: #4fc3f7;
            margin-bottom: 0.5rem;
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .course-card {
            background: linear-gradient(135deg, #f1f8ff 0%, #e3f2fd 100%);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .course-card:hover {
            transform: translateY(-8px);
        }

        .course-card h4 {
            color: #4fc3f7;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .course-details {
            color: #546e7a;
            margin: 0.5rem 0;
        }

        .price {
            font-size: 1.5rem;
            color: #81d4fa;
            font-weight: bold;
            margin-top: 1rem;
        }

        .contact-info {
            background: linear-gradient(135deg, #b3e5fc 0%, #81d4fa 100%);
            color: #01579b;
            padding: 3rem 2rem;
            text-align: center;
            margin-top: 3rem;
            border-radius: 15px;
        }

        .contact-info h2 {
            color: #01579b;
            border-bottom: 3px solid #01579b;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .contact-item {
            background: rgba(255,255,255,0.3);
            padding: 1.5rem;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .contact-item h4 {
            margin-bottom: 0.5rem;
            color: #01579b;
        }

        footer {
            background: #4fc3f7;
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        .cta-button {
            display: inline-block;
            background: #81d4fa;
            color: #01579b;
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            margin: 0.5rem;
            transition: all 0.3s;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .cta-button:hover {
            background: #4fc3f7;
            color: white;
            transform: scale(1.05);
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background: #81d4fa;
            border-radius: 3px;
            transition: 0.3s;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: white;
                flex-direction: column;
                padding: 2rem;
                box-shadow: 0 4px 6px rgba(0,0,0,0.1);
                gap: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .logo img {
                height: 80px;
            }

            nav {
                padding: 0 1rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .section {
                padding: 1.5rem;
            }

            .courses-grid {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .logo img {
                height: 60px;
            }

            .hero h1 {
                font-size: 1.5rem;
            }

            .hero p {
                font-size: 1rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            .section {
                padding: 1rem;
            }

            .value-card, .course-card {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">
                <img src="https://i.imgur.com/bZO565p.jpeg" alt="Yenny Caraballo - Abogada, Psicóloga Clínica y Tanatología">
            </div>
            <div class="menu-toggle" onclick="toggleMenu()">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#sobre-mi" onclick="closeMenu()">Sobre Mí</a></li>
                <li><a href="#servicios" onclick="closeMenu()">Servicios</a></li>
                <li><a href="#cursos" onclick="closeMenu()">Cursos</a></li>
                <li><a href="#contacto" onclick="closeMenu()">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <div class="hero">
        <h1>Sanación Integral del Alma</h1>
        <p>Acompañamiento psicológico, espiritual y tanatológico con más de 20 años de experiencia</p>
    </div>

    <div class="container">
        <section id="sobre-mi" class="section">
            <h2>Sobre Mí</h2>
            <div style="display: flex; gap: 2rem; align-items: center; flex-wrap: wrap;">
                <img src="https://i.imgur.com/Uff1n9m.png" alt="Yenny Caraballo - Psicóloga Clínica y Tanatóloga" style="width: 300px; height: 300px; object-fit: cover; border-radius: 15px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
                <div style="flex: 1; min-width: 300px;">
                    <p>Soy una canalizadora de nacimiento con el don innato de leer el alma. He practicado la mediumnidad por más de 20 años a nivel nacional e internacional, perfeccionando este hermoso don con dedicación y disciplina.</p>
                    <p>Originaria de la República Dominicana, mi pasión por el conocimiento del mundo espiritual se entrelaza con una sólida formación académica que me permite ofrecer un enfoque integral y compasivo.</p>
                </div>
            </div>
            
            <h3>Formación Académica</h3>
            <ul class="education-list">
                <li>Abogada, Especialista en Sucesión y Partición</li>
                <li>Psicóloga Mención Clínica</li>
                <li>Tanatóloga Certificada por el Instituto Tanatológico de México en conjunto con la UNAM</li>
                <li>Psicología Holística</li>
                <li>Certificada por UNWOMEN ONU en temas de Género y Violencia Intrafamiliar</li>
                <li>Conferencista y Escritora de temas espirituales</li>
            </ul>
        </section>

        <section class="section">
            <h2>Misión, Visión y Valores</h2>
            <h3>Misión</h3>
            <p>Brindamos atención psicológica, espiritual y tanatológica integral para ayudar a las personas a superar dificultades emocionales y encontrar consuelo tras la pérdida de un ser querido.</p>
            
            <h3>Visión</h3>
            <p>Nos esforzamos por abordar de manera holística los aspectos psicológicos, espirituales y emocionales de nuestros usuarios, especialmente durante momentos difíciles como la pérdida, la enfermedad o la ruptura amorosa.</p>
            
            <h3>Valores</h3>
            <div class="values-grid">
                <div class="value-card">
                    <h4>Empatía</h4>
                    <p>Comprendemos profundamente tus emociones</p>
                </div>
                <div class="value-card">
                    <h4>Respeto</h4>
                    <p>Honramos tu proceso individual</p>
                </div>
                <div class="value-card">
                    <h4>Confidencialidad</h4>
                    <p>Tu privacidad es sagrada</p>
                </div>
                <div class="value-card">
                    <h4>Compromiso</h4>
                    <p>Dedicados a tu sanación</p>
                </div>
                <div class="value-card">
                    <h4>Autonomía</h4>
                    <p>Te empoderamos en tu proceso</p>
                </div>
                <div class="value-card">
                    <h4>Solidaridad</h4>
                    <p>Contigo en cada paso</p>
                </div>
            </div>
        </section>

        <section id="servicios" class="section">
            <h2>Servicios</h2>
            
            <h3>Servicios de Psicología</h3>
            <ul class="services-list">
                <li>Terapia de duelo individual</li>
                <li>Terapia de grupo de duelo</li>
                <li>Terapia familiar</li>
                <li>Intervención en crisis</li>
                <li>Orientación espiritual</li>
                <li>Consultoría organizacional</li>
            </ul>

            <h3>Servicios de Tanatología y Espiritualidad</h3>
            <p><strong>El duelo puede ser por:</strong> Pérdida de un ser querido, pérdida de una relación, pérdida de la salud, pérdida de empleo, pérdida de la seguridad, pérdida de sueños o expectativas.</p>
            <ul class="services-list">
                <li>Acompañamiento durante el proceso de duelo</li>
                <li>Asesoramiento en enfermedades terminales</li>
                <li>Preparación para la muerte</li>
                <li>Asesoramiento en cuidados paliativos</li>
                <li>Terapia de grupo para el duelo</li>
                <li>Asesoramiento en planificación funeraria</li>
                <li>Rituales y ceremonias de despedida</li>
                <li>Educación sobre el duelo</li>
            </ul>

            <h3>Servicios de Conferencias</h3>
            <ul class="services-list">
                <li>Conferencias Magistrales</li>
                <li>Seminarios y Talleres</li>
                <li>Capacitaciones Corporativas</li>
                <li>Eventos Académicos</li>
                <li>Charlas en Instituciones Educativas</li>
                <li>Programas de Desarrollo Personal</li>
                <li>Conferencias Virtuales o Webinars</li>
                <li>Charlas de Sensibilización y Prevención</li>
            </ul>
        </section>

        <section class="section">
            <h2>Programa SANAR</h2>
            <p>Sanar es un proceso fundamental para el bienestar integral. Comprometerse con la sanación ofrece múltiples beneficios:</p>
            <ul class="services-list">
                <li><strong>Bienestar emocional:</strong> Liberar emociones reprimidas y encontrar paz interior</li>
                <li><strong>Mejora en las relaciones:</strong> Resolver conflictos internos para relaciones más saludables</li>
                <li><strong>Crecimiento personal:</strong> Evolucionar hacia tu mejor versión</li>
                <li><strong>Salud física:</strong> Reducir el estrés y mejorar la salud general</li>
                <li><strong>Empoderamiento:</strong> Desarrollar autoconciencia, autoaceptación y autoestima</li>
            </ul>
            <p style="text-align: center; margin-top: 2rem; font-size: 1.2rem; color: #4fc3f7;"><strong>Pregunta por nuestros planes compartidos e individuales</strong></p>
        </section>

        <section id="cursos" class="section">
            <h2>Cursos en Vivo</h2>
            <div class="courses-grid">
                <div class="course-card">
                    <h4>Cómo Dejar de Sentirte Culpable</h4>
                    <p>Con ejercicios y terapia de liberación</p>
                    <p class="course-details">⏱️ 4 semanas - 1 día a la semana</p>
                    <p class="price">$200.00</p>
                </div>

                <div class="course-card">
                    <h4>Superando el Duelo</h4>
                    <p>Aprende a sanar las heridas que produce el duelo y siéntete escuchado. Te damos técnicas y herramientas para tu diario vivir.</p>
                    <p class="course-details">⏱️ 4 semanas - 1 día a la semana</p>
                    <p class="price">$200.00</p>
                </div>

                <div class="course-card">
                    <h4>Misión y Propósito</h4>
                    <p>Lograrás trascender y tener la vida que quieres. Identificando cuál es tu misión y propósito.</p>
                    <p class="course-details">⏱️ 4 semanas - 1 día a la semana</p>
                    <p class="price">$200.00</p>
                </div>

                <div class="course-card">
                    <h4>Sanando la Ansiedad</h4>
                    <p>Te damos las herramientas para sanar y aprender a liberarte de la ansiedad.</p>
                    <p class="course-details">⏱️ 4 semanas - 1 día a la semana</p>
                    <p class="price">$200.00</p>
                </div>

                <div class="course-card">
                    <h4>Relaciones Sanas</h4>
                    <p>Obtendrás la relación que deseas. Te damos las claves esenciales para que tus relaciones se vuelvan sanas y duraderas.</p>
                    <p class="course-details">⏱️ 4 semanas - 1 día a la semana</p>
                    <p class="price">$200.00</p>
                </div>
            </div>
            <p style="text-align: center; margin-top: 2rem; font-size: 1.1rem; font-style: italic;">Permítenos ayudarte a sanar desde el alma y liberarte de esa carga que has llevado por años.</p>
        </section>

        <section id="contacto" class="contact-info">
            <h2 style="color: #01579b; border-bottom: 3px solid #01579b;">¡Tu próximo paso hacia el éxito comienza aquí!</h2>
            <p style="font-size: 1.2rem; margin: 1rem 0;">Contáctame ahora</p>
            
            <div class="contact-grid">
                <div class="contact-item">
                    <h4>📱 WhatsApp</h4>
                    <p>849-378-4503</p>
                </div>
                <div class="contact-item">
                    <h4>☎️ Teléfono</h4>
                    <p>809-746-5966</p>
                </div>
                <div class="contact-item">
                    <h4>✉️ Email</h4>
                    <p>yennycaraballo13@gmail.com</p>
                </div>
                <div class="contact-item">
                    <h4>📍 Dirección</h4>
                    <p>Calle República de Argentina, Plaza Pujols, Suite 204<br>Santiago, Rep. Dom.</p>
                </div>
            </div>

            <div style="margin-top: 2rem;">
                <h4>💳 Métodos de Pago</h4>
                <p>PayPal: yennycaraballo13@gmail.com</p>
                <p>Banco Popular: 746372150</p>
                <p>Banco de Reservas: 9603803085</p>
            </div>

            <div style="margin-top: 2rem;">
                <h4>🌐 Sígueme en Redes Sociales</h4>
                <p>Instagram | YouTube | TikTok | LinkedIn: @yennycaraballoa</p>
            </div>

            <div style="margin-top: 2rem;">
                <a href="https://wa.me/18493784503" class="cta-button">📱 Agendar Consulta por WhatsApp</a>
                <a href="tel:+18097465966" class="cta-button" style="background: #4fc3f7; color: white;">☎️ Llamar Ahora</a>
                <a href="mailto:yennycaraballo13@gmail.com" class="cta-button" style="background: white; color: #4fc3f7;">✉️ Enviar Email</a>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Yenny Caraballo. Todos los derechos reservados.</p>
        <p>Psicología | Tanatología | Espiritualidad</p>
        <p style="margin-top: 1rem; font-size: 0.9rem;">Servicios profesionales y personalizados con más de 20 años de experiencia</p>
    </footer>

    <script>
        function toggleMenu() {
            const navLinks = document.getElementById('navLinks');
            navLinks.classList.toggle('active');
        }

        function closeMenu() {
            const navLinks = document.getElementById('navLinks');
            navLinks.classList.remove('active');
        }

        document.addEventListener('click', function(event) {
            const nav = document.querySelector('nav');
            const navLinks = document.getElementById('navLinks');
            if (!nav.contains(event.target)) {
                navLinks.classList.remove('active');
            }
        });
    </script>
</body>
</html>
