---
name: frontend-designer
description: >
  Guides creation of distinctive, production-grade frontend interfaces that avoid generic AI aesthetics.
  Trigger: When user asks to design, redesign, or improve a UI interface or component.
license: Apache-2.0
metadata:
  author: prowler-cloud
  version: "1.0"
  scope: [root, ui]
  auto_invoke: "Designing, redesigning, or improving UI interfaces"
  allowed-tools: Read, Edit, Write, Glob, Grep, Bash, WebFetch, WebSearch, Task
---

## When to Use

Use this skill when:
- User asks to create a new frontend component, page, or interface
- User requests redesigning or improving an existing UI
- User mentions UI design, frontend design, or interface improvements
- Building landing pages, dashboards, forms, or any interactive interface

## Design Thinking

Before coding, understand the context and commit to a BOLD aesthetic direction:

### Questions to Answer
- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick an extreme:
  - Brutally minimal
  - Maximalist chaos
  - Retro-futuristic
  - Organic/natural
  - Luxury/refined
  - Playful/toy-like
  - Editorial/magazine
  - Brutalist/raw
  - Art deco/geometric
  - Soft/pastel
  - Industrial/utilitarian
  - And many more flavors to choose from
- **Constraints**: Technical requirements (framework, performance, accessibility)
- **Differentiation**: What makes this UNFORGETTABLE? What's the one thing someone will remember?

**CRITICAL**: Choose a clear conceptual direction and execute it with precision. Bold maximalism and refined minimalism both work - the key is intentionality, not intensity.

## Critical Rules

### NEVER Use Generic Aesthetics

```html
<!-- ❌ NEVER: Generic fonts -->
font-family: Arial, Inter, Roboto, system-ui

<!-- ❌ NEVER: Cliched color schemes -->
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); /* Purple gradient on white */

<!-- ❌ NEVER: Predictable layouts -->
<div class="container mx-auto px-4">
  <h1 class="text-4xl font-bold text-center">Heading</h1>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
    <!-- Cards -->
  </div>
</div>
```

```html
<!-- ✅ ALWAYS: Distinctive character -->
font-family: 'Playfair Display', 'Space Mono', 'Outfit', 'Instrument Serif', 'Syne', 'Clash Display'

<!-- ✅ ALWAYS: Cohesive, intentional palettes */
--color-primary: #C41E3A;
--color-accent: #D4A017;
--color-surface: #F8F5F0;

<!-- ✅ ALWAYS: Unexpected layouts -->
 asymmetry, diagonal flow, grid-breaking, overlapping elements
```

### Font Guidelines

Choose fonts that are beautiful, unique, and interesting. Pair a distinctive display font with a refined body font.

**Distinctive Display Fonts (Examples):**
- Playfair Display (serif, elegant)
- Syne (bold, geometric)
- Clash Display (modern, distinctive)
- Instrument Serif (refined, literary)
- Space Grotesk (bold, technical)
- Outfit (modern sans)
- Fraunces (display serif)

**Refined Body Fonts (Examples):**
- Satoshi (clean sans)
- Source Sans Pro
- Cormorant Garamond (elegant serif)
- DM Sans (modern geometric)
- IBM Plex Sans (technical)

### Color & Theme Rules

```css
/* ✅ Dominant colors with sharp accents */
:root {
  --color-primary: #0F172A;    /* Dominant: dark slate */
  --color-accent: #FF5733;    /* Sharp: vibrant orange */
  --color-surface: #F1F5F9;
  --color-text: #334155;
}

/* ❌ Timid, evenly-distributed palettes */
:root {
  --color-blue: #3B82F6;
  --color-green: #10B981;
  --color-purple: #8B5CF6;
  --color-pink: #EC4899;
  --color-orange: #F97316;
}
```

## Frontend Aesthetics Guidelines

### Typography

