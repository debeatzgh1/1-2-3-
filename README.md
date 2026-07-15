<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>welcome to- Dynamic Multi-Hub</title>
    <!-- Tailwind CSS for state-of-the-art styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Smooth transitions & custom scrollbar behavior */
        html { scroll-behavior: smooth; }
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #0b0f19; }
        ::-webkit-scrollbar-thumb { background: #1e1b4b; border-radius: 3px; }
        ::-webkit-scrollbar-thumb:hover { background: #4f46e5; }

        /* Custom glow pulsing and animations */
        @keyframes pulse-indigo {
            0%, 100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(99, 102, 241, 0.5); }
            50% { transform: scale(1.05); box-shadow: 0 0 12px 6px rgba(99, 102, 241, 0.2); }
        }
        .animate-premium-pulse {
            animation: pulse-indigo 2s infinite;
        }

        /* Hide-scroll utility for seamless carousels */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }

        /* Lazy loading fading system */
        .lazy-item {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .lazy-item.loaded {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen overflow-x-hidden font-sans">

    <!-- 1. SLIM FLOATING TOP BANNER (Opens URL externally without losing position) -->
    <div class="fixed top-0 left-0 w-full z-50 bg-indigo-950/80 backdrop-blur-md border-b border-indigo-500/20 py-2 px-4 flex justify-between items-center text-xs">
        <div class="flex items-center gap-2">
            <span class="h-2 w-2 rounded-full bg-emerald-500 animate-ping"></span>
            <span class="text-indigo-200 font-medium tracking-wide">DeBeatzGH Cloud Network Active</span>
        </div>
        <a href="https://debeatzgh1.github.io/-/" target="_blank" rel="noopener noreferrer" class="bg-indigo-600 hover:bg-indigo-500 text-white font-bold px-3 py-1 rounded transition-all duration-200 shadow-md">
            Launch Main Node &rarr;
        </a>
    </div>

    <!-- 2. SOCIALCREATOR MANDATORY SPLASH/OVERLAY (Closes instantly on Sidebar interaction) -->
    <div id="mandatory-splash" class="fixed inset-0 z-50 bg-slate-950 flex flex-col items-center justify-center p-6 transition-all duration-500">
        <div class="max-w-md w-full bg-slate-900 border border-indigo-500/30 rounded-2xl p-6 text-center shadow-2xl relative">
            <div class="w-16 h-16 bg-gradient-to-tr from-indigo-600 to-purple-600 rounded-2xl flex items-center justify-center mx-auto mb-4 animate-premium-pulse">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
            </div>
            <h2 class="text-xl font-bold mb-2">Welcome to faq Hub</h2>
            <p class="text-sm text-slate-400 mb-6">Initializing digital assets & application environments...</p>
            <div class="h-80 w-full rounded-lg overflow-hidden border border-slate-800 bg-black mb-4">
                <!-- Autoloading Socialcreator Application first -->
                <iframe src="https://debeatzgh1.github.io/-/" class="w-full h-full border-none"></iframe>
            </div>
            <button onclick="hideSplash()" class="w-full py-2.5 bg-indigo-600 hover:bg-indigo-500 font-bold rounded-lg transition-all">
                Enter Interface
            </button>
        </div>
    </div>

    <!-- 3. DETACHED FLOATING SIDEBAR MENU TRIGGER -->
    <button id="sidebar-trigger" onclick="toggleSidebar(); hideSplash()" class="fixed left-4 top-16 z-40 bg-indigo-600 hover:bg-indigo-500 text-white p-3.5 rounded-full shadow-lg shadow-indigo-600/30 transition-all duration-300 hover:rotate-90" aria-label="Toggle Navigation">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M4 6h16M4 12h16M4 18h16"/></svg>
    </button>

    <!-- 4. SLIDE-OUT OVERLAY NAVIGATION SIDEBAR -->
    <div id="nav-sidebar" class="fixed inset-y-0 left-0 z-40 w-80 bg-slate-900/95 backdrop-blur-lg border-r border-slate-800 shadow-2xl transform -translate-x-full transition-transform duration-300 flex flex-col justify-between pt-24 pb-6">
        <div class="px-6 overflow-y-auto flex-1 no-scrollbar">
            <h3 class="text-xs font-bold text-indigo-400 uppercase tracking-widest mb-4">Navigation Nodes</h3>
            <nav id="sidebar-nav-list" class="space-y-2">
                <!-- Programmatically populated for lightweight DOM rendering -->
            </nav>
        </div>
        <div class="px-6 pt-4 border-t border-slate-800 text-xs text-slate-500 text-center">
            &copy; 2026 DeBeatzGH Hub. All Assets Synced.
        </div>
    </div>

    <!-- MAIN PAGE CONTAINER -->
    <main class="pt-20 px-6 max-w-7xl mx-auto space-y-16 pb-24">
        
        <!-- HERO / SCROLL-TO-VIEW ENTRY -->
        <section class="lazy-item pt-12 text-center max-w-3xl mx-auto">
            <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight bg-gradient-to-r from-white via-indigo-200 to-purple-400 bg-clip-text text-transparent mb-6">
                DeBeatzGH Ecosystem
            </h1>
            <p class="text-slate-400 leading-relaxed md:text-lg">
                Your primary access terminal for bleeding-edge web applications, specialized AI chatbot instances, micro-SaaS blueprints, and high-performance frontend code architectures.
            </p>
        </section>

        <!-- 5. LOOK-AND-FEEL AUTO CAROUSEL SECTION -->
        <section class="lazy-item bg-slate-900/50 border border-slate-800 p-8 rounded-3xl relative overflow-hidden">
            <div class="flex items-center justify-between mb-6">
                <div>
                    <h2 class="text-xl font-bold tracking-tight text-white">Live Node Carousel</h2>
                    <p class="text-xs text-slate-400">Continuous background cycling of primary environments</p>
                </div>
                <div class="flex space-x-2">
                    <button onclick="scrollCarousel('left')" class="p-2 bg-slate-800 hover:bg-slate-700 rounded-lg text-white transition">&larr;</button>
                    <button onclick="scrollCarousel('right')" class="p-2 bg-slate-800 hover:bg-slate-700 rounded-lg text-white transition">&rarr;</button>
                </div>
            </div>
            
            <div id="carousel-viewport" class="flex gap-6 overflow-x-auto no-scrollbar scroll-smooth snap-x">
                <!-- Carousel slides dynamically loaded -->
            </div>
        </section>

        <!-- FAQ ACCORDION HUB -->
        <section class="lazy-item max-w-4xl mx-auto">
            <h2 class="text-2xl font-bold text-center mb-8">Ecosystem Knowledge Hub</h2>
            <div id="faq-accordion-container" class="space-y-4">
                <!-- Populated dynamically via config schema -->
            </div>
        </section>
    </main>

    <!-- 6. SMART DETACHED IFRAME/EXTERNAL TARGET MODAL -->
    <div id="iframe-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden items-center justify-center p-4">
        <div class="bg-slate-900 border border-slate-800 w-full max-w-5xl h-[85vh] rounded-2xl flex flex-col overflow-hidden shadow-2xl">
            <!-- Modal Header -->
            <div class="bg-slate-950 p-4 border-b border-slate-800 flex items-center justify-between">
                <div class="flex flex-col">
                    <h4 id="modal-title" class="font-bold text-white text-sm">Target Portal View</h4>
                    <span id="modal-url" class="text-xs text-indigo-400 truncate max-w-xs md:max-w-md"></span>
                </div>
                <div class="flex items-center gap-2">
                    <a id="modal-external-link" href="#" target="_blank" rel="noopener noreferrer" class="bg-slate-800 hover:bg-slate-700 text-xs px-3 py-1.5 rounded-lg flex items-center gap-1 transition">
                        Open External
                        <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                    </a>
                    <button onclick="closeModal()" class="text-slate-400 hover:text-white p-1 rounded-lg hover:bg-slate-800 transition">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
                    </button>
                </div>
            </div>
            <!-- Frame Body -->
            <div class="flex-1 bg-black relative">
                <iframe id="modal-iframe" src="" class="w-full h-full border-none" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture"></iframe>
            </div>
        </div>
    </div>

    <!-- CORE CONFIGURATION ENGINE -->
    <script>
        // Directory config payload (URLs, Metadata, FAQ Content)
        const nodeDirectory = [
            {
                id: "node1",
                title: "Premium Client Intake Portal",
                url: "https://debeatzgh1.github.io/1/",
                description: "Direct request collection interface with high-performance formatting rules.",
                faq: "How do I submit design requests? Utilize the built-in request fields to auto-compile details and initiate design structures directly.",
                icon: "M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
            },
            {
                id: "node2",
                title: "Custom AI-Chat Engine",
                url: "https://debeatzgh1.github.io/ai-chat/",
                description: "Context-aware AI dialogue layer configured specifically for interactive tech consultations.",
                faq: "Can I host this on Blogger? Yes. The AI assistant can be safely integrated into any standard sidebar or gadget section easily.",
                icon: "M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"
            },
            {
                id: "node3",
                title: "Content & Blog Stream",
                url: "https://debeatzgh1.github.io/posts/",
                description: "Premium technical article compilation for modern digital system operators.",
                faq: "Is the RSS feed auto-updating? Yes, the underlying service automatically gathers system posts via active standard protocols.",
                icon: "M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"
            },
            {
                id: "node4",
                title: "Personal Portfolio Interface",
                url: "https://debeatzgh1.github.io/Personal-Portfolio-site-/",
                description: "The live design showcase for DeBeatzGH engineering achievements.",
                faq: "Are layouts optimized for mobile devices? Every design is built fully using mobile-first responsive grid architectures.",
                icon: "M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
            },
            {
                id: "node5",
                title: "Collaborators Central Hub",
                url: "https://debeatzgh1.github.io/Debeatzgh-Collaborators-Hub/",
                description: "Unified workspace dashboard managing development tasks and team deliverables.",
                faq: "How do I request collaborative credentials? Use the contact systems inside the app or the main TechShop message drawer.",
                icon: "M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
            },
            {
                id: "node6",
                title: "Decode AI Starter Kit",
                url: "https://debeatzgh1.github.io/Decode-AI-starter-kit-/",
                description: "Introductory developer stack for setting up and debugging custom language processing APIs.",
                faq: "What model configurations are included? Templates for lightweight API integrations and structural system prompts are bundled.",
                icon: "M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"
            },
            {
                id: "node7",
                title: "Ultimate Side Hustle Guide",
                url: "https://debeatzgh1.github.io/The-Ultimate-Guide-to-Side-Hustle/",
                description: "Monetization plans and business architectures ready for execution.",
                faq: "Are update materials free? All successive publications inside our platform are completely free for active community hub members.",
                icon: "M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"
            },
            {
                id: "node8",
                title: "Firebase Component Engine",
                url: "https://debeatzgh1.github.io/firebase-front-end-components/",
                description: "Reusable frontend modules tailored specifically for quick Firebase integration layers.",
                faq: "Do these support real-time database channels? Absolutely, components are pre-configured to process active snapshot listeners natively.",
                icon: "M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4"
            },
            {
                id: "node9",
                title: "Optimized Sales Funnels",
                url: "https://debeatzgh1.github.io/sales/",
                description: "Interactive sales structures designed to boost conversions.",
                faq: "Can I customize the payment methods? Yes, the front-end layout can interface seamlessly with Stripe, PayPal, or specialized local payment APIs.",
                icon: "M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
            },
            {
                id: "node10",
                title: "Primary Digital Contact Terminal",
                url: "https://debeatzgh1.github.io/me-/",
                description: "Direct contact card and service catalog interface.",
                faq: "What is the typical response time? Direct developer requests are processed within 24-48 business hours.",
                icon: "M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
            },
            {
                id: "node11",
                title: "Official Brand Workspace",
                url: "https://debeatzgh1.github.io/debeatzgh/",
                description: "The core platform ecosystem for managing custom systems.",
                faq: "Can I request white-label versions? Yes, custom white-label solutions can be requested directly inside our communications channels.",
                icon: "M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
            },
            {
                id: "node12",
                title: "Side-Hustle Starter Kit",
                url: "https://debeatzgh1.github.io/Side-hustle-starter-kit-/",
                description: "A clean launch kit featuring templates and marketing material configurations.",
                faq: "Do these require programming knowledge? These are built to be copy-paste ready for Blogger and simple static hosting sites.",
                icon: "M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"
            },
            {
                id: "node13",
                title: "Online Business Framework",
                url: "https://debeatzgh1.github.io/Online-business-kit/",
                description: "Interactive planning guides designed to map out new digital products.",
                faq: "How do I download the configuration files? The kit links directly to raw setup scripts on GitHub.",
                icon: "M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
            },
            {
                id: "node14",
                title: "Modern TailwindCSS Homepage",
                url: "https://debeatzgh1.github.io/Modern-homepage-styling-with-TailwindCSS-/",
                description: "Lightweight single-page homepage styled for high performance and visual appeal.",
                faq: "Is this customizable? Yes, the classes are modular and built natively for rapid modification.",
                icon: "M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
            },
            {
                id: "node15",
                title: "Interactive Menu Widget",
                url: "https://debeatzgh1.github.io/menu-widget-/",
                description: "A compact floating widget built for multi-link redirection panels.",
                faq: "Can I use this widget in Blogger sidebars? Yes, paste the compiled script into an HTML/JavaScript gadget.",
                icon: "M4 6h16M4 12h8m-8 6h16"
            },
            {
                id: "node16",
                title: "MB Online Ecosystem",
                url: "https://debeatzgh1.github.io/MB--online-/",
                description: "An interactive portfolio and services platform designed for creators.",
                faq: "Is this system open-source? Yes, visit the project page for the raw repository and styling guides.",
                icon: "M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"
            },
            {
                id: "node17",
                title: "Popup HTML Page Generator",
                url: "https://debeatzgh1.github.io/popup-html-page-generator-blogger/",
                description: "A simple visual builder used to design modal and popup sequences for Blogger.",
                faq: "Does it require external hosting? No, the generator compiles raw inline components that can be pasted directly into Blogger.",
                icon: "M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"
            },
            {
                id: "node18",
                title: "Floating Dock & Smart Modal",
                url: "https://debeatzgh1.github.io/-Floating-Dock-Smart-Iframe-Modal/#",
                description: "A system-wide floating navigation dock that renders content inside clean overlays.",
                faq: "Is it touch-friendly? Yes, the UI is optimized for swipe and drag actions on mobile displays.",
                icon: "M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4"
            }
        ];

        // 1. Splash Screen Control (Dismisses automatically on Sidebar activity)
        function hideSplash() {
            const splash = document.getElementById('mandatory-splash');
            if (splash) {
                splash.classList.add('opacity-0', 'pointer-events-none');
                setTimeout(() => splash.style.display = 'none', 500);
            }
        }

        // 2. Sidebar Navigation Control
        function toggleSidebar() {
            const sidebar = document.getElementById('nav-sidebar');
            sidebar.classList.toggle('-translate-x-full');
        }

        // 3. Modal / Iframe View System
        function openPortal(title, url, mode) {
            if (mode === 'external') {
                window.open(url, '_blank', 'noopener,noreferrer');
            } else {
                const modal = document.getElementById('iframe-modal');
                const iframe = document.getElementById('modal-iframe');
                const modalTitle = document.getElementById('modal-title');
                const modalUrl = document.getElementById('modal-url');
                const externalLink = document.getElementById('modal-external-link');

                modalTitle.textContent = title;
                modalUrl.textContent = url;
                externalLink.href = url;
                iframe.src = url;

                modal.classList.remove('hidden');
                modal.classList.add('flex');
            }
        }

        function closeModal() {
            const modal = document.getElementById('iframe-modal');
            const iframe = document.getElementById('modal-iframe');
            iframe.src = ""; // Stop audio/video playing in background
            modal.classList.remove('flex');
            modal.classList.add('hidden');
        }

        // 4. Accordion Actions
        function toggleAccordion(button) {
            const panel = button.nextElementSibling;
            const icon = button.querySelector('svg');
            panel.classList.toggle('hidden');
            icon.classList.toggle('rotate-180');
        }

        // 5. Build components dynamically from the config schema
        function initializeEcosystem() {
            const navContainer = document.getElementById('sidebar-nav-list');
            const carouselContainer = document.getElementById('carousel-viewport');
            const faqContainer = document.getElementById('faq-accordion-container');

            nodeDirectory.forEach((node, index) => {
                // Generate Sidebar Nodes
                const navItem = document.createElement('div');
                navItem.className = "p-3 bg-slate-950/40 rounded-xl border border-slate-800 hover:border-indigo-500/30 transition duration-200";
                navItem.innerHTML = `
                    <div class="flex items-start gap-3">
                        <div class="p-2 bg-indigo-950 rounded-lg text-indigo-400">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="${node.icon}"/></svg>
                        </div>
                        <div class="flex-1 min-w-0">
                            <h4 class="text-xs font-semibold text-white truncate">${node.title}</h4>
                            <p class="text-[10px] text-slate-400 truncate mb-2">${node.description}</p>
                            <div class="flex gap-2">
                                <button onclick="openPortal('${node.title}', '${node.url}', 'iframe'); toggleSidebar()" class="text-[10px] bg-indigo-600/20 hover:bg-indigo-600 text-indigo-300 hover:text-white px-2 py-1 rounded transition">Iframe</button>
                                <button onclick="openPortal('${node.title}', '${node.url}', 'external'); toggleSidebar()" class="text-[10px] bg-slate-800 hover:bg-slate-700 text-slate-300 px-2 py-1 rounded transition">External</button>
                            </div>
                        </div>
                    </div>
                `;
                navContainer.appendChild(navItem);

                // Generate Look-and-Feel Carousel Elements
                const carouselCard = document.createElement('div');
                carouselCard.className = "min-w-[280px] md:min-w-[320px] bg-slate-950 border border-slate-800 rounded-2xl p-5 flex flex-col justify-between snap-start hover:border-indigo-500/40 transition duration-300";
                carouselCard.innerHTML = `
                    <div>
                        <div class="w-10 h-10 bg-indigo-950 rounded-lg flex items-center justify-center text-indigo-400 mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="${node.icon}"/></svg>
                        </div>
                        <h3 class="font-bold text-sm mb-1 truncate text-white">${node.title}</h3>
                        <p class="text-xs text-slate-400 line-clamp-2 mb-4">${node.description}</p>
                    </div>
                    <div class="flex items-center justify-between border-t border-slate-800/60 pt-4">
                        <button onclick="openPortal('${node.title}', '${node.url}', 'iframe')" class="text-xs font-semibold text-indigo-400 hover:text-indigo-300">Inline Open &rarr;</button>
                        <button onclick="openPortal('${node.title}', '${node.url}', 'external')" class="text-xs text-slate-500 hover:text-slate-400">External</button>
                    </div>
                `;
                carouselContainer.appendChild(carouselCard);

                // Generate FAQ Accordions
                const faqItem = document.createElement('div');
                faqItem.className = "bg-slate-900 border border-slate-800 rounded-xl overflow-hidden";
                faqItem.innerHTML = `
                    <button onclick="toggleAccordion(this)" class="w-full flex justify-between items-center p-5 text-left font-medium text-slate-200 hover:bg-slate-800/40 transition">
                        <span class="text-sm md:text-base">${node.title} — FAQ</span>
                        <svg class="w-5 h-5 text-slate-500 transform transition-transform duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/></svg>
                    </button>
                    <div class="hidden p-5 text-xs md:text-sm text-slate-400 border-t border-slate-800/60 bg-slate-950/20">
                        ${node.faq}
                    </div>
                `;
                faqContainer.appendChild(faqItem);
            });

            // Initialize Intersection Observer for Scroll-To-View animations
            initLazyLoading();
        }

        // 6. Carousel Manual Scroll Controls
        function scrollCarousel(direction) {
            const viewport = document.getElementById('carousel-viewport');
            const offset = direction === 'left' ? -300 : 300;
            viewport.scrollBy({ left: offset, behavior: 'smooth' });
        }

        // 7. Auto Carousel Cycling Engine
        let autoScrollInterval;
        function startAutoScroll() {
            const viewport = document.getElementById('carousel-viewport');
            autoScrollInterval = setInterval(() => {
                if (viewport.scrollLeft + viewport.clientWidth >= viewport.scrollWidth - 5) {
                    viewport.scrollTo({ left: 0, behavior: 'smooth' });
                } else {
                    viewport.scrollBy({ left: 300, behavior: 'smooth' });
                }
            }, 4000); // Cycles every 4 seconds
        }

        function stopAutoScroll() {
            clearInterval(autoScrollInterval);
        }

        // 8. Intersection Observer lazy load configuration
        function initLazyLoading() {
            const items = document.querySelectorAll('.lazy-item');
            const observer = new IntersectionObserver((entries, obs) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('loaded');
                        obs.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });

            items.forEach(item => observer.observe(item));
        }

        // Init App on boot
        window.addEventListener('DOMContentLoaded', () => {
            initializeEcosystem();
            startAutoScroll();

            // Pause auto-scroll on carousel interaction for a premium user experience
            const carousel = document.getElementById('carousel-viewport');
            carousel.addEventListener('mouseenter', stopAutoScroll);
            carousel.addEventListener('mouseleave', startAutoScroll);
            carousel.addEventListener('touchstart', stopAutoScroll);
        });
    </script>
</body>
</html>
