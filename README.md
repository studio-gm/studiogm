<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>studiogm. | arquitectura + integral</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Syne:wght@400;700;800&display=swap');

        :root {
            --color-mision: #ece7e1;
            --color-servicios: #4a5441;
            --color-proyectos: #c4beb6;
            --color-consejos: #575556;
            --text-dark: #1a1a1a;
            --text-light: #f9f9f9;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            scroll-behavior: smooth;
            background-color: var(--color-mision);
        }

        .font-syne-brand {
            font-family: 'Syne', sans-serif;
            font-weight: 700;
            text-transform: lowercase;
        }

        .brand-m {
            font-size: 1.15em;
            display: inline-block;
            margin-left: -2px;
        }

        .brand-dot {
            color: #000;
            font-weight: 800;
            margin-left: 1px;
        }

        h1, h2, h3, .font-syne-title {
            font-family: 'Syne', sans-serif;
            text-transform: lowercase;
            letter-spacing: -0.02em;
        }

        .nav-link {
            position: relative;
            transition: color 0.3s;
            font-size: 0.75rem;
            letter-spacing: 0.25em;
            font-weight: 400;
            text-transform: lowercase;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 1px;
            bottom: -4px;
            left: 0;
            background-color: currentColor;
            transition: width 0.3s;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .img-container {
            overflow: hidden;
            clip-path: inset(0 0 0 0);
            transition: clip-path 0.5s ease;
        }

        .project-card:hover .img-container {
            clip-path: inset(10px 10px 10px 10px);
        }

        .hero-title {
            font-family: 'Montserrat', sans-serif;
            font-weight: 300;
            text-transform: lowercase;
            letter-spacing: -0.01em;
            color: #000;
        }

        .float-btn {
            position: fixed;
            right: 25px;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: white;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            z-index: 100;
            transition: transform 0.3s ease;
        }

        .float-btn:hover {
            transform: scale(1.1) rotate(5deg);
        }

        .whatsapp-float { bottom: 30px; background-color: #25d366; }
        .instagram-float { bottom: 95px; background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888); }
        .linkedin-float { bottom: 160px; background-color: #0077b5; }

        @media (max-width: 768px) {
            .float-btn { right: 20px; width: 50px; height: 50px; font-size: 22px; }
        }
    </style>
</head>
<body class="text-gray-900">

    <!-- Navegación -->
    <nav class="fixed w-full z-50 bg-white/90 backdrop-blur-md border-b border-gray-100">
        <div class="max-w-7xl mx-auto px-6 py-5 flex justify-between items-center">
            <div class="flex items-baseline text-2xl md:text-3xl cursor-pointer">
                studio<span class="font-syne-brand text-4xl md:text-5xl text-black mx-[1px]">g</span><span class="font-syne-brand brand-m text-3xl md:text-4xl text-black">m</span><span class="brand-dot text-2xl md:text-3xl">.</span>
            </div>
            
            <div class="hidden md:flex space-x-10 items-center">
                <a href="#inicio" class="nav-link">inicio</a>
                <a href="#proyectos" class="nav-link">proyectos</a>
                <a href="#servicios" class="nav-link">servicios</a>
                <a href="#contacto" class="nav-link">contacto</a>
                <div class="h-4 w-px bg-black/20 mx-2"></div>
                <div class="flex space-x-5">
                    <a href="https://www.instagram.com/arq.gustavomaidana/?hl=es" target="_blank" class="text-xl hover:text-pink-600 transition-colors">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="https://www.linkedin.com/in/arquitectogustavomaidana/" target="_blank" class="text-xl hover:text-blue-700 transition-colors">
                        <i class="fab fa-linkedin"></i>
                    </a>
                </div>
            </div>

            <button class="md:hidden text-3xl" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Menú Móvil -->
    <div id="mobileMenu" class="fixed inset-0 bg-white z-[60] flex-col items-center justify-center space-y-8 text-2xl hidden lowercase font-syne-title">
        <button class="absolute top-6 right-6 text-4xl" onclick="toggleMenu()">&times;</button>
        <a href="#inicio" onclick="toggleMenu()">inicio</a>
        <a href="#proyectos" onclick="toggleMenu()">proyectos</a>
        <a href="#servicios" onclick="toggleMenu()">servicios</a>
        <a href="#contacto" onclick="toggleMenu()">contacto</a>
    </div>

    <!-- Hero Section -->
    <section id="inicio" class="h-screen bg-[#ece7e1] flex items-center justify-center px-6">
        <div class="max-w-6xl text-center space-y-8">
            <div class="text-sm md:text-base tracking-[0.6em] flex items-center justify-center font-medium opacity-80">
                studio<span class="font-syne-brand text-xl md:text-2xl mx-1">g</span><span class="font-syne-brand brand-m text-lg md:text-xl">m</span><span class="brand-dot">.</span>
            </div>
            
            <h1 class="hero-title text-5xl md:text-7xl lg:text-9xl leading-none">
                arquitectura + integral
            </h1>
            
            <p class="text-xs md:text-sm max-w-xl mx-auto uppercase tracking-[0.4em] font-medium opacity-70">
                diseño que conecta con el bienestar
            </p>
            
            <div class="pt-10">
                <a href="#proyectos" class="inline-block border border-black text-black px-14 py-4 text-[10px] uppercase tracking-widest font-light hover:bg-black hover:text-white transition-all duration-500">
                    explorar proyectos
                </a>
            </div>
        </div>
    </section>

    <!-- Sección Proyectos -->
    <section id="proyectos" class="py-32 px-6 bg-[#c4beb6]">
        <div class="max-w-7xl mx-auto">
            <div class="mb-24 flex flex-col md:flex-row md:items-end justify-between gap-6">
                <div>
                    <h2 class="text-5xl md:text-7xl font-light mb-4">proyectos</h2>
                    <div class="h-px bg-black/20 w-32"></div>
                </div>
                <p class="text-[10px] uppercase tracking-[0.3em] max-w-xs opacity-60">Selección de obras recientes con enfoque en la funcionalidad y estética contemporánea.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-20">
                <div class="project-card group cursor-pointer">
                    <div class="img-container mb-8 aspect-[16/10]">
                        <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?q=80&w=2070&auto=format&fit=crop" alt="[Casa moderna con piscina]" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-1000">
                    </div>
                    <h3 class="text-2xl font-light">casa horizonte</h3>
                    <p class="text-[10px] uppercase tracking-widest mt-2 opacity-60 font-bold">Residencial / un solo nivel / 2024</p>
                </div>

                <div class="project-card group cursor-pointer md:mt-40">
                    <div class="img-container mb-8 aspect-[16/10]">
                        <img src="https://images.unsplash.com/photo-1613490493576-7fde63acd811?q=80&w=2071&auto=format&fit=crop" alt="[Arquitectura Contemporánea]" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-1000">
                    </div>
                    <h3 class="text-2xl font-light">estudio <span class="font-syne-brand">g</span><span class="font-syne-brand brand-m">m</span>.</h3>
                    <p class="text-[10px] uppercase tracking-widest mt-2 opacity-60 font-bold">Oficinas / Diseño argentino / 2023</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Servicios -->
    <section id="servicios" class="py-32 px-6 bg-[#4a5441] text-white">
        <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-24 items-center">
                <div class="space-y-16">
                    <h2 class="text-6xl md:text-8xl font-light text-white/90">servicios</h2>
                    <div class="grid gap-12">
                        <div class="border-l border-white/20 pl-8">
                            <span class="font-syne-brand text-3xl text-white/20 block mb-2">01</span>
                            <h4 class="text-xl font-light uppercase tracking-widest">proyecto integral</h4>
                            <p class="text-white/50 text-sm mt-4 leading-relaxed font-light">Gestión de arquitectura desde la concepción del plano hasta la dirección técnica final de obra.</p>
                        </div>
                        <div class="border-l border-white/20 pl-8">
                            <span class="font-syne-brand text-3xl text-white/20 block mb-2">02</span>
                            <h4 class="text-xl font-light uppercase tracking-widest">interiorismo</h4>
                            <p class="text-white/50 text-sm mt-4 leading-relaxed font-light">Curaduría de mobiliario, iluminación y materiales para crear espacios que transmitan calma.</p>
                        </div>
                    </div>
                </div>
                <div class="hidden lg:block">
                    <img src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?q=80&w=2070&auto=format&fit=crop" alt="[Detalle constructivo]" class="w-full aspect-[4/5] object-cover opacity-80">
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Contacto -->
    <section id="contacto" class="py-32 px-6 bg-[#ece7e1]">
        <div class="max-w-4xl mx-auto">
            <div class="text-center mb-20">
                <h2 class="text-5xl md:text-7xl font-light mb-6">contacto</h2>
                <div class="h-px bg-black/10 w-20 mx-auto mb-6"></div>
                <p class="text-[10px] uppercase tracking-[0.4em] font-bold">conectemos para tu próximo proyecto</p>
            </div>
            
            <form class="space-y-12" onsubmit="event.preventDefault(); showSuccess();">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                    <div class="space-y-2">
                        <label class="text-[9px] uppercase tracking-widest opacity-50">Nombre</label>
                        <input type="text" required class="w-full py-3 bg-transparent border-b border-black/20 outline-none focus:border-black transition-colors uppercase text-[10px] tracking-widest">
                    </div>
                    <div class="space-y-2">
                        <label class="text-[9px] uppercase tracking-widest opacity-50">Email</label>
                        <input type="email" required class="w-full py-3 bg-transparent border-b border-black/20 outline-none focus:border-black transition-colors uppercase text-[10px] tracking-widest">
                    </div>
                </div>
                <div class="space-y-2">
                    <label class="text-[9px] uppercase tracking-widest opacity-50">Mensaje</label>
                    <textarea rows="4" required class="w-full py-3 bg-transparent border-b border-black/20 outline-none focus:border-black transition-colors uppercase text-[10px] tracking-widest"></textarea>
                </div>
                
                <div class="text-center pt-8">
                    <button type="submit" class="bg-black text-white px-24 py-5 text-[10px] uppercase tracking-[0.4em] font-light hover:scale-105 transition-all duration-300">
                        enviar mensaje
                    </button>
                </div>
            </form>

            <div id="successMessage" class="hidden mt-12 p-8 bg-white/40 border border-black/5 text-center text-[10px] tracking-[0.3em] uppercase">
                mensaje enviado con éxito. responderemos a la brevedad.
            </div>
        </div>
    </section>

    <!-- Botones Flotantes -->
    <a href="https://www.linkedin.com/in/arquitectogustavomaidana/" class="float-btn linkedin-float" target="_blank" title="LinkedIn">
        <i class="fab fa-linkedin-in"></i>
    </a>
    <a href="https://www.instagram.com/arq.gustavomaidana/?hl=es" class="float-btn instagram-float" target="_blank" title="Instagram">
        <i class="fab fa-instagram"></i>
    </a>
    <a href="https://wa.me/5493765005083" class="float-btn whatsapp-float" target="_blank" title="WhatsApp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Footer -->
    <footer class="bg-[#ece7e1] border-t border-black/5 py-20 px-6 text-center">
        <div class="flex items-baseline text-3xl justify-center mb-10">
            studio<span class="font-syne-brand text-5xl text-black mx-[1px]">g</span><span class="font-syne-brand brand-m text-4xl text-black">m</span><span class="brand-dot">.</span>
        </div>
        
        <div class="flex flex-wrap justify-center gap-x-12 gap-y-6 text-[10px] uppercase tracking-[0.3em] mb-12">
            <a href="https://www.instagram.com/arq.gustavomaidana/?hl=es" target="_blank" class="hover:opacity-50 transition-opacity">instagram</a>
            <a href="https://www.linkedin.com/in/arquitectogustavomaidana/" target="_blank" class="hover:opacity-50 transition-opacity">linkedin</a>
            <a href="https://wa.me/5493765005083" target="_blank" class="hover:opacity-50 transition-opacity">whatsapp</a>
        </div>
        
        <div class="text-[9px] text-black opacity-40 uppercase tracking-[0.5em]">
            &copy; 2024 studio<span class="font-syne-brand">g</span><span class="font-syne-brand brand-m text-[8px]">m</span>. arquitectura integral
        </div>
    </footer>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
            menu.classList.toggle('flex');
        }

        function showSuccess() {
            const msg = document.getElementById('successMessage');
            msg.classList.remove('hidden');
            setTimeout(() => {
                msg.classList.add('hidden');
                document.querySelector('form').reset();
            }, 4000);
        }
    </script>
</body>
</html>