```html
<!-- Distinctive pairings -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Satoshi:wght@400;500&display=swap');

  h1, h2, h3 { font-family: 'Playfair Display', serif; }
  body { font-family: 'Satoshi', sans-serif; }
</style>

<h1 class="text-5xl font-bold tracking-tight">Brilliant Design</h1>
<p class="text-lg leading-relaxed text-gray-600">Elegant body text with refined spacing.</p>
```

### Motion & Animations

**High-Impact Moments:**

```html
<!-- One orchestrated page load with staggered reveals -->
<style>
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-title {
    animation: fadeInUp 1s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .hero-description {
    animation: fadeInUp 1s cubic-bezier(0.16, 1, 0.3, 1) 0.2s forwards;
    opacity: 0;
  }

  .hero-cta {
    animation: fadeInUp 1s cubic-bezier(0.16, 1, 0.3, 1) 0.4s forwards;
    opacity: 0;
  }
</style>
```

**Scroll-Triggered Effects:**

```html
<!-- Intersection Observer for scroll animations -->
<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.animate-on-scroll').forEach(el => {
    observer.observe(el);
  });
</script>

<style>
  .animate-on-scroll {
    opacity: 0;
    transform: translateY(30px);
    transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  }

  .animate-on-scroll.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
```

**Hover States That Surprise:**

```html
<!-- Unexpected hover effects -->
<button class="group relative overflow-hidden px-8 py-4 bg-black text-white transition-all duration-500">
  <span class="relative z-10 transition-colors duration-500 group-hover:text-black">
    Hover Me
  </span>
  <div class="absolute inset-0 bg-white transform scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-500 ease-out"></div>
</button>
```

### Spatial Composition

```html
<!-- Asymmetry -->
<div class="grid grid-cols-12 gap-8">
  <div class="col-span-7">Large element</div>
  <div class="col-span-5 mt-16">Offset smaller element</div>
</div>

<!-- Overlap -->
<div class="relative">
  <div class="absolute -top-8 -left-8 w-48 h-48 bg-accent/20 rounded-full blur-3xl"></div>
  <div class="relative z-10 bg-white p-8 shadow-xl rounded-2xl">
    Content overlapping decorative blur
  </div>
</div>

<!-- Diagonal flow -->
<div class="transform -rotate-2 origin-left">
  <div class="bg-gradient-to-r from-primary to-accent p-12 rounded-3xl shadow-2xl">
    Diagonal section creates dynamic movement
  </div>
</div>

<!-- Grid-breaking elements -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
  <div class="col-span-1">Normal card</div>
  <div class="col-span-2">Wide card breaking the grid</div>
  <div class="col-span-1">Normal card</div>
</div>

<!-- Generous negative space -->
<section class="min-h-[90vh] flex items-center justify-center">
  <div class="max-w-xl mx-auto text-center">
    <h1>Bold Statement</h1>
  </div>
</section>
```

### Backgrounds & Visual Details

