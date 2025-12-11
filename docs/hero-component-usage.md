# Hero Component Usage Guide

The Hero component is now fully reusable and configurable through props. Here's how to use it:

## Basic Usage

```astro
---
import Hero from '../components/sections/Hero.astro';
---

<Hero
  title="Your Title"
  description="Your description here"
/>
```

## All Available Props

### Required Props
- `title` (string): The main title text
- `description` (string): The descriptive text below the title

### Optional Props

#### Section Configuration
- `sectionId` (string, default: "inicio"): ID for the section element

#### Text Content
- `titleHighlight` (string): Text to highlight with amber color
- `title` (string): Main title text (required)
- `description` (string): Description text (required)

#### Visual Configuration
- `backgroundGradient` (string, default: "bg-linear-to-br from-red-900 to-red-700"): CSS classes for background gradient
- `backgroundImage` (string, default: "/compresor_hero.png"): URL for background image
- `backgroundImageAlt` (string, default: "Fondo del compresor"): Alt text for background image
- `productImage` (string, default: "/compresor_hero.png"): URL for product image
- `productImageAlt` (string, default: "Compresor Industrial de Alta Calidad"): Alt text for product image

#### CTA Configuration
- `ctaText` (string, default: "Contactar por WhatsApp"): Text for the call-to-action button
- `ctaHref` (string, default: WhatsApp link): URL for the CTA button
- `showCTA` (boolean, default: true): Whether to show the CTA button

#### Layout Options
- `showProductImage` (boolean, default: true): Whether to show the product image
- `showBackgroundImage` (boolean, default: true): Whether to show the background image

#### Animation Options
- `enableAnimations` (boolean, default: true): Whether to enable fade-in animations

## Examples

### Example 1: Default Configuration
```astro
<Hero
  title="Producción Ininterrumpida"
  titleHighlight="Garantizada"
  description="Sistemas de aire comprimido que eliminan la incertidumbre."
/>
```

### Example 2: Minimal Hero (No CTA, No Product Image)
```astro
<Hero
  title="Simple Hero"
  description="A minimal hero section without extra elements."
  showCTA={false}
  showProductImage={false}
/>
```

### Example 3: Custom Styled Hero
```astro
<Hero
  title="Custom Style"
  titleHighlight="Blue Theme"
  description="Hero with custom blue gradient theme."
  backgroundGradient="bg-linear-to-br from-blue-900 to-blue-700"
  ctaText="Get Started"
  ctaHref="/contact"
  showBackgroundImage={false}
/>
```

### Example 4: Hero Without Animations
```astro
<Hero
  title="Static Hero"
  description="Hero with no animations for faster loading."
  enableAnimations={false}
/>
```

### Example 5: Full Customization
```astro
<Hero
  sectionId="custom-hero"
  title="Fully Customized"
  titleHighlight="Hero"
  description="This hero uses all the customization options available."
  backgroundGradient="bg-linear-to-br from-purple-900 to-pink-700"
  backgroundImage="/custom-bg.jpg"
  backgroundImageAlt="Custom background"
  productImage="/custom-product.png"
  productImageAlt="Custom product"
  ctaText="Learn More"
  ctaHref="/learn-more"
  showCTA={true}
  showProductImage={true}
  showBackgroundImage={true}
  enableAnimations={true}
/>
```

## Notes
- All images should be placed in the `public/` directory
- The component maintains responsive design and accessibility features
- Conditional rendering is used for optional elements to optimize performance