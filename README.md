<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مدونة إبراهيم الأغبس - التقنية والتطوير الشخصي والثقافة</title>
    <meta name="description" content="مدونة عربية شاملة تغطي أحدث تطورات التقنية والذكاء الاصطناعي، التطوير الشخصي، الثقافة، السفر، والطبخ">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'arabic': ['Tajawal', 'Cairo', 'Segoe UI', 'Tahoma', 'Arial', 'sans-serif'],
                    },
                    colors: {
                        primary: '#5D5CDE',
                        secondary: '#7C3AED',
                        accent: '#F59E0B',
                        success: '#10B981',
                        warning: '#F59E0B',
                        danger: '#EF4444',
                    },
                    boxShadow: {
                        'neon': '0 8px 32px 0 rgba(93,92,222,0.12), 0 4px 16px 0 rgba(93,92,222,0.08)',
                        'glow': '0 0 20px rgba(93,92,222,0.3)',
                        'deep': '0 20px 40px -12px rgba(0,0,0,0.25)',
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'bounce-slow': 'bounce 3s infinite',
                        'gradient': 'gradient 8s ease infinite',
                    },
                    backgroundImage: {
                        'gradient-radial': 'radial-gradient(var(--tw-gradient-stops))',
                        'hero-pattern': 'linear-gradient(45deg, #667eea 0%, #764ba2 100%)',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;900&family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <style>
        html { scroll-behavior: smooth; }
        body { 
            font-family: 'Cairo', 'Tajawal', Segoe UI, Tahoma, Arial, sans-serif;
            overflow-x: hidden;
        }
        
        /* Custom Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        @keyframes gradient {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(60px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(100px); }
            to { opacity: 1; transform: translateX(0); }
        }
        @keyframes zoomIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
        
        .animate-fade-up { animation: fadeInUp 0.8s ease-out forwards; }
        .animate-slide-right { animation: slideInRight 0.8s ease-out forwards; }
        .animate-zoom-in { animation: zoomIn 0.6s ease-out forwards; }
        
        /* Text Effects */
        .gradient-text {
            background: linear-gradient(135deg, #5D5CDE, #7C3AED, #F59E0B);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 8s ease infinite;
        }
        
        .glow-text {
            text-shadow: 0 0 20px rgba(93,92,222,0.5);
        }
        
        /* Glass Effects */
        .glass {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.2);
        }
        .glass-dark {
            background: rgba(0,0,0,0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Cards */
        .card-hover {
            transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .card-hover:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25);
        }
        
        /* Category Pills */
        .category-pill {
            transition: all 0.3s cubic-bezier(0.4,0,0.2,1);
            position: relative;
            overflow: hidden;
        }
        .category-pill::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }
        .category-pill:hover::before {
            left: 100%;
        }
        
        /* Progress Bar */
        .progress-bar {
            background: linear-gradient(90deg, #5D5CDE, #7C3AED, #F59E0B);
            background-size: 300% 100%;
            animation: gradient 3s ease infinite;
        }
        
        /* Scrollbar */
        .custom-scrollbar::-webkit-scrollbar { width: 8px; }
        .custom-scrollbar::-webkit-scrollbar-track { background: rgba(156,163,175,0.1); border-radius: 10px; }
        .custom-scrollbar::-webkit-scrollbar-thumb { 
            background: linear-gradient(135deg, #5D5CDE, #7C3AED);
            border-radius: 10px;
            border: 2px solid transparent;
            background-clip: content-box;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover { 
            background: linear-gradient(135deg, #4C46D6, #6D28D9);
            background-clip: content-box;
        }
        
        /* Hero Background */
        .hero-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #5D5CDE 100%);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            position: relative;
        }
        .hero-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 20% 80%, rgba(253,224,71,0.3) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(93,92,222,0.3) 0%, transparent 50%);
        }
        
        /* Line Clamp */
        .line-clamp-2 {
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        .line-clamp-3 {
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        
        /* Modal */
        .modal-backdrop {
            backdrop-filter: blur(8px);
            background: rgba(0,0,0,0.6);
        }
        
        /* Stats Counter Animation */
        .counter { font-variant-numeric: tabular-nums; }
        
        /* Featured Badge */
        .featured-badge {
            background: linear-gradient(45deg, #F59E0B, #EAB308);
            animation: pulse-slow 2s infinite;
        }
        
        /* Navigation */
        .nav-sticky {
            backdrop-filter: blur(20px);
            background: rgba(255,255,255,0.9);
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }
        .dark .nav-sticky {
            background: rgba(17,24,39,0.9);
            border-bottom: 1px solid rgba(75,85,99,0.2);
        }
        
        /* Focus Styles */
        .focus-ring:focus {
            outline: 2px solid #5D5CDE;
            outline-offset: 2px;
        }
        
        /* Article Grid Masonry Effect */
        .articles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            align-items: start;
        }
        
        /* Intersection Observer Animation */
        .reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease-out;
        }
        .reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Dark mode specific styles */
        .dark .prose h1, .dark .prose h2, .dark .prose h3 { color: #F9FAFB; }
        .dark .prose p { color: #D1D5DB; }
        .dark .prose strong { color: #FDE047; }
        .dark .prose a { color: #A5B4FC; }
        .dark .prose code { background: #374151; color: #F9FAFB; }
        
        /* Loading Skeleton */
        .skeleton {
            background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
            background-size: 200% 100%;
            animation: loading 1.5s infinite;
        }
        @keyframes loading {
            0% { background-position: 200% 0; }
            100% { background-position: -200% 0; }
        }
    </style>
</head>
<body class="font-arabic bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-gray-100 transition-all duration-500 custom-scrollbar">

<!-- Loading Screen -->
<div id="loading-screen" class="fixed inset-0 z-50 flex items-center justify-center bg-gradient-to-br from-purple-600 to-blue-600">
    <div class="text-center">
        <div class="w-16 h-16 border-4 border-white border-t-transparent rounded-full animate-spin mb-4 mx-auto"></div>
        <h2 class="text-white text-xl font-bold">جاري التحميل...</h2>
    </div>
</div>

<!-- Navigation -->
<nav id="navbar" class="fixed top-0 w-full z-40 transition-all duration-300 nav-sticky">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center py-4">
            <!-- Logo -->
            <div class="flex items-center space-x-3 space-x-reverse">
                <div class="relative group">
                    <div class="w-12 h-12 bg-gradient-to-r from-purple-600 to-blue-600 rounded-2xl flex items-center justify-center transform group-hover:scale-110 transition-transform duration-300 shadow-glow">
                        <span class="text-white font-black text-xl">ت</span>
                    </div>
                    <div class="absolute -inset-2 bg-gradient-to-r from-purple-600 to-blue-600 rounded-2xl opacity-0 group-hover:opacity-20 transition-opacity duration-300 blur"></div>
                </div>
                <div>
                    <h1 class="text-2xl font-black gradient-text tracking-tight">إبراهيم الأغبس</h1>
                    <p class="text-xs text-gray-500 dark:text-gray-400 font-medium">مدونة التقنية والحياة</p>
                </div>
            </div>
            
            <!-- Desktop Navigation -->
            <div class="hidden lg:flex items-center space-x-8 space-x-reverse">
                <button onclick="filterByCategory('all')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="all">
                    جميع المقالات
                </button>
                <button onclick="filterByCategory('tech')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="tech">
                    تقنية
                </button>
                <button onclick="filterByCategory('personal')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="personal">
                    تطوير شخصي
                </button>
                <button onclick="filterByCategory('culture')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="culture">
                    ثقافة
                </button>
                <button onclick="filterByCategory('travel')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="travel">
                    سفر
                </button>
                <button onclick="filterByCategory('cooking')" class="nav-link text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-300 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="cooking">
                    طبخ
                </button>
            </div>
            
            <!-- Search & Mobile Menu -->
            <div class="flex items-center space-x-4 space-x-reverse">
                <!-- Search -->
                <div class="relative hidden md:block">
                    <input type="text" id="search-input" placeholder="ابحث في المقالات..." 
                           class="w-72 px-6 py-3 text-sm border-2 border-gray-200 dark:border-gray-600 rounded-2xl bg-white dark:bg-gray-800 focus:border-purple-500 focus:ring-4 focus:ring-purple-200 dark:focus:ring-purple-800 outline-none transition-all duration-300 pr-12">
                    <svg class="absolute right-4 top-3.5 h-5 w-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                    </svg>
                </div>
                
                <!-- Theme Toggle -->
                <button id="theme-toggle" class="p-3 rounded-2xl bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors duration-300 focus-ring">
                    <span id="theme-icon" class="text-xl">🌙</span>
                </button>
                
                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="lg:hidden p-3 rounded-2xl bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors duration-300 focus-ring">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>
    </div>
</nav>

<!-- Mobile Menu -->
<div id="mobile-menu" class="fixed inset-0 z-50 lg:hidden transform translate-x-full transition-transform duration-300">
    <div class="absolute inset-0 bg-black bg-opacity-50 backdrop-blur-sm" onclick="closeMobileMenu()"></div>
    <div class="absolute right-0 top-0 w-80 max-w-full h-full bg-white dark:bg-gray-900 shadow-deep">
        <div class="flex justify-between items-center p-6 border-b border-gray-200 dark:border-gray-700">
            <div class="flex items-center space-x-3 space-x-reverse">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-blue-600 rounded-xl flex items-center justify-center">
                    <span class="text-white font-bold">ت</span>
                </div>
                <h1 class="text-xl font-black gradient-text">إبراهيم الأغبس</h1>
            </div>
            <button onclick="closeMobileMenu()" class="p-2 rounded-xl hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors duration-300">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
            </button>
        </div>
        <div class="p-6 space-y-4">
            <input type="text" id="mobile-search" placeholder="ابحث في المقالات..." 
                   class="w-full px-4 py-3 text-sm border-2 border-gray-200 dark:border-gray-600 rounded-xl bg-white dark:bg-gray-800 focus:border-purple-500 outline-none transition-all duration-300">
            <div class="space-y-2">
                <button onclick="filterByCategory('all');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">جميع المقالات</button>
                <button onclick="filterByCategory('tech');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">تقنية</button>
                <button onclick="filterByCategory('personal');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">تطوير شخصي</button>
                <button onclick="filterByCategory('culture');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">ثقافة</button>
                <button onclick="filterByCategory('travel');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">سفر</button>
                <button onclick="filterByCategory('cooking');closeMobileMenu()" class="block w-full text-right px-4 py-3 rounded-xl text-base font-semibold hover:bg-purple-100 dark:hover:bg-purple-900 transition-colors duration-300">طبخ</button>
            </div>
        </div>
    </div>
</div>

<!-- Hero Section -->
<section class="relative hero-bg min-h-screen flex items-center pt-20">
    <div class="absolute inset-0 bg-gradient-to-br from-black/20 to-black/40"></div>
    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <div class="text-center">
            <!-- Floating Elements -->
            <div class="absolute top-10 left-10 w-20 h-20 bg-yellow-400 rounded-full opacity-20 animate-float"></div>
            <div class="absolute top-32 right-16 w-16 h-16 bg-purple-500 rounded-full opacity-30 animate-float" style="animation-delay: 2s;"></div>
            <div class="absolute bottom-20 left-1/4 w-12 h-12 bg-blue-500 rounded-full opacity-25 animate-float" style="animation-delay: 4s;"></div>
            
            <div class="animate-fade-up">
                <h1 class="text-5xl md:text-7xl font-black text-white mb-8 leading-tight">
                    مرحباً بك في
                    <span class="block gradient-text glow-text">إبراهيم الأغبس</span>
                </h1>
                <p class="text-xl md:text-2xl text-blue-100 mb-12 max-w-4xl mx-auto leading-relaxed opacity-90">
                    مدونة عربية شاملة تجمع بين أحدث التطورات التقنية والذكاء الاصطناعي، التطوير الشخصي، الثقافة، السفر، والطبخ
                </p>
                <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
                    <button onclick="filterByCategory('tech')" class="group px-10 py-4 bg-white text-purple-900 font-black rounded-2xl shadow-deep hover:shadow-glow transform hover:scale-105 transition-all duration-300 focus-ring">
                        <span class="flex items-center">
                            استكشف المقالات التقنية
                            <svg class="w-5 h-5 mr-3 group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
                            </svg>
                        </span>
                    </button>
                    <button onclick="scrollToSection('about')" class="group px-10 py-4 border-2 border-white text-white font-black rounded-2xl hover:bg-white hover:text-purple-900 transform hover:scale-105 transition-all duration-300 focus-ring">
                        <span class="flex items-center">
                            تعرف علينا أكثر
                            <svg class="w-5 h-5 mr-3 group-hover:rotate-12 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
                            </svg>
                        </span>
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
        <div class="w-6 h-10 border-2 border-white rounded-full flex justify-center">
            <div class="w-1 h-3 bg-white rounded-full mt-2 animate-pulse"></div>
        </div>
    </div>
</section>

<!-- Stats Section -->
<section class="py-20 bg-white dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700 reveal">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
            <div class="text-center p-6 rounded-2xl bg-gradient-to-br from-purple-50 to-purple-100 dark:from-purple-900/20 dark:to-purple-800/20 transform hover:scale-105 transition-transform duration-300">
                <div class="text-4xl md:text-5xl font-black gradient-text counter" id="articles-count">0</div>
                <div class="text-sm font-semibold text-gray-600 dark:text-gray-400 mt-2">مقال منشور</div>
            </div>
            <div class="text-center p-6 rounded-2xl bg-gradient-to-br from-blue-50 to-blue-100 dark:from-blue-900/20 dark:to-blue-800/20 transform hover:scale-105 transition-transform duration-300">
                <div class="text-4xl md:text-5xl font-black text-blue-600 dark:text-blue-400 counter" id="total-views">0</div>
                <div class="text-sm font-semibold text-gray-600 dark:text-gray-400 mt-2">مشاهدة</div>
            </div>
            <div class="text-center p-6 rounded-2xl bg-gradient-to-br from-green-50 to-green-100 dark:from-green-900/20 dark:to-green-800/20 transform hover:scale-105 transition-transform duration-300">
                <div class="text-4xl md:text-5xl font-black text-green-600 dark:text-green-400">6</div>
                <div class="text-sm font-semibold text-gray-600 dark:text-gray-400 mt-2">أقسام متنوعة</div>
            </div>
            <div class="text-center p-6 rounded-2xl bg-gradient-to-br from-orange-50 to-orange-100 dark:from-orange-900/20 dark:to-orange-800/20 transform hover:scale-105 transition-transform duration-300">
                <div class="text-4xl md:text-5xl font-black text-orange-600 dark:text-orange-400 counter" id="avg-rating">0.0</div>
                <div class="text-sm font-semibold text-gray-600 dark:text-gray-400 mt-2">متوسط التقييم</div>
            </div>
        </div>
    </div>
</section>

<!-- Articles Section -->
<section class="py-20 reveal">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section Header -->
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-gray-900 dark:text-white mb-6 gradient-text">أحدث المقالات</h2>
            <p class="text-xl text-gray-600 dark:text-gray-300 max-w-3xl mx-auto leading-relaxed">اكتشف مجموعة متنوعة من المقالات المفيدة والممتعة في مختلف المجالات</p>
        </div>
        
        <!-- Filter Buttons -->
        <div class="flex flex-wrap justify-center gap-4 mb-12">
            <button onclick="filterByCategory('all')" class="filter-btn category-pill active px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gradient-to-r from-purple-500 to-blue-500 text-white shadow-neon focus-ring" data-category="all">
                الكل (<span id="count-all" class="font-black">0</span>)
            </button>
            <button onclick="filterByCategory('tech')" class="filter-btn category-pill px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gray-100 dark:bg-gray-800 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="tech">
                تقنية (<span id="count-tech" class="font-black">0</span>)
            </button>
            <button onclick="filterByCategory('personal')" class="filter-btn category-pill px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gray-100 dark:bg-gray-800 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="personal">
                تطوير شخصي (<span id="count-personal" class="font-black">0</span>)
            </button>
            <button onclick="filterByCategory('culture')" class="filter-btn category-pill px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gray-100 dark:bg-gray-800 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="culture">
                ثقافة (<span id="count-culture" class="font-black">0</span>)
            </button>
            <button onclick="filterByCategory('travel')" class="filter-btn category-pill px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gray-100 dark:bg-gray-800 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="travel">
                سفر (<span id="count-travel" class="font-black">0</span>)
            </button>
            <button onclick="filterByCategory('cooking')" class="filter-btn category-pill px-8 py-3 rounded-2xl text-sm font-bold transition-all duration-300 bg-gray-100 dark:bg-gray-800 hover:bg-purple-100 dark:hover:bg-purple-900 focus-ring" data-category="cooking">
                طبخ (<span id="count-cooking" class="font-black">0</span>)
            </button>
        </div>
        
        <!-- Articles Grid -->
        <div id="articles-container" class="articles-grid"></div>
        
        <!-- Load More Button -->
        <div class="text-center mt-16">
            <button id="load-more-btn" class="group px-12 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-bold rounded-2xl shadow-neon hover:shadow-glow transform hover:scale-105 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed focus-ring">
                <span class="flex items-center">
                    تحميل المزيد
                    <svg class="w-5 h-5 mr-3 group-hover:translate-y-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
                    </svg>
                </span>
            </button>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about" class="py-20 bg-gradient-to-br from-gray-50 to-purple-50 dark:from-gray-800 dark:to-purple-900/20 reveal">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-gray-900 dark:text-white mb-6 gradient-text">
                لماذا إبراهيم الأغبس؟
            </h2>
            <p class="text-xl text-gray-600 dark:text-gray-300 max-w-4xl mx-auto leading-relaxed">
                نحن نؤمن بقوة المحتوى العربي عالي الجودة في تطوير مجتمعنا وإثراء معرفتنا
            </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="group bg-white dark:bg-gray-800 p-10 rounded-3xl shadow-deep hover:shadow-glow card-hover glass border border-gray-100 dark:border-gray-700">
                <div class="w-16 h-16 bg-gradient-to-r from-purple-500 to-purple-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                    </svg>
                </div>
                <h3 class="text-2xl font-black text-gray-900 dark:text-white mb-4 group-hover:text-purple-600 dark:group-hover:text-purple-400 transition-colors duration-300">محتوى متميز</h3>
                <p class="text-gray-600 dark:text-gray-300 leading-relaxed">مقالات مدروسة ومفصلة تغطي أحدث التطورات بأسلوب واضح ومفهوم للجميع</p>
            </div>
            
            <div class="group bg-white dark:bg-gray-800 p-10 rounded-3xl shadow-deep hover:shadow-glow card-hover glass border border-gray-100 dark:border-gray-700">
                <div class="w-16 h-16 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C20.832 18.477 19.246 18 17.5 18c-1.746 0-3.332.477-4.5 1.253"></path>
                    </svg>
                </div>
                <h3 class="text-2xl font-black text-gray-900 dark:text-white mb-4 group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors duration-300">تنوع المواضيع</h3>
                <p class="text-gray-600 dark:text-gray-300 leading-relaxed">من التقنية إلى التطوير الشخصي والثقافة، نغطي كل ما يهمك في حياتك اليومية</p>
            </div>
            
            <div class="group bg-white dark:bg-gray-800 p-10 rounded-3xl shadow-deep hover:shadow-glow card-hover glass border border-gray-100 dark:border-gray-700">
                <div class="w-16 h-16 bg-gradient-to-r from-green-500 to-green-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path>
                    </svg>
                </div>
                <h3 class="text-2xl font-black text-gray-900 dark:text-white mb-4 group-hover:text-green-600 dark:group-hover:text-green-400 transition-colors duration-300">مجتمع نشط</h3>
                <p class="text-gray-600 dark:text-gray-300 leading-relaxed">انضم لمجتمع من المهتمين بالتعلم والتطوير المستمر والنقاش البناء</p>
            </div>
        </div>
    </div>
</section>

<!-- Newsletter Section -->
<section class="py-20 bg-gradient-to-r from-purple-600 to-blue-600 reveal">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <div class="bg-white/10 backdrop-blur-md rounded-3xl p-12 border border-white/20">
            <h2 class="text-3xl md:text-4xl font-black text-white mb-6">ابق على اطلاع دائم</h2>
            <p class="text-xl text-blue-100 mb-8 leading-relaxed">اشترك في النشرة البريدية لتصلك أحدث المقالات والمحتوى الحصري</p>
            <div class="flex flex-col sm:flex-row gap-4 max-w-md mx-auto">
                <input type="email" placeholder="البريد الإلكتروني" 
                       class="flex-1 px-6 py-4 rounded-2xl border-2 border-white/30 bg-white/10 text-white placeholder-blue-200 focus:border-white focus:outline-none backdrop-blur-sm">
                <button class="px-8 py-4 bg-white text-purple-600 font-bold rounded-2xl hover:bg-gray-100 transform hover:scale-105 transition-all duration-300 focus-ring shadow-lg">
                    اشتراك
                </button>
            </div>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="bg-gray-900 dark:bg-gray-950 text-white py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-12">
            <!-- Brand -->
            <div class="col-span-1 md:col-span-2">
                <div class="flex items-center space-x-3 space-x-reverse mb-6">
                    <div class="w-12 h-12 bg-gradient-to-r from-purple-600 to-blue-600 rounded-2xl flex items-center justify-center">
                        <span class="text-white font-black text-xl">ت</span>
                    </div>
                    <div>
                        <h3 class="text-2xl font-black gradient-text">إبراهيم الأغبس</h3>
                        <p class="text-sm text-gray-400 font-medium">مدونة التقنية والحياة</p>
                    </div>
                </div>
                <p class="text-gray-300 leading-relaxed mb-8 text-lg">
                    مدونة عربية تهدف إلى نشر المعرفة والثقافة التقنية، وتقديم محتوى مفيد ومتنوع يساعد على التطوير والنمو الشخصي.
                </p>
                <div class="flex space-x-4 space-x-reverse">
                    <a href="#" class="w-12 h-12 bg-gray-800 rounded-2xl flex items-center justify-center hover:bg-purple-600 transition-colors duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/></svg>
                    </a>
                    <a href="#" class="w-12 h-12 bg-gray-800 rounded-2xl flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/></svg>
                    </a>
                    <a href="#" class="w-12 h-12 bg-gray-800 rounded-2xl flex items-center justify-center hover:bg-green-600 transition-colors duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/></svg>
                    </a>
                </div>
            </div>
            
            <!-- Categories -->
            <div>
                <h4 class="text-xl font-bold mb-6 text-white">الأقسام</h4>
                <ul class="space-y-3">
                    <li><a href="#" onclick="filterByCategory('tech')" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">التقنية والذكاء الاصطناعي</a></li>
                    <li><a href="#" onclick="filterByCategory('personal')" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">التطوير الشخصي</a></li>
                    <li><a href="#" onclick="filterByCategory('culture')" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">الثقافة والقراءة</a></li>
                    <li><a href="#" onclick="filterByCategory('travel')" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">السفر والاستكشاف</a></li>
                    <li><a href="#" onclick="filterByCategory('cooking')" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">الطبخ والتغذية</a></li>
                </ul>
            </div>
            
            <!-- Links -->
            <div>
                <h4 class="text-xl font-bold mb-6 text-white">روابط مفيدة</h4>
                <ul class="space-y-3">
                    <li><a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">من نحن</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">اتصل بنا</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">سياسة الخصوصية</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">الشروط والأحكام</a></li>
                </ul>
            </div>
        </div>
        
        <div class="border-t border-gray-800 mt-16 pt-8 text-center">
            <p class="text-gray-400 text-lg">&copy; 2024 إبراهيم الأغبس. جميع الحقوق محفوظة.</p>
        </div>
    </div>
</footer>

<!-- Floating Action Buttons -->
<div class="fixed bottom-6 left-6 z-50 flex flex-col gap-4">
    <!-- Scroll to Top -->
    <button id="scroll-top" class="w-14 h-14 bg-gradient-to-r from-purple-600 to-blue-600 rounded-full shadow-glow flex items-center justify-center text-white opacity-0 transform translate-y-4 transition-all duration-300 hover:scale-110 focus-ring">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 15l7-7 7 7"></path>
        </svg>
    </button>
</div>

<script src="https://cdn.jsdelivr.net/npm/marked@5.1.1/marked.min.js"></script>
<script>
// Articles Data
const articlesData = [
    {
        id: '1',
        title: 'مستقبل الذكاء الاصطناعي في التعليم العربي',
        content: 'استكشاف كيفية تأثير تقنيات الذكاء الاصطناعي على منظومة التعليم في العالم العربي، والتحديات والفرص المتاحة لتطوير التعليم الرقمي باللغة العربية.',
        category: 'tech',
        author: 'إبراهيم الأغبس',
        date: '2024-01-15',
        readTime: 8,
        views: 1250,
        rating: 4.8,
        comments: 23,
        tags: ['ذكاء اصطناعي', 'تعليم', 'تقنية', 'مستقبل'],
        featured: true,
        hasFullContent: true,
        fullContent: `# مستقبل الذكاء الاصطناعي في التعليم العربي

## مقدمة

يشهد العالم تطوراً متسارعاً في مجال الذكاء الاصطناعي، وهذا التطور يفتح آفاقاً جديدة في قطاع التعليم. في هذا المقال، سنستكشف كيف يمكن للذكاء الاصطناعي أن يثور منظومة التعليم في العالم العربي.

## التحديات الحالية في التعليم العربي

- **نقص في الموارد التعليمية** باللغة العربية
- **صعوبة الوصول** للتعليم عالي الجودة في المناطق النائية
- **الحاجة لتخصيص** التعليم حسب قدرات كل طالب

## الفرص المتاحة

### 1. التعلم الشخصي
يمكن للذكاء الاصطناعي تحليل أسلوب تعلم كل طالب وتقديم محتوى مخصص يناسب قدراته واهتماماته.

### 2. المساعدين الافتراضيين
تطوير مساعدين ذكيين يتحدثون العربية ويمكنهم الإجابة على أسئلة الطلاب على مدار الساعة.

### 3. التقييم الذكي
استخدام التحليل التنبؤي لتحديد نقاط القوة والضعف لدى الطلاب وتقديم خطط تحسين شخصية.

## التطبيقات العملية

- **منصات التعلم التفاعلية** التي تتكيف مع مستوى الطالب
- **أنظمة ترجمة متطورة** لإتاحة المحتوى العالمي باللغة العربية
- **برامج محاكاة** للتجارب العلمية والتدريب المهني

## الخلاصة

الذكاء الاصطناعي ليس مجرد تقنية جديدة، بل هو أداة قوية يمكنها تحويل التعليم العربي إلى نظام أكثر فعالية وإنصافاً وتخصيصاً. المطلوب الآن هو استثمار حكيم وتخطيط محكم لضمان الاستفادة القصوى من هذه التقنيات.`
    },
    {
        id: '2',
        title: 'كيفية بناء عادات إيجابية تستمر مدى الحياة',
        content: 'دليل شامل لفهم علم بناء العادات وتطبيق استراتيجيات عملية لتكوين عادات إيجابية والتخلص من العادات السيئة بطريقة علمية ومؤثرة.',
        category: 'personal',
        author: 'إبراهيم الأغبس',
        date: '2024-01-12',
        readTime: 6,
        views: 2100,
        rating: 4.9,
        comments: 45,
        tags: ['تطوير شخصي', 'عادات', 'إنتاجية', 'نمو'],
        featured: true,
        hasFullContent: true,
        fullContent: `# كيفية بناء عادات إيجابية تستمر مدى الحياة

## فهم علم العادات

العادة هي سلوك نقوم به تلقائياً دون تفكير واعي. وفقاً للدراسات، **40% من أفعالنا اليومية** هي عادات وليست قرارات واعية.

## دورة العادة الأساسية

### 1. المحفز (Cue)
العامل الذي يشير لدماغك لبدء العادة

### 2. الروتين (Routine)  
السلوك نفسه الذي تريد تكوينه

### 3. المكافأة (Reward)
الفائدة التي تحصل عليها من أداء العادة

## استراتيجيات بناء العادات الجديدة

### قاعدة الـ 2%
ابدأ بتحسين صغير جداً (2% يومياً) بدلاً من تغييرات جذرية

### تقنية التكديس
اربط العادة الجديدة بعادة موجودة بالفعل

**مثال:** "بعد أن أشرب قهوة الصباح، سأقرأ 5 صفحات من كتاب"

### قانون البيئة
اجعل العادة الجيدة واضحة ومرئية، والعادة السيئة مخفية وصعبة

## خطة عملية للـ 30 يوم الأولى

**الأسبوع الأول:** ركز على الاتساق وليس الكمال
**الأسبوع الثاني:** زد الصعوبة تدريجياً  
**الأسبوع الثالث:** تعامل مع التحديات والانتكاسات
**الأسبوع الرابع:** قيّم التقدم واضبط المسار

## أمثلة عملية

- **عادة القراءة:** اقرأ صفحة واحدة قبل النوم
- **عادة الرياضة:** اخصص 10 دقائق للحركة عند الاستيقاظ  
- **عادة التأمل:** تنفس بعمق لمدة دقيقتين بعد كل وجبة

## الخلاصة

بناء العادات الإيجابية يحتاج صبر والتزام، لكن التأثير التراكمي هائل. ابدأ صغيراً، كن متسقاً، وثق في العملية.`
    },
    {
        id: '3',
        title: 'رحلة استكشاف المغرب: من مراكش إلى الصحراء',
        content: 'تجربة سفر ممتعة عبر أجمل مدن المغرب، من أسواق مراكش التاريخية إلى كثبان الصحراء الذهبية، مع نصائح عملية للمسافرين العرب.',
        category: 'travel',
        author: 'إبراهيم الأغبس',
        date: '2024-01-10',
        readTime: 7,
        views: 1800,
        rating: 4.7,
        comments: 31,
        tags: ['سفر', 'المغرب', 'مراكش', 'صحراء', 'ثقافة'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '4',
        title: 'فن الطبخ المغربي: الطاجين الأصيل خطوة بخطوة',
        content: 'تعلم كيفية إعداد الطاجين المغربي الأصيل بطريقة تقليدية، مع أسرار النكهات والتوابل التي تجعل الطبق لذيذاً لا يقاوم.',
        category: 'cooking',
        author: 'إبراهيم الأغبس',
        date: '2024-01-08',
        readTime: 5,
        views: 3200,
        rating: 4.8,
        comments: 67,
        tags: ['طبخ', 'طاجين', 'مغربي', 'وصفات', 'تقليدي'],
        featured: true,
        hasFullContent: true,
        fullContent: `# فن الطبخ المغربي: الطاجين الأصيل خطوة بخطوة

## مقدمة

الطاجين هو رمز من رموز المطبخ المغربي العريق. هذا الطبق التقليدي الذي يحمل في طياته تاريخاً عريقاً من النكهات والتوابل الأصيلة.

## المكونات الأساسية

### اللحم (1 كيلو)
- لحم ضأن أو دجاج مقطع قطع متوسطة
- يفضل اللحم مع العظم للنكهة

### الخضروات
- 2 حبة بصل مقطعة شرائح
- 3 حبات جزر مقطعة دوائر سميكة  
- 2 حبة بطاطس مقطعة أرباع
- 200 غرام من الزيتون الأخضر

### التوابل المغربية
- ملعقة صغيرة **رأس الحانوت** (خلطة التوابل المغربية)
- نصف ملعقة صغيرة زنجبيل مطحون
- نصف ملعقة صغيرة قرفة
- رشة زعفران حقيقي
- ملح وفلفل أسود

## طريقة التحضير

### الخطوة الأولى: تحضير اللحم
1. اغسل قطع اللحم جيداً وتبلها بالملح والفلفل
2. اتركها ترتاح لمدة 30 دقيقة

### الخطوة الثانية: الطبخ البطيء
1. ضع إناء الطاجين على نار متوسطة
2. أضف زيت الزيتون واتركه يسخن
3. حمر قطع اللحم من جميع الجهات
4. أضف البصل واتركه ينذبل

### الخطوة الثالثة: إضافة التوابل
1. أضف جميع التوابل وحرك لدقيقتين
2. أضف كوب من الماء المغلي
3. غطي الإناء واتركه ينضج لمدة ساعة

### الخطوة الرابعة: إضافة الخضروات
1. أضف الجزر والبطاطس
2. اتركه ينضج لـ 30 دقيقة إضافية
3. أضف الزيتون في آخر 10 دقائق

## نصائح الطهي الاحترافية

- **استخدم إناء الطاجين الطيني** للحصول على النكهة الأصيلة
- **لا تحرك الطعام كثيراً** دعه ينضج بهدوء
- **تذوق واضبط التوابل** حسب الذوق الشخصي

## التقديم التقليدي

يُقدم الطاجين ساخناً مع:
- **الخبز المغربي** (الخبز المدور)
- **سلطة مغربية** بالطماطم والخيار
- **الشاي المغربي بالنعناع** كمشروب مرافق

## الخلاصة

الطاجين المغربي ليس مجرد وجبة، بل تجربة ثقافية كاملة. بالصبر والتوابل الصحيحة، ستحصل على طبق يحمل كل نكهات المغرب الأصيلة.`
    },
    {
        id: '5',
        title: 'تأثير القراءة على تطوير الشخصية والذكاء',
        content: 'دراسة معمقة حول الفوائد العلمية للقراءة وتأثيرها على الدماغ والشخصية، مع استراتيجيات عملية لبناء عادة القراءة اليومية.',
        category: 'culture',
        author: 'إبراهيم الأغبس',
        date: '2024-01-05',
        readTime: 9,
        views: 1650,
        rating: 4.9,
        comments: 29,
        tags: ['قراءة', 'ثقافة', 'تطوير', 'ذكاء', 'كتب'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '6',
        title: 'ثورة الحوسبة الكمية: هل ستغير مستقبل التقنية؟',
        content: 'نظرة شاملة على تقنية الحوسبة الكمية وإمكانياتها الهائلة في حل المشاكل المعقدة، والتحديات التي تواجه تطويرها وتطبيقها.',
        category: 'tech',
        author: 'إبراهيم الأغبس',
        date: '2024-01-03',
        readTime: 10,
        views: 980,
        rating: 4.6,
        comments: 15,
        tags: ['حوسبة كمية', 'تقنية', 'مستقبل', 'ابتكار'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '7',
        title: 'فن إدارة الوقت: تقنيات مثبتة علمياً',
        content: 'استراتيجيات عملية لإدارة الوقت بفعالية أكبر، بناءً على أحدث الأبحاث في علم النفس والإنتاجية، مع تطبيقات عملية يومية.',
        category: 'personal',
        author: 'إبراهيم الأغبس',
        date: '2024-01-01',
        readTime: 6,
        views: 2800,
        rating: 4.8,
        comments: 52,
        tags: ['إدارة وقت', 'إنتاجية', 'تنظيم', 'تطوير شخصي'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '8',
        title: 'تجربة السفر إلى اليابان: دليل المسافر العربي',
        content: 'رحلة مفصلة عبر اليابان من طوكيو إلى كيوتو، مع نصائح عملية حول الثقافة اليابانية، التأشيرات، الطعام، والأماكن السياحية المميزة.',
        category: 'travel',
        author: 'إبراهيم الأغبس',
        date: '2023-12-28',
        readTime: 8,
        views: 1420,
        rating: 4.7,
        comments: 26,
        tags: ['اليابان', 'سفر', 'ثقافة', 'سياحة', 'آسيا'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '9',
        title: 'أسرار المطبخ الشامي: الكبة اللبنانية الأصيلة',
        content: 'طريقة إعداد الكبة اللبنانية التقليدية بخطوات مفصلة، مع أسرار الحشو والعجينة والقلي للحصول على كبة مقرمشة من الخارج وطرية من الداخل.',
        category: 'cooking',
        author: 'إبراهيم الأغبس',
        date: '2023-12-25',
        readTime: 7,
        views: 2150,
        rating: 4.9,
        comments: 38,
        tags: ['كبة', 'لبناني', 'شامي', 'طبخ', 'تقليدي'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '10',
        title: 'تاريخ الأدب العربي الحديث: من النهضة إلى المعاصرة',
        content: 'رحلة عبر تطور الأدب العربي من عصر النهضة حتى اليوم، مع استعراض أهم الكتاب والحركات الأدبية التي شكلت الهوية الثقافية العربية.',
        category: 'culture',
        author: 'إبراهيم الأغبس',
        date: '2023-12-22',
        readTime: 12,
        views: 890,
        rating: 4.5,
        comments: 19,
        tags: ['أدب عربي', 'تاريخ', 'ثقافة', 'نهضة', 'معاصر'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '11',
        title: 'الأمن السيبراني في عصر إنترنت الأشياء',
        content: 'التحديات الأمنية الجديدة التي تفرضها أجهزة إنترنت الأشياء، وكيفية حماية خصوصيتنا وبياناتنا في عالم متصل بالكامل.',
        category: 'tech',
        author: 'إبراهيم الأغبس',
        date: '2023-12-20',
        readTime: 9,
        views: 1100,
        rating: 4.7,
        comments: 21,
        tags: ['أمن سيبراني', 'إنترنت الأشياء', 'خصوصية', 'حماية'],
        featured: false,
        hasFullContent: false
    },
    {
        id: '12',
        title: 'بناء الثقة بالنفس: دليل عملي للتطوير الذاتي',
        content: 'استراتيجيات مثبتة لبناء الثقة بالنفس وتطوير صورة ذاتية إيجابية، مع تمارين عملية وتقنيات نفسية فعالة.',
        category: 'personal',
        author: 'إبراهيم الأغبس',
        date: '2023-12-18',
        readTime: 8,
        views: 1950,
        rating: 4.8,
        comments: 35,
        tags: ['ثقة بالنفس', 'تطوير ذاتي', 'علم نفس', 'شخصية'],
        featured: false,
        hasFullContent: false
    }
];

// App State
let currentFilter = 'all';
let currentPage = 1;
const articlesPerPage = 6;
let filteredArticles = [...articlesData];
let isLoading = false;

// Initialize App
document.addEventListener('DOMContentLoaded', function() {
    // Hide loading screen
    setTimeout(() => {
        document.getElementById('loading-screen').style.opacity = '0';
        setTimeout(() => {
            document.getElementById('loading-screen').style.display = 'none';
        }, 500);
    }, 1500);
    
    initializeTheme();
    setupEventListeners();
    updateStats();
    updateCategoryCounts();
    renderArticles(getArticlesToShow());
    updateLoadMoreButton();
    setupIntersectionObserver();
    setupScrollEffects();
});

// Theme Management
function initializeTheme() {
    const savedTheme = localStorage.getItem('theme');
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    const theme = savedTheme || (prefersDark ? 'dark' : 'light');
    
    setTheme(theme);
    
    // Listen for system theme changes
    window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
        if (!localStorage.getItem('theme')) {
            setTheme(event.matches ? 'dark' : 'light');
        }
    });
}

function setTheme(theme) {
    const html = document.documentElement;
    const icon = document.getElementById('theme-icon');
    
    if (theme === 'dark') {
        html.classList.add('dark');
        icon.textContent = '☀️';
    } else {
        html.classList.remove('dark');
        icon.textContent = '🌙';
    }
    
    localStorage.setItem('theme', theme);
}

function toggleTheme() {
    const isDark = document.documentElement.classList.contains('dark');
    setTheme(isDark ? 'light' : 'dark');
}

// Event Listeners
function setupEventListeners() {
    // Theme toggle
    document.getElementById('theme-toggle').addEventListener('click', toggleTheme);
    
    // Mobile menu
    document.getElementById('mobile-menu-btn').addEventListener('click', openMobileMenu);
    
    // Search
    const searchInputs = [document.getElementById('search-input'), document.getElementById('mobile-search')];
    searchInputs.forEach(input => {
        if (input) {
            input.addEventListener('input', debounce(handleSearch, 300));
        }
    });
    
    // Load more
    document.getElementById('load-more-btn').addEventListener('click', loadMore);
    
    // Scroll to top
    document.getElementById('scroll-top').addEventListener('click', scrollToTop);
}

// Utility Functions
function debounce(func, delay) {
    let timeoutId;
    return function (...args) {
        clearTimeout(timeoutId);
        timeoutId = setTimeout(() => func.apply(this, args), delay);
    };
}

function animateCounter(elementId, target, decimals = 0) {
    const element = document.getElementById(elementId);
    if (!element) return;
    
    const increment = target / 100;
    let current = 0;
    
    const timer = setInterval(() => {
        current += increment;
        if (current >= target) {
            current = target;
            clearInterval(timer);
        }
        element.textContent = decimals > 0 ? current.toFixed(decimals) : Math.floor(current).toLocaleString();
    }, 20);
}

function getCategoryName(category) {
    const categories = {
        'tech': 'تقنية',
        'personal': 'تطوير شخصي', 
        'culture': 'ثقافة',
        'travel': 'سفر',
        'cooking': 'طبخ'
    };
    return categories[category] || category;
}

// Stats Functions
function updateStats() {
    const totalViews = articlesData.reduce((sum, article) => sum + article.views, 0);
    const avgRating = articlesData.reduce((sum, article) => sum + article.rating, 0) / articlesData.length;
    
    setTimeout(() => {
        animateCounter('articles-count', articlesData.length);
        animateCounter('total-views', totalViews);
        animateCounter('avg-rating', avgRating, 1);
    }, 500);
}

function updateCategoryCounts() {
    const categories = ['all', 'tech', 'personal', 'culture', 'travel', 'cooking'];
    categories.forEach(category => {
        const count = category === 'all' ? 
            articlesData.length : 
            articlesData.filter(article => article.category === category).length;
        
        const element = document.getElementById(`count-${category}`);
        if (element) element.textContent = count;
    });
}

// Filter Functions
function filterByCategory(category) {
    currentFilter = category;
    currentPage = 1;
    
    // Update active button
    document.querySelectorAll('.filter-btn').forEach(btn => {
        btn.classList.remove('active');
        btn.classList.remove('bg-gradient-to-r', 'from-purple-500', 'to-blue-500', 'text-white', 'shadow-neon');
        btn.classList.add('bg-gray-100', 'dark:bg-gray-800', 'hover:bg-purple-100', 'dark:hover:bg-purple-900');
    });
    
    const activeBtn = document.querySelector(`[data-category="${category}"]`);
    if (activeBtn) {
        activeBtn.classList.add('active');
        activeBtn.classList.remove('bg-gray-100', 'dark:bg-gray-800', 'hover:bg-purple-100', 'dark:hover:bg-purple-900');
        activeBtn.classList.add('bg-gradient-to-r', 'from-purple-500', 'to-blue-500', 'text-white', 'shadow-neon');
    }
    
    applyFilters();
}

function handleSearch(event) {
    const query = event.target.value.trim();
    applyFilters(query);
}

function applyFilters(searchQuery = '') {
    let articles = articlesData;
    
    // Apply category filter
    if (currentFilter !== 'all') {
        articles = articles.filter(article => article.category === currentFilter);
    }
    
    // Apply search filter
    if (searchQuery) {
        articles = articles.filter(article =>
            article.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
            article.content.toLowerCase().includes(searchQuery.toLowerCase()) ||
            article.tags.some(tag => tag.toLowerCase().includes(searchQuery.toLowerCase()))
        );
    }
    
    filteredArticles = articles;
    currentPage = 1;
    renderArticles(getArticlesToShow());
    updateLoadMoreButton();
}

// Rendering Functions
function getArticlesToShow() {
    const endIndex = currentPage * articlesPerPage;
    return filteredArticles.slice(0, endIndex);
}

function renderArticles(articles) {
    const container = document.getElementById('articles-container');
    
    if (articles.length === 0) {
        container.innerHTML = `
            <div class="col-span-full text-center py-16">
                <div class="text-6xl mb-4">🔍</div>
                <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-2">لا توجد مقالات</h3>
                <p class="text-gray-600 dark:text-gray-400">جرب البحث عن شيء آخر أو اختر قسماً مختلفاً</p>
            </div>
        `;
        return;
    }
    
    container.innerHTML = articles.map(article => `
        <article class="group bg-white dark:bg-gray-800 rounded-3xl shadow-deep hover:shadow-glow card-hover border border-gray-100 dark:border-gray-700 overflow-hidden reveal">
            <!-- Image/Header -->
            <div class="relative h-56 bg-gradient-to-br from-purple-500 via-blue-500 to-indigo-600 overflow-hidden">
                <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent"></div>
                
                <!-- Category Badge -->
                <div class="absolute top-4 right-4">
                    <span class="px-3 py-1 bg-white/90 text-purple-700 text-xs font-bold rounded-full backdrop-blur-sm">
                        ${getCategoryName(article.category)}
                    </span>
                </div>
                
                <!-- Featured Badge -->
                ${article.featured ? `
                    <div class="absolute top-4 left-4">
                        <span class="featured-badge px-3 py-1 text-white text-xs font-black rounded-full shadow-lg">
                            ✨ مميز
                        </span>
                    </div>
                ` : ''}
                
                <!-- Title -->
                <div class="absolute bottom-4 left-4 right-4">
                    <h3 class="text-white font-black text-xl leading-tight line-clamp-2 glow-text">
                        ${article.title}
                    </h3>
                </div>
            </div>
            
            <!-- Content -->
            <div class="p-8">
                <p class="text-gray-600 dark:text-gray-300 leading-relaxed mb-6 line-clamp-3 text-lg">
                    ${article.content}
                </p>
                
                <!-- Meta Info -->
                <div class="flex items-center justify-between mb-6 text-sm text-gray-500 dark:text-gray-400">
                    <div class="flex items-center space-x-6 space-x-reverse">
                        <span class="flex items-center">
                            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                            </svg>
                            ${article.readTime} دقيقة
                        </span>
                        <span class="flex items-center">
                            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                            </svg>
                            ${article.views.toLocaleString()}
                        </span>
                        <span class="flex items-center">
                            <svg class="w-4 h-4 ml-1" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
                            </svg>
                            ${article.rating}
                        </span>
                    </div>
                    <span class="text-gray-400">${article.date}</span>
                </div>
                
                <!-- Tags -->
                <div class="flex flex-wrap gap-2 mb-6">
                    ${article.tags.slice(0, 3).map(tag => `
                        <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 text-sm font-medium rounded-full">
                            ${tag}
                        </span>
                    `).join('')}
                    ${article.tags.length > 3 ? `
                        <span class="text-sm text-gray-500 dark:text-gray-400 px-2 py-1">
                            +${article.tags.length - 3} أخرى
                        </span>
                    ` : ''}
                </div>
                
                <!-- Footer -->
                <div class="flex items-center justify-between">
                    <!-- Author -->
                    <div class="flex items-center space-x-3 space-x-reverse">
                        <img src="https://ui-avatars.com/api/?name=${encodeURIComponent(article.author)}&background=5d5cde&color=fff&size=48" 
                             alt="avatar" 
                             class="w-10 h-10 rounded-full shadow-md border-2 border-purple-200 dark:border-purple-700">
                        <span class="font-bold text-gray-900 dark:text-white">${article.author}</span>
                    </div>
                    
                    <!-- Read Button -->
                    <button onclick="openArticle('${article.id}')" 
                            class="group px-6 py-3 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-bold rounded-2xl shadow-neon hover:shadow-glow transform hover:scale-105 transition-all duration-300 focus-ring">
                        <span class="flex items-center">
                            اقرأ المقال
                            <svg class="w-4 h-4 mr-2 group-hover:-translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                            </svg>
                        </span>
                    </button>
                </div>
            </div>
        </article>
    `).join('');
}

function updateLoadMoreButton() {
    const btn = document.getElementById('load-more-btn');
    const totalArticles = filteredArticles.length;
    const showingArticles = currentPage * articlesPerPage;
    
    if (showingArticles >= totalArticles) {
        btn.style.display = 'none';
    } else {
        btn.style.display = 'inline-flex';
        const remaining = totalArticles - showingArticles;
        btn.querySelector('span').firstChild.textContent = `تحميل المزيد (${remaining} متبقي)`;
    }
}

function loadMore() {
    if (isLoading) return;
    
    isLoading = true;
    const btn = document.getElementById('load-more-btn');
    const originalText = btn.querySelector('span').firstChild.textContent;
    
    btn.querySelector('span').firstChild.textContent = 'جاري التحميل...';
    btn.disabled = true;
    
    setTimeout(() => {
        currentPage++;
        renderArticles(getArticlesToShow());
        updateLoadMoreButton();
        isLoading = false;
        btn.disabled = false;
    }, 800);
}

// Mobile Menu Functions
function openMobileMenu() {
    document.getElementById('mobile-menu').style.transform = 'translateX(0)';
}

function closeMobileMenu() {
    document.getElementById('mobile-menu').style.transform = 'translateX(100%)';
}

// Scroll Functions
function setupScrollEffects() {
    let lastScrollY = window.scrollY;
    const navbar = document.getElementById('navbar');
    const scrollTop = document.getElementById('scroll-top');
    
    window.addEventListener('scroll', () => {
        const currentScrollY = window.scrollY;
        
        // Navbar hide/show
        if (currentScrollY > lastScrollY && currentScrollY > 100) {
            navbar.style.transform = 'translateY(-100%)';
        } else {
            navbar.style.transform = 'translateY(0)';
        }
        
        // Scroll to top button
        if (currentScrollY > 600) {
            scrollTop.style.opacity = '1';
            scrollTop.style.transform = 'translateY(0)';
        } else {
            scrollTop.style.opacity = '0';
            scrollTop.style.transform = 'translateY(16px)';
        }
        
        lastScrollY = currentScrollY;
    });
}

function scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
}

function scrollToSection(sectionId) {
    document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
}

// Intersection Observer for Animations
function setupIntersectionObserver() {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('revealed');
            }
        });
    }, { threshold: 0.1 });
    
    document.querySelectorAll('.reveal').forEach(el => {
        observer.observe(el);
    });
}

// Article Modal Functions
function openArticle(articleId) {
    const article = articlesData.find(a => a.id === articleId);
    if (!article) return;
    
    const modal = document.createElement('div');
    modal.className = 'fixed inset-0 z-50 flex items-center justify-center modal-backdrop';
    modal.innerHTML = `
        <div class="relative bg-white dark:bg-gray-800 max-w-5xl w-full mx-4 my-8 rounded-3xl shadow-deep overflow-hidden max-h-screen flex flex-col animate-zoom-in">
            <!-- Progress Bar -->
            <div id="read-progress" class="absolute top-0 left-0 right-0 h-1 progress-bar" style="width: 0%; z-index: 10;"></div>
            
            <!-- Header -->
            <div class="bg-gradient-to-r from-purple-600 to-blue-600 text-white p-8">
                <div class="flex justify-between items-start">
                    <div class="flex-1">
                        <h1 class="text-3xl font-black mb-4 leading-tight">${article.title}</h1>
                        <div class="flex items-center space-x-6 space-x-reverse text-blue-100">
                            <span class="flex items-center">
                                <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                                </svg>
                                ${article.readTime} دقيقة قراءة
                            </span>
                            <span class="flex items-center">
                                <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
                                </svg>
                                ${article.date}
                            </span>
                            <span class="flex items-center">
                                <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path>
                                </svg>
                                ${article.author}
                            </span>
                        </div>
                    </div>
                    <button onclick="closeArticle()" class="p-2 hover:bg-white/20 rounded-xl transition-colors duration-300 focus-ring">
                        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                        </svg>
                    </button>
                </div>
            </div>
            
            <!-- Content -->
            <div class="flex-1 overflow-y-auto custom-scrollbar" id="article-content">
                <div class="p-8">
                    <div class="prose prose-xl max-w-none dark:prose-invert">
                        ${article.hasFullContent && article.fullContent ? 
                            marked.parse(article.fullContent) : 
                            `<div class="text-center py-16">
                                <div class="w-24 h-24 mx-auto mb-6 bg-gradient-to-br from-purple-100 to-blue-100 dark:from-purple-900/30 dark:to-blue-900/30 rounded-3xl flex items-center justify-center">
                                    <svg class="w-12 h-12 text-purple-600 dark:text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                                    </svg>
                                </div>
                                <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">المحتوى الكامل قريباً</h3>
                                <p class="text-gray-600 dark:text-gray-300 text-lg leading-relaxed max-w-2xl mx-auto">
                                    ${article.content}
                                </p>
                                <div class="mt-8 p-6 bg-gradient-to-r from-purple-50 to-blue-50 dark:from-purple-900/20 dark:to-blue-900/20 rounded-2xl border border-purple-200 dark:border-purple-800">
                                    <p class="text-purple-700 dark:text-purple-300 font-semibold">
                                        نعمل على إضافة المحتوى الكامل لهذا المقال. ابق متابعاً للحصول على التحديثات!
                                    </p>
                                </div>
                            </div>`
                        }
                    </div>
                </div>
            </div>
            
            <!-- Footer -->
            <div class="bg-gray-50 dark:bg-gray-900 p-8 border-t border-gray-200 dark:border-gray-700">
                <!-- Tags -->
                <div class="flex flex-wrap gap-3 mb-6">
                    ${article.tags.map(tag => `
                        <span class="px-4 py-2 bg-gradient-to-r from-purple-100 to-blue-100 dark:from-purple-900/30 dark:to-blue-900/30 text-purple-700 dark:text-purple-300 font-bold rounded-xl border border-purple-200 dark:border-purple-800">
                            ${tag}
                        </span>
                    `).join('')}
                </div>
                
                <!-- Stats & Actions -->
                <div class="flex items-center justify-between">
                    <div class="flex items-center space-x-6 space-x-reverse text-gray-600 dark:text-gray-400">
                        <span class="flex items-center font-semibold">
                            <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                            </svg>
                            ${article.views.toLocaleString()} مشاهدة
                        </span>
                        <span class="flex items-center font-semibold">
                            <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
                            </svg>
                            ${article.comments} تعليق
                        </span>
                        <span class="flex items-center font-semibold">
                            <svg class="w-5 h-5 ml-2" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
                            </svg>
                            ${article.rating} تقييم
                        </span>
                    </div>
                    <button onclick="closeArticle()" class="px-8 py-3 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-bold rounded-2xl shadow-neon hover:shadow-glow transform hover:scale-105 transition-all duration-300 focus-ring">
                        إغلاق
                    </button>
                </div>
            </div>
        </div>
    `;
    
    document.body.appendChild(modal);
    document.body.style.overflow = 'hidden';
    
    // Setup reading progress
    const content = modal.querySelector('#article-content');
    const progress = modal.querySelector('#read-progress');
    
    content.addEventListener('scroll', () => {
        const scrolled = content.scrollTop;
        const maxScroll = content.scrollHeight - content.clientHeight;
        const percent = (scrolled / maxScroll) * 100;
        progress.style.width = Math.min(100, Math.max(0, percent)) + '%';
    });
    
    // Close on backdrop click
    modal.addEventListener('click', (e) => {
        if (e.target === modal) closeArticle();
    });
    
    // Close on Escape key
    const handleEscape = (e) => {
        if (e.key === 'Escape') {
            closeArticle();
            document.removeEventListener('keydown', handleEscape);
        }
    };
    document.addEventListener('keydown', handleEscape);
}

function closeArticle() {
    const modal = document.querySelector('.modal-backdrop');
    if (modal) {
        modal.style.opacity = '0';
        modal.style.transform = 'scale(0.95)';
        setTimeout(() => {
            modal.remove();
            document.body.style.overflow = '';
        }, 300);
    }
}
</script>
</body>
</html>