```css
/* Gradient mesh */
.background {
  background:
    radial-gradient(at 40% 20%, rgba(196, 30, 58, 0.15) 0px, transparent 50%),
    radial-gradient(at 80% 0%, rgba(212, 160, 23, 0.15) 0px, transparent 50%),
    radial-gradient(at 0% 50%, rgba(59, 130, 246, 0.15) 0px, transparent 50%);
}

/* Noise texture */
.noise-overlay {
  position: fixed;
  inset: 0;
  pointer-events: none;
  opacity: 0.03;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
}

/* Geometric patterns */
.geometric-pattern {
  background-image:
    linear-gradient(rgba(196, 30, 58, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(196, 30, 58, 0.03) 1px, transparent 1px);
  background-size: 40px 40px;
}

/* Layered transparencies */
.layered-card {
  background: linear-gradient(135deg, rgba(255,255,255,0.1), rgba(255,255,255,0.05));
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255,255,255,0.1);
}

/* Dramatic shadows */
.dramatic-shadow {
  box-shadow:
    0 20px 40px -10px rgba(0,0,0,0.3),
    0 0 0 1px rgba(255,255,255,0.1) inset;
}

/* Decorative borders */
.decorative-border {
  position: relative;
}

.decorative-border::before {
  content: '';
  position: absolute;
  inset: -2px;
  background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
  border-radius: inherit;
  z-index: -1;
}

/* Custom cursor */
.custom-cursor {
  cursor: none;
}

.cursor-dot {
  width: 8px;
  height: 8px;
  background: var(--color-primary);
  border-radius: 50%;
  position: fixed;
  pointer-events: none;
  z-index: 9999;
}

/* Grain overlay */
.grain {
  position: fixed;
  inset: 0;
  pointer-events: none;
  opacity: 0.5;
  background-size: 200% 200%;
  animation: grain 8s steps(10) infinite;
}

@keyframes grain {
  0%, 100% { transform: translate(0, 0); }
  10% { transform: translate(-5%, -10%); }
  30% { transform: translate(3%, -15%); }
  50% { transform: translate(12%, 9%); }
  70% { transform: translate(9%, 4%); }
  90% { transform: translate(-1%, 7%); }
}
```

## Implementation Rules

### Match Complexity to Vision

```javascript
// ❌ WRONG: Minimalist code for maximalist vision
const MinimalComponent = () => (
  <div className="p-4">
    <h1>Title</h1>
  </div>
);

// ✅ CORRECT: Maximalist vision needs elaborate code
const MaximalistComponent = () => {
  const [mousePos, setMousePos] = useState({ x: 0, y: 0 });
  const [isVisible, setIsVisible] = useState(false);

  useEffect(() => {
    const handleMouseMove = (e) => {
      setMousePos({ x: e.clientX, y: e.clientY });
    };
    window.addEventListener('mousemove', handleMouseMove);
    return () => window.removeEventListener('mousemove', handleMouseMove);
  }, []);

  return (
    <div
      className="relative min-h-screen overflow-hidden bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900"
      onMouseEnter={() => setIsVisible(true)}
    >
      {/* Animated gradient mesh */}
      <div className="absolute inset-0 opacity-30">
        <div
          className="absolute w-[800px] h-[800px] rounded-full blur-3xl animate-pulse"
          style={{
            background: `radial-gradient(circle, rgba(139,92,246,0.6) 0%, transparent 70%)`,
            transform: `translate(${mousePos.x * 0.1}px, ${mousePos.y * 0.1}px)`,
          }}
        />
      </div>

      {/* Noise overlay */}
      <div className="absolute inset-0 opacity-5" style={{
        backgroundImage: 'url("data:image/svg+xml,%3Csvg...")'
      }} />

      {/* Geometric pattern */}
      <div className="absolute inset-0 opacity-10" style={{
        backgroundImage: 'linear-gradient(45deg, #333 25%, transparent 25%), ...',
        backgroundSize: '60px 60px'
      }} />

      {/* Content */}
      <div className="relative z-10 container mx-auto px-8 py-20">
        {/* Staggered animations */}
        <motion.h1
          initial={{ opacity: 0, y: 60 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 1, ease: [0.16, 1, 0.3, 1] }}
          className="text-7xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-pink-500 via-purple-500 to-cyan-500"
        >
          Maximalist Design
        </motion.h1>
      </div>
    </div>
  );
};
```

```javascript
// ✅ CORRECT: Refined minimalist vision needs restraint
const RefinedMinimalist = () => {
  return (
    <div className="min-h-screen bg-[#F8F5F0] flex items-center justify-center">
      <div className="max-w-2xl mx-auto px-8">
        <h1 className="text-[clamp(3rem,8vw,6rem)] font-[500] tracking-tight text-[#0F172A] leading-[0.95]">
          Precise
        </h1>
        <p className="text-xl text-[#64748B] mt-8 leading-relaxed max-w-md">
          Elegance comes from executing the vision well.
        </p>
      </div>
    </div>
  );
};
```

