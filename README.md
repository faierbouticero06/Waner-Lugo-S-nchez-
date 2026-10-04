# Waner-Lugo-S-nchez-
Sitio wed para comprar Ebooks, secciones privadas con psicólogos, y asesoría 
```html
<!DOCTYPE html>
<html lang="es" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE BROTHERHOOD | Waner Lugo Sánchez</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        darkBg: '#09090b',
                        cardBg: '#121215',
                        brandRed: '#dc2626',
                        brandRedHover: '#b91c1c',
                        accentBorder: '#27272a',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons & Google Fonts -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #09090b;
            color: #ffffff;
            overflow-x: hidden;
        }
        .hero-title {
            font-weight: 900;
            line-height: 0.90;
            letter-spacing: -0.04em;
        }
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #09090b;
        }
        ::-webkit-scrollbar-thumb {
            background: #27272a;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #dc2626;
        }
    </style>
</head>
<body class="bg-darkBg text-white antialiased selection:bg-brandRed selection:text-white">

    <!-- Top Announcement Bar -->
    <div class="bg-brandRed text-white text-xs md:text-sm font-black py-2.5 px-4 text-center tracking-wider uppercase shadow-lg flex items-center justify-center space-x-2">
        <span>🔥 DIPLOMA & DERECHOS INCLUIDOS · 40% OFF CÓDIGO <span class="bg-black text-white px-2 py-0.5 rounded ml-1 font-mono">BROTHERHOOD40</span> 🔥</span>
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 bg-darkBg/90 backdrop-blur-md border-b border-accentBorder">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Brand Logo & Owner Info -->
            <a href="#" class="group flex flex-col">
                <span class="text-2xl sm:text-3xl font-black tracking-widest uppercase text-white group-hover:text-brandRed transition-colors">THE BROTHERHOOD</span>
                <span class="text-[10px] sm:text-xs font-semibold tracking-widest text-gray-400 -mt-1 uppercase">
                    FUNDADO POR <span class="text-brandRed font-bold">WANER LUGO SÁNCHEZ</span>
                </span>
            </a>

            <!-- Nav Links & Admin Button -->
            <div class="flex items-center space-x-3 sm:space-x-6">
                <button onclick="toggleAdminModal(true)" class="bg-neutral-900 border border-brandRed/40 text-brandRed hover:bg-brandRed hover:text-white font-extrabold px-3 py-2 sm:px-4 sm:py-2.5 rounded-xl transition-all text-xs uppercase tracking-wider flex items-center space-x-2 shadow-lg">
                    <i class="fa-solid fa-lock text-xs"></i>
                    <span class="hidden sm:inline">PANEL DE CONTROL</span>
                    <span class="sm:hidden">ADMIN</span>
                </button>

                <!-- Cart Button -->
                <button id="cartBtn" onclick="toggleCart(true)" class="relative bg-white text-black font-extrabold px-4 py-2.5 sm:px-5 sm:py-2.5 rounded-xl hover:bg-gray-200 transition-all transform active:scale-95 flex items-center space-x-2 shadow-lg">
                    <i class="fa-solid fa-bag-shopping text-sm text-brandRed"></i>
                    <span class="tracking-wider text-xs sm:text-sm">CARRITO <span id="cartCountBadge" class="ml-1 bg-brandRed text-white px-2 py-0.5 rounded-full text-xs">0</span></span>
                </button>
            </div>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="relative min-h-[75vh] flex items-center justify-center px-4 sm:px-6 lg:px-8 py-16 border-b border-accentBorder overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-b from-brandRed/10 via-darkBg to-darkBg pointer-events-none"></div>
            <div class="absolute -top-32 -right-32 w-96 h-96 bg-brandRed/20 rounded-full blur-3xl pointer-events-none"></div>

            <div class="relative max-w-4xl mx-auto text-left w-full">
                <div class="inline-block mb-6">
                    <span class="border border-brandRed/40 bg-neutral-900/90 text-brandRed text-xs sm:text-sm font-black uppercase tracking-widest px-4 py-2 rounded-full shadow-inner">
                        <i class="fa-solid fa-book-bookmark mr-1"></i> LIBROS DIGITALES & ASESORÍAS DIRECTAS
                    </span>
                </div>

                <h1 class="hero-title text-5xl sm:text-7xl lg:text-9xl uppercase text-white mb-6 tracking-tight">
                    DOMINIO Y<br><span class="text-brandRed">PODER REAL.</span>
                </h1>

                <p class="text-gray-300 text-lg sm:text-xl font-normal max-w-2xl mb-8 leading-relaxed">
                    Accede a la colección exclusiva de libros en formato PDF y agenda sesiones privadas con <strong class="text-white">Waner Lugo Sánchez</strong> para transformar tu mentalidad y estrategia.
                </p>

                <!-- Contact Badge -->
                <div class="inline-flex items-center space-x-3 bg-neutral-900/80 border border-neutral-800 p-3 rounded-xl mb-10">
                    <i class="fa-solid fa-envelope text-brandRed"></i>
                    <span class="text-xs sm:text-sm font-mono text-gray-300">WANERLUGOSANCHEZ203@GMAIL.COM</span>
                </div>

                <div class="flex flex-col sm:flex-row gap-4">
                    <a href="#catalogo" class="text-center bg-brandRed hover:bg-brandRedHover text-white font-black px-8 py-4 rounded-xl transition-all text-xs uppercase tracking-widest shadow-xl transform hover:-translate-y-0.5">
                        EXPLORAR CATÁLOGO
                    </a>
                    <a href="mailto:WANERLUGOSANCHEZ203@GMAIL.COM" class="text-center border border-neutral-700 hover:border-white text-white font-extrabold px-8 py-4 rounded-xl hover:bg-neutral-900 transition-all text-xs uppercase tracking-widest">
                        CONTACTAR DIRECTO
                    </a>
                </div>
            </div>
        </section>

        <!-- Product Catalog Section -->
        <section id="catalogo" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <h2 class="text-3xl sm:text-5xl font-black uppercase tracking-tight text-white mb-3">
                        CATÁLOGO OFICIAL
                    </h2>
                    <p class="text-gray-400 text-sm sm:text-base">Libros en PDF con descarga e instrucciones de asesoría inmediata.</p>
                </div>

                <!-- Filter Controls -->
                <div class="flex flex-wrap gap-2 mt-6 md:mt-0">
                    <button onclick="filterProducts('all')" class="filter-btn active bg-brandRed text-white px-4 py-2 rounded-xl text-xs font-black uppercase tracking-wider transition-all">Todos</button>
                    <button onclick="filterProducts('ebooks')" class="filter-btn bg-neutral-900 text-gray-400 hover:text-white px-4 py-2 rounded-xl text-xs font-black uppercase tracking-wider border border-neutral-800 transition-all">Libros PDF</button>
                    <button onclick="filterProducts('services')" class="filter-btn bg-neutral-900 text-gray-400 hover:text-white px-4 py-2 rounded-xl text-xs font-black uppercase tracking-wider border border-neutral-800 transition-all">Asesorías</button>
                </div>
            </div>

            <!-- Dynamic Product Grid -->
            <div id="productGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Injected dynamically -->
            </div>
        </section>
    </main>

    <!-- OWNER ADMIN MODAL (Control Total) -->
    <div id="adminModal" class="fixed inset-0 z-50 overflow-y-auto hidden">
        <div class="fixed inset-0 bg-black/90 backdrop-blur-md" onclick="toggleAdminModal(false)"></div>
        
        <div class="relative min-h-screen flex items-center justify-center p-4">
            <div class="relative w-full max-w-2xl bg-neutral-950 border border-brandRed/50 rounded-3xl p-6 sm:p-8 shadow-2xl text-white">
                
                <div class="flex items-center justify-between border-b border-neutral-800 pb-4 mb-6">
                    <div>
                        <span class="text-xs font-black uppercase tracking-widest text-brandRed">ADMINISTRACIÓN TOTAL</span>
                        <h2 class="text-2xl font-black uppercase">PANEL DE WANER LUGO SÁNCHEZ</h2>
                    </div>
                    <button onclick="toggleAdminModal(false)" class="text-gray-400 hover:text-white p-2">
                        <i class="fa-solid fa-xmark text-2xl"></i>
                    </button>
                </div>

                <!-- Add New Product Form -->
                <form id="productForm" onsubmit="handleProductSubmit(event)" class="space-y-4">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-400 mb-1">Título del Producto / Libro</label>
                            <input type="text" id="adminTitle" required placeholder="Ej: Libro: El Código de Dominio" class="w-full bg-neutral-900 border border-neutral-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brandRed">
                        </div>
                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-400 mb-1">Categoría</label>
                            <select id="adminCategory" required class="w-full bg-neutral-900 border border-neutral-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brandRed">
                                <option value="ebooks">Libro PDF Digital</option>
                                <option value="services">Asesoría / Consejo Directivo</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-400 mb-1">Precio (USD $)</label>
                            <input type="number" step="0.01" id="adminPrice" required placeholder="Ej: 29.99" class="w-full bg-neutral-900 border border-neutral-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brandRed">
                        </div>
                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-400 mb-1">Etiqueta Destacada</label>
                            <input type="text" id="adminBadge" placeholder="Ej: MÁS VENDIDO / PDF OFICIAL" class="w-full bg-neutral-900 border border-neutral-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brandRed">
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-bold uppercase text-gray-400 mb-1">Descripción del Contenido</label>
                        <textarea id="adminDesc" rows="3" required placeholder="Explica qué aprenderán en este libro en PDF o en la sesión de asesoría..." class="w-full bg-neutral-900 border border-neutral-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brandRed"></textarea>
                    </div>

                    <!-- PDF Upload Simulator / Link -->
                    <div class="bg-neutral-900/80 p-4 rounded-xl border border-neutral-800 space-y-3">
                        <label class="block text-xs font-bold uppercase text-brandRed">
                            <i class="fa-solid fa-file-pdf mr-1"></i> Archivo PDF / Enlace de Descarga
                        </label>
                        <p class="text-[11px] text-gray-400">Inserta el enlace directo de tu PDF (ej. Google Drive, Dropbox, servidor privado) o selecciona un archivo para simular la subida:</p>
                        
                        <div class="flex flex-col sm:flex-row gap-2">
                            <input type="url" id="adminPdfUrl" placeholder="https://ejemplo.com/mi-libro.pdf" class="flex-1 bg-black border border-neutral-700 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-brandRed font-mono">
                            <label class="bg-neutral-800 hover:bg-neutral-700 text-white text-xs font-bold px-4 py-2 rounded-lg cursor-pointer flex items-center justify-center space-x-1">
                                <i class="fa-solid fa-upload"></i>
                                <span>Subir Local</span>
                                <input type="file" accept=".pdf" onchange="handleFileUpload(event)" class="hidden">
                            </label>
                        </div>
                    </div>

                    <div class="pt-4 flex justify-end space-x-3">
                        <button type="button" onclick="toggleAdminModal(false)" class="bg-neutral-900 text-gray-400 font-bold px-6 py-3 rounded-xl text-xs uppercase">Cancelar</button>
                        <button type="submit" class="bg-brandRed hover:bg-brandRedHover text-white font-black px-8 py-3 rounded-xl text-xs uppercase tracking-wider shadow-lg">
                            GUARDAR Y PUBLICAR
                        </button>
                    </div>
                </form>

                <!-- Manage Current Inventory -->
                <div class="mt-8 border-t border-neutral-800 pt-6">
                    <h3 class="text-sm font-black uppercase text-gray-300 mb-4">Inventario Actual (Puedes borrar o editar)</h3>
                    <div id="adminInventory" class="space-y-3 max-h-48 overflow-y-auto pr-2">
                        <!-- Dynamically populated -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- CART SLIDE-OVER MODAL -->
    <div id="cartModal" class="fixed inset-0 z-50 overflow-hidden hidden">
        <div id="cartBackdrop" onclick="toggleCart(false)" class="fixed inset-0 bg-black/80 backdrop-blur-sm transition-opacity opacity-0 duration-300"></div>

        <div class="fixed inset-y-0 right-0 max-w-full flex pl-10">
            <div id="cartPanel" class="w-screen max-w-md bg-neutral-950 border-l border-neutral-800 text-white transform translate-x-full transition-transform duration-300 ease-in-out flex flex-col justify-between">
                
                <div class="p-6 border-b border-neutral-800 flex items-center justify-between">
                    <div class="flex items-center space-x-2">
                        <i class="fa-solid fa-bag-shopping text-brandRed text-xl"></i>
                        <h2 class="text-xl font-black uppercase tracking-wider">Tu Carrito</h2>
                    </div>
                    <button onclick="toggleCart(false)" class="text-gray-400 hover:text-white p-2">
                        <i class="fa-solid fa-xmark text-xl"></i>
                    </button>
                </div>

                <!-- Items Container -->
                <div id="cartItemsContainer" class="p-6 overflow-y-auto flex-1 space-y-4">
                    <!-- Dynamic Cart Items -->
                </div>

                <!-- Cart Footer & Checkout -->
                <div class="p-6 border-t border-neutral-800 bg-neutral-900/50 space-y-4">
                    <div class="space-y-2">
                        <label class="text-xs font-semibold text-gray-400 uppercase tracking-wider block">Código Promocional</label>
                        <div class="flex space-x-2">
                            <input type="text" id="couponInput" placeholder="BROTHERHOOD40" class="bg-neutral-900 border border-neutral-700 rounded-xl px-3 py-2 text-sm text-white uppercase tracking-wider focus:outline-none focus:border-brandRed flex-1 font-mono">
                            <button onclick="applyCoupon()" class="bg-neutral-800 hover:bg-neutral-700 text-white font-bold px-4 py-2 rounded-xl text-xs uppercase tracking-wider">
                                Aplicar
                            </button>
                        </div>
                        <p id="couponMessage" class="text-xs hidden"></p>
                    </div>

                    <div class="space-y-1.5 text-sm pt-2">
                        <div class="flex justify-between text-gray-400">
                            <span>Subtotal</span>
                            <span id="cartSubtotal">$0.00</span>
                        </div>
                        <div id="discountRow" class="flex justify-between text-brandRed hidden font-bold">
                            <span>Descuento (40%)</span>
                            <span id="cartDiscount">-$0.00</span>
                        </div>
                        <div class="flex justify-between text-xl font-black text-white border-t border-neutral-800 pt-3">
                            <span>TOTAL</span>
                            <span id="cartTotal">$0.00</span>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 gap-2 pt-2">
                        <button onclick="checkoutWhatsApp()" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-black py-3.5 rounded-xl transition-all uppercase tracking-wider text-xs flex items-center justify-center space-x-2 shadow-lg">
                            <i class="fa-brands fa-whatsapp text-lg"></i>
                            <span>ORDENAR VÍA WHATSAPP</span>
                        </button>
                        <button onclick="checkoutEmail()" class="w-full bg-brandRed hover:bg-brandRedHover text-white font-black py-3.5 rounded-xl transition-all uppercase tracking-wider text-xs flex items-center justify-center space-x-2 shadow-lg">
                            <i class="fa-solid fa-envelope text-base"></i>
                            <span>ORDENAR VÍA EMAIL</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Popup Notifications -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 bg-white text-black font-bold px-5 py-3 rounded-xl shadow-2xl transition-all duration-300 transform translate-y-20 opacity-0 flex items-center space-x-3 pointer-events-none">
        <i class="fa-solid fa-circle-check text-brandRed text-lg"></i>
        <span id="toastMessage" class="text-sm uppercase tracking-wider">Acción realizada</span>
    </div>

    <!-- Footer -->
    <footer class="border-t border-accentBorder bg-black py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-6">
            <div>
                <span class="text-xl font-black tracking-widest uppercase block text-white">THE BROTHERHOOD</span>
    
