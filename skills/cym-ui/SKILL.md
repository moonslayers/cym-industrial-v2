---
name: cym-ui
description: >
  CYM Industrial UI design patterns and styles (index section only).
  Trigger: When user requests UI changes to the index section or creates/modifies components used in index (Hero, HeroProducts, Benefits).
license: Apache-2.0
metadata:
  author: prowler-cloud
  version: "1.0"
  scope: [ui]
  auto_invoke: "Working with index section UI"
allowed-tools: Read, Edit, Write, Glob, Grep, Bash, WebFetch, WebSearch, Task
---

## Color Palette

### Primary Colors
```html
<!-- Brand Red -->
bg-red-900, bg-red-700, bg-red-600, bg-red-500
text-red-400, text-red-300
border-red-500/20, border-red-500/30

<!-- Amber for highlights -->
text-amber-400
bg-amber-500/10

<!-- Emerald for CTAs -->
bg-emerald-500, hover:bg-emerald-700
```

### Backgrounds
```html
<!-- Hero section -->
bg-linear-to-br from-red-900 to-red-700

<!-- Products section -->
bg-gray-100

<!-- Benefits section -->
bg-gradient-to-b from-gray-900 to-gray-950
bg-gray-800/50 backdrop-blur-sm

<!-- Cards/Overlays -->
bg-red-500/20
bg-red-900/30
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
text-red-300 (highlights)
```

---

## Typography

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

### Hero Section
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

### Benefits Card
```html
<div class="relative group">
    <!-- Glow effect -->
    <div class="absolute inset-0 bg-linear-to-br from-red-500/5 to-transparent rounded-2xl blur-xl group-hover:blur-2xl transition-all duration-300"></div>

    <!-- Card -->
    <div class="relative bg-gray-800/50 backdrop-blur-sm border border-gray-700/50 rounded-2xl p-8 hover:border-red-500/30 transition-all duration-300 h-full">
        <!-- Icon -->
        <div class="w-12 h-12 bg-red-500/20 rounded-xl flex items-center justify-center mb-6">
            <svg class="w-6 h-6 text-red-400">...</svg>
        </div>

        <!-- Content -->
        <h3 class="text-xl font-bold text-white mb-4">Title</h3>
        <p class="text-gray-300 leading-relaxed">
            Text with <span class="text-red-300 font-semibold">highlight</span>
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

---

## Interactive Effects

### Hover Transitions
```html
<!-- Scale hover -->
transform hover:scale-105
hover:scale-110

<!-- Border hover -->
hover:border-red-500/30

<!-- Blur glow -->
group-hover:blur-2xl

<!-- Shadow -->
shadow-lg hover:shadow-xl
shadow-red-500/25
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
   class="inline-flex items-center gap-3 px-8 py-4 bg-emerald-500 hover:bg-emerald-700 text-white font-semibold rounded-lg transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
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
3. **Animations**: Use fadeInUp/fadeInLeft for entry animations
4. **WhatsApp**: Always use the provided phone number (526643108937)
5. **Gradients**: Use linear-to-br for backgrounds, gradient-to-b for sections
6. **Blur**: Use blur-xl/blur-2xl/blur-3xl for glow effects
7. **Backdrop**: Use backdrop-blur-sm with semi-transparent backgrounds
8. **Spacing**: Use py-20 for standard sections, min-h-screen for hero
