---
name: cym-ui
description: >
  CYM Industrial UI design patterns and styles (index section only).
  Trigger: When user requests UI changes to the index section or creates/modifies components used in index (Hero, HeroProducts, Benefits).
license: Apache-2.0
metadata:
  author: prowler-cloud
  version: "2.0"
  scope: [ui]
  auto_invoke: "Working with index section UI"
allowed-tools: Read, Edit, Write, Glob, Grep, Bash, WebFetch, WebSearch, Task
---

## Color Palette

### Primary Colors (Brand Red)
```html
<!-- Brand Red Scale -->
bg-red-500 (#ef4444) - Acentos, gradientes, borders
bg-red-600 (#dc2626) - Botones primarios, textos destacados
bg-red-700 (#b91c1c) - Logo background, elementos de énfasis
bg-red-900 (#7f1d1d) - Fondo oscuro, badges

text-red-400, text-red-300
border-red-500/20, border-red-500/30
```

### Secondary Colors (Amber/Gold)
```html
<!-- Amber Scale -->
text-amber-400 (#fbbf24) - Textos secundarios, iconos
bg-amber-500/10
bg-amber-500 (#f59e0b) - Botones secundarios, gradientes

<!-- Premium Gold Accents -->
bg-[#D4A017] - Acentos premium, líneas decorativas
hover:bg-[#B8940F] - Hover states premium
bg-[#9A7800] - Acentos oscuros premium
```

### Custom Premium Colors
```html
<!-- Premium Red/Brown Scale -->
bg-[#8B0000] - Dark Red (fondo Hero Premium)
bg-[#722F37] - Merlot (gradiente Hero Premium)
bg-[#5D1E1E] - Dark Brown (gradiente Hero Premium)
text-[#FAFAF9] - Off-White (texto Hero Premium)
```

### Action Colors (Emerald)
```html
<!-- Emerald for CTAs -->
bg-emerald-500 (#10b981) - Botones CTA (WhatsApp)
bg-emerald-600 (#059669) - Hover de botones CTA
hover:bg-emerald-700
```

### Backgrounds
```html
<!-- Hero sections -->
bg-linear-to-br from-red-900 to-red-700
bg-gradient-to-br from-[#8B0000] via-[#722F37] to-[#5D1E1E]

<!-- Products section -->
bg-gray-100
bg-[#F8F5F0] - Warm Gray (fondo minimalist)

<!-- Benefits section -->
bg-gradient-to-b from-gray-900 to-gray-950
bg-gray-800/50 backdrop-blur-sm

<!-- Dark/Tech themes -->
bg-gray-900 (#111827) - Footer, dark themes
bg-gray-950 (#030712) - Fondo oscuro tech

<!-- Cards/Overlays -->
bg-red-500/20
bg-red-900/30
bg-[#FAFAF9] - Off-white backgrounds
```

### Typography Colors
```html
<!-- Light backgrounds -->
text-white
text-gray-300
text-gray-400

<!-- Dark/Gray backgrounds -->
text-slate-700
text-gray-600
text-[#0F172A] - Slate Dark (texto minimalist)
text-red-300 (highlights)
```

---

## Typography

### Fonts
```html
<!-- Playfair Display - Headings premium -->
font-serif (Playfair Display)

<!-- Source Sans Pro - Body text -->
font-sans (Source Sans Pro)
```

### Headings
```html
<!-- Hero title -->
text-4xl md:text-5xl lg:text-6xl font-bold leading-tight

<!-- Section titles -->
text-4xl lg:text-5xl font-bold

<!-- Card titles -->
text-xl font-bold

<!-- Badges -->
text-sm font-semibold uppercase tracking-wide
```

### Body Text
```html
<!-- Descriptions -->
text-xl text-gray-300
text-xl text-gray-600

<!-- Card descriptions -->
text-gray-300 leading-relaxed
text-gray-400
```

---