## Code Examples

### Brutalist/Raw Aesthetic

```html
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap');

  :root {
    --color-primary: #000000;
    --color-accent: #FF0000;
    --color-border: #000000;
  }

  body {
    font-family: 'Space Mono', monospace;
    background: white;
  }

  .brutalist-card {
    border: 4px solid var(--color-border);
    padding: 0;
    box-shadow: 12px 12px 0 var(--color-border);
    transition: all 0.2s ease;
  }

  .brutalist-card:hover {
    transform: translate(-4px, -4px);
    box-shadow: 16px 16px 0 var(--color-border);
  }

  .brutalist-btn {
    background: var(--color-accent);
    color: white;
    font-family: 'Space Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }
</style>

<div class="brutalist-card">
  <div class="p-8">
    <h2 class="text-3xl font-bold uppercase">Bold Statement</h2>
    <p class="mt-4 text-lg">Raw, unfiltered design that commands attention.</p>
    <button class="brutalist-btn px-6 py-4 mt-6">Take Action</button>
  </div>
</div>
```

### Luxury/Refined Aesthetic

```html
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Source+Sans+Pro:wght@300;400&display=swap');

  :root {
    --color-primary: #1A1A1A;
    --color-accent: #C9A87C;
    --color-surface: #FAFAF9;
  }

  body {
    font-family: 'Source Sans Pro', sans-serif;
    background: var(--color-surface);
  }

  .luxury-card {
    background: white;
    padding: 3rem;
    box-shadow:
      0 1px 3px rgba(0,0,0,0.04),
      0 4px 12px rgba(0,0,0,0.04);
  }

  h1, h2, h3 {
    font-family: 'Playfair Display', serif;
    font-weight: 400;
  }

  .elegant-border {
    border-top: 1px solid var(--color-accent);
  }
</style>

<div class="luxury-card">
  <div class="elegant-border pt-8">
    <h2 class="text-4xl text-[var(--color-primary)]">Sophisticated</h2>
    <p class="mt-6 text-[var(--color-primary)] leading-loose">
      Refined elegance through meticulous attention to detail.
    </p>
  </div>
</div>
```

### Retro-Futuristic Aesthetic

```html
<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@400;500&display=swap');

  :root {
    --color-primary: #00F0FF;
    --color-secondary: #FF006E;
    --color-bg: #0A0A0A;
  }

  body {
    font-family: 'Rajdhani', sans-serif;
    background: var(--color-bg);
  }

  .retro-future-card {
    background: linear-gradient(135deg, rgba(0,240,255,0.1), rgba(255,0,110,0.1));
    border: 2px solid var(--color-primary);
    padding: 2rem;
    position: relative;
  }

  .retro-future-card::before {
    content: '';
    position: absolute;
    inset: -4px;
    background: linear-gradient(45deg, var(--color-primary), var(--color-secondary), var(--color-primary));
    z-index: -1;
    filter: blur(10px);
  }

  h1, h2 {
    font-family: 'Orbitron', sans-serif;
  }
</style>

<div class="retro-future-card">
  <h2 class="text-3xl text-[var(--color-primary)] uppercase">Neon Dreams</h2>
  <p class="mt-4 text-xl text-[var(--color-secondary)]">
    Blending retro aesthetics with futuristic vision.
  </p>
</div>
```

## Important Reminders

- **Vary between light and dark themes** - Not every design should be dark mode
- **Different fonts across generations** - Don't converge on common choices (Space Grotesk, etc.)
- **Match complexity to vision** - Maximalist needs elaborate code, minimalist needs restraint
- **Creative execution** - Make unexpected choices that feel genuinely designed for the context
- **No design should be the same** - Each interface deserves its own unique character
- **Claude is capable** - Don't hold back, show what can truly be created when thinking outside the box