## Layout Patterns

### Containers
```html
<!-- Hero container -->
max-w-7xl mx-auto px-6 lg:px-8 w-full

<!-- Products container -->
max-w-6xl mx-auto px-8

<!-- Benefits container -->
max-w-7xl mx-auto px-6 lg:px-8
```

### Grid Systems
```html
<!-- Hero two-column -->
grid grid-cols-1 lg:grid-cols-2 gap-12 items-center

<!-- Products three-column -->
grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8

<!-- Benefits three-column -->
grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8
```

### Spacing
```html
<!-- Section padding -->
py-20 (standard section)
min-h-screen (hero)

<!-- Centered headers -->
text-center mb-12

<!-- Element spacing -->
mb-4, mb-6, mb-8, mb-16
space-y-6, space-y-8
gap-8, gap-12
```

---

## Component Patterns

### Hero Section (Base)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-linear-to-br from-red-900 to-red-700"
>
    <!-- Background image with overlay -->
    <div class="absolute inset-0 opacity-20">
        <img src="/path/to/image" class="w-full h-full object-cover" />
    </div>

    <!-- Content -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <!-- Text content -->
            <div class="text-white space-y-8">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
                    Title <span class="text-amber-400">Highlight</span>
                </h1>
                <p class="text-xl text-gray-300">Description</p>
                <!-- CTA -->
                <a href="#" class="inline-flex items-center gap-3 px-8 py-4 bg-emerald-500 hover:bg-emerald-700 text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105">
                    <svg class="w-6 h-6">...</svg>
                    <span>Button Text</span>
                </a>
            </div>
            <!-- Image -->
            <div class="relative">
                <img src="/path/to/image" class="w-max max-w-6xl mx-auto object-contain" />
                <div class="absolute inset-0 bg-amber-500/10 blur-3xl rounded-full scale-125"></div>
            </div>
        </div>
    </div>
</section>
```

### Hero Section (TechForward)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gray-950"
>
    <!-- Mesh gradient background -->
    <div class="absolute inset-0 overflow-hidden">
        <div class="absolute inset-0 opacity-100 animate-[meshGradient_15s_ease_infinite]" style="background-image: 
            radial-gradient(at 40% 20%, rgba(127, 29, 29, 0.8) 0px, transparent 50%),
            radial-gradient(at 80% 0%, rgba(185, 28, 28, 0.6) 0px, transparent 50%),
            radial-gradient(at 0% 50%, rgba(220, 38, 38, 0.6) 0px, transparent 50%),
            radial-gradient(at 80% 50%, rgba(127, 29, 29, 0.7) 0px, transparent 50%),
            radial-gradient(at 0% 100%, rgba(185, 28, 28, 0.8) 0px, transparent 50%),
            radial-gradient(at 80% 100%, rgba(220, 38, 38, 0.6) 0px, transparent 50%);
        "></div>
    </div>

    <!-- Content with glass effect -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full z-10">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <!-- Animated gradient text -->
            <div class="text-white space-y-8">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold animate-gradientText">
                    Tech <span class="text-amber-400">Forward</span>
                </h1>
                <p class="text-xl text-gray-300">Description</p>
                <!-- CTA with glow -->
                <a href="#" class="relative inline-flex items-center gap-3 px-8 py-4 bg-emerald-500 hover:bg-emerald-700 text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105 shadow-lg shadow-emerald-500/25">
                    <div class="absolute inset-0 bg-gradient-to-r from-emerald-400 to-emerald-600 rounded-lg blur opacity-20 group-hover:opacity-30 transition-opacity"></div>
                    <svg class="w-6 h-6 relative z-10">...</svg>
                    <span class="relative z-10">Button Text</span>
                </a>
            </div>
        </div>
    </div>
</section>
```

### Hero Section (Premium)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-[#8B0000] via-[#722F37] to-[#5D1E1E]"
>
    <!-- Premium gold accents -->
    <div class="absolute top-0 right-0 w-96 h-96 bg-[#D4A017]/10 blur-3xl rounded-full"></div>
    <div class="absolute bottom-0 left-0 w-96 h-96 bg-[#D4A017]/10 blur-3xl rounded-full"></div>

    <!-- Content -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="text-[#FAFAF9] space-y-8">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
                    Premium <span class="text-[#D4A017]">Gold</span>
                </h1>
                <p class="text-xl text-gray-300">Description</p>
                <!-- CTA with gold border -->
                <a href="#" class="inline-flex items-center gap-3 px-8 py-4 bg-gradient-to-r from-[#D4A017] to-[#B8940F] hover:from-[#B8940F] hover:to-[#9A7800] text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105 shadow-lg shadow-[#D4A017]/25 border border-[#D4A017]/30">
                    <svg class="w-6 h-6">...</svg>
                    <span>Button Text</span>
                </a>
            </div>
        </div>
    </div>
</section>
```

### Hero Section (Minimalist)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-[#F8F5F0]"
>
    <!-- Clean content with slate dark text -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="text-[#0F172A] space-y-8">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
                    Minimalist <span class="text-red-600">Design</span>
                </h1>
                <p class="text-xl text-gray-600">Description</p>
                <!-- Simple CTA -->
                <a href="#" class="inline-flex items-center gap-3 px-8 py-4 bg-red-600 hover:bg-red-700 text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105">
                    <svg class="w-6 h-6">...</svg>
                    <span>Button Text</span>
                </a>
            </div>
        </div>
    </div>
</section>
```

### Hero Section (Products3DTilt)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gray-950"
>
    <!-- Mesh gradient -->
    <div class="absolute inset-0 overflow-hidden">
        <div class="absolute inset-0 opacity-100 animate-[meshGradient_15s_ease_infinite]" style="background-image: 
            radial-gradient(at 40% 20%, rgba(127, 29, 29, 0.8) 0px, transparent 50%),
            radial-gradient(at 80% 0%, rgba(185, 28, 28, 0.6) 0px, transparent 50%);
        "></div>
    </div>

    <!-- Content with 3D tilt cards -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full z-10">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="text-white space-y-8">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
                    3D <span class="text-amber-400">Products</span>
                </h1>
                <p class="text-xl text-gray-300">Description</p>
            </div>
            <!-- 3D tilt product showcase -->
            <div class="relative perspective-1000">
                <div class="transform-style-3d rotate-y-12 rotate-x-6 transition-transform duration-700 hover:rotate-y-0 hover:rotate-x-0">
                    <img src="/path/to/image" class="w-full max-w-2xl mx-auto object-contain" />
                </div>
            </div>
        </div>
    </div>
</section>
```

### Hero Section (ProductsHorizontal)
```html
<section
    id="inicio"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gray-950"
>
    <!-- Animated gradient background -->
    <div class="absolute inset-0 animate-gradientBackground" style="background: 
        linear-gradient(135deg, #ef4444 0%, #dc2626 25%, #f59e0b 50%, #ef4444 75%, #dc2626 100%);
        background-size: 200% auto;
        animation: gradientShift 3s ease-in-out infinite;
    "></div>

    <!-- Horizontal product showcase -->
    <div class="relative max-w-7xl mx-auto px-6 lg:px-8 w-full z-10">
        <div class="text-white space-y-8 mb-12">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold animate-gradientText">
                Horizontal <span class="text-amber-400">Showcase</span>
            </h1>
        </div>
        <!-- Horizontal scroll or grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            <!-- Product cards -->
        </div>
    </div>
</section>
```

### Product Card Section
```html
<section id="productos" class="py-20 px-0 bg-gray-100">
    <div class="max-w-6xl mx-auto px-8">
        <!-- Header -->
        <div class="text-center mb-12">
            <h2 class="text-4xl lg:text-5xl font-bold text-slate-700 mb-4">TITLE</h2>
            <p class="text-xl text-gray-600">Description</p>
        </div>

        <!-- Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- ProductCard component -->
        </div>
    </div>
</section>
```

### Benefits Card (With Red Hover)
```html
<div class="relative group">
    <!-- Glow effect -->
    <div class="absolute inset-0 bg-linear-to-br from-red-500/10 to-transparent rounded-2xl blur-xl group-hover:blur-2xl transition-all duration-300"></div>

    <!-- Card with red hover border -->
    <div class="relative bg-white border border-gray-200 rounded-2xl p-8 hover:-translate-y-2 hover:shadow-2xl hover:border-red-500 transition-all duration-300 h-full">
        <!-- Icon -->
        <div class="w-12 h-12 bg-red-500/20 rounded-xl flex items-center justify-center mb-6">
            <svg class="w-6 h-6 text-red-400">...</svg>
        </div>

        <!-- Content -->
        <h3 class="text-xl font-bold text-slate-700 mb-4 group-hover:text-red-600 transition-colors">Title</h3>
        <p class="text-gray-600 leading-relaxed">
            Text with <span class="text-red-500 font-semibold">highlight</span>
        </p>
    </div>
</div>
```

### Section Header with Badge
```html
<div class="text-center mb-16">
    <span class="inline-block px-4 py-2 bg-red-900/30 border border-red-500/20 rounded-full text-red-300 text-sm font-semibold mb-4">
        Badge Text
    </span>
    <h2 class="text-4xl md:text-5xl font-bold text-white mb-6">
        Title <span class="text-red-500">Highlight</span>
    </h2>
    <p class="text-xl text-gray-400 max-w-3xl mx-auto">
        Description text
    </p>
</div>
```

### CTA Box
```html
<div class="bg-gradient-to-r from-gray-800/50 to-gray-900/50 backdrop-blur-sm border border-gray-700/30 rounded-2xl p-12 max-w-4xl mx-auto">
    <h3 class="text-3xl font-bold text-white mb-6">Title</h3>
    <p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
        Text with <span class="text-red-300 font-semibold">highlight</span>
    </p>

    <a href="#" class="inline-flex items-center gap-3 px-10 py-4 bg-gradient-to-r from-red-600 to-red-700 hover:from-red-700 hover:to-red-800 text-white font-bold text-lg rounded-xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl shadow-red-500/25 border border-red-500/30 group">
        <svg class="w-7 h-7 group-hover:scale-110 transition-transform">...</svg>
        <span>Button Text</span>
    </a>

    <p class="text-gray-400 text-sm mt-6 flex items-center justify-center gap-2">
        <!-- Icon --> Subtitle text
    </p>
</div>
```

---

## Animations

### Standard Entry Animations
```html
<style>
    @keyframes fadeInUp {
        from { opacity: 0; transform: translateY(30px); }
        to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInLeft {
        from { opacity: 0; transform: translateX(-30px); }
        to { opacity: 1; transform: translateX(0); }
    }

    /* Usage */
    h1 {
        animation: fadeInUp 0.8s ease-out forwards;
    }

    p {
        animation: fadeInUp 0.8s ease-out 0.2s forwards;
        opacity: 0;
    }

    /* Staggered grid items */
    .grid > :nth-child(1) { animation: fadeInUp 0.8s ease-out forwards; }
    .grid > :nth-child(2) { animation: fadeInUp 0.8s ease-out 0.2s forwards; opacity: 0; }
    .grid > :nth-child(3) { animation: fadeInUp 0.8s ease-out 0.4s forwards; opacity: 0; }
</style>
```

### Animated Gradient Text
```html
<style>
    .animate-gradientText {
        background: linear-gradient(135deg, #ef4444 0%, #dc2626 25%, #f59e0b 50%, #ef4444 75%, #dc2626 100%);
        background-size: 200% auto;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        animation: gradientShift 3s ease-in-out infinite;
    }

    @keyframes gradientShift {
        0% { background-position: 0% center; }
        50% { background-position: 100% center; }
        100% { background-position: 0% center; }
    }
</style>
```

### Animated Gradient Background
```html
<style>
    .animate-gradientBackground {
        background: linear-gradient(135deg, #ef4444 0%, #dc2626 25%, #f59e0b 50%, #ef4444 75%, #dc2626 100%);
        background-size: 200% auto;
        animation: gradientShift 3s ease-in-out infinite;
    }
</style>
```

### Mesh Gradient Animation
```html
<style>
    @keyframes meshGradient {
        0% { transform: scale(1) rotate(0deg); }
        50% { transform: scale(1.1) rotate(5deg); }
        100% { transform: scale(1) rotate(0deg); }
    }

    .animate-meshGradient {
        animation: meshGradient 15s ease infinite;
    }
</style>
```

---

## Interactive Effects

### Hover Transitions (Red Glow)
```html
<!-- Card hover with red border and glow -->
group
hover:-translate-y-2
hover:shadow-2xl
hover:border-red-500
transition-all duration-300

<!-- Glow effect -->
absolute inset-0 bg-linear-to-br from-red-500/10 to-transparent blur-xl
group-hover:blur-2xl
transition-all duration-300
```

### Scale Hover
```html
transform hover:scale-105
hover:scale-110
transition-transform duration-500
```

### Border Hover
```html
hover:border-red-500/30
transition-all duration-300
```

### Shadow Effects
```html
shadow-lg hover:shadow-xl
shadow-red-500/25
shadow-[#D4A017]/25 (gold shadow)
shadow-emerald-500/25 (CTA shadow)
```

### Blur Glow
```html
group-hover:blur-2xl
transition-all duration-300
```

### Transition Classes
```html
transition-all duration-300
transform hover:scale-105 transition-transform duration-500
```

---

## Border Radius
```html
rounded-lg      <!-- Buttons, small cards -->
rounded-xl      <!-- Icon containers, badges -->
rounded-2xl     <!-- Large cards, sections -->
rounded-full    <!-- Circular badges, buttons -->
```

---

## WhatsApp CTA Pattern
```html
<a href="https://api.whatsapp.com/send?phone=526643108937&text=URL_ENCODED_MESSAGE" target="_blank"
   class="inline-flex items-center gap-3 px-8 py-4 bg-emerald-500 hover:bg-emerald-700 text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl shadow-emerald-500/25">
    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"></path>
    </svg>
    <span>Contactar por WhatsApp</span>
</a>
```

---

## Critical Rules

1. **Scope**: Only apply to index section components (Hero, HeroProducts, Benefits)
2. **Colors**: Use brand red palette, avoid generic colors
3. **Animations**: Use fadeInUp/fadeInLeft for entry animations, gradientShift/meshGradient for backgrounds
4. **WhatsApp**: Always use the provided phone number (526643108937)
5. **Gradients**: Use linear-to-br for backgrounds, gradient-to-b for sections
6. **Blur**: Use blur-xl/blur-2xl/blur-3xl for glow effects
7. **Backdrop**: Use backdrop-blur-sm with semi-transparent backgrounds
8. **Spacing**: Use py-20 for standard sections, min-h-screen for hero
9. **Custom Colors**: Use hex values for premium colors (#8B0000, #722F37, #5D1E1E, #D4A017, #B8940F, #9A7800)
10. **Shadows**: Use shadow-red-500/25 for red glows, shadow-[#D4A017]/25 for gold accents
11. **Hero Variants**: Choose appropriate Hero variant (TechForward, Premium, Minimalist, Products3DTilt, ProductsHorizontal) based on design needs
12. **Hover Effects**: Use red border hover (hover:border-red-500) for cards with glow effects
