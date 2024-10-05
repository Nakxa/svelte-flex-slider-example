# Svelte Flex Slider

**Svelte Flex Slider** is a versatile slider library for Svelte, allowing you to create beautiful and responsive image sliders, carousels, testimonial sliders, product showcases, and news tickers with ease.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Image Slider](#image-slider)
  - [Full-width Carousel](#full-width-carousel)
  - [Testimonial Slider](#testimonial-slider)
  - [Product Showcase](#product-showcase)
  - [News Ticker](#news-ticker)
- [Styling](#styling)
- [License](#license)

## Installation

To install the `svelte-flex-slider` library, use npm:

```bash
npm install svelte-flex-slider

```
Usage
Import the SvelteFlexSlider component in your Svelte file and pass the appropriate cards data. Here are examples of various slider types you can create:

Image Slider
```bash
<script>
  import SvelteFlexSlider from 'svelte-flex-slider';

  const cards = [
    '<div class="card-content"><img class="slider-img" src="img1.jpg" alt="Slide 1"></div>',
    // Add more slides...
  ];

  const responsiveCards = { default: 1, 520: 2, 800: 3 };
</script>

<div class="container">
  <h2>Image Slider</h2>
  <SvelteFlexSlider
    cards={cards}
    autoplay={true}
    interval={3000}
    loop={true}
    visibleCards={responsiveCards}
  />
</div>

```
Full-width Carousel
```bash
<script>
  const carousel_card = [
    '<div class="carousel-content"><img class="carousel-img" src="c-1.jpg" alt="Slide 1"></div>',
    // Add more carousel items...
  ];
</script>

<div class="container">
  <h2>Full-width Carousel</h2>
  <SvelteFlexSlider
    cards={carousel_card}
    autoplay={true}
    interval={5000}
    loop={true}
    visibleCards={{ default: 1 }}
  />
</div>

```
Testimonial Slider
```bash
<script>
  const testimonialCards = [
    '<div class="testimonial-card"><p>"This product changed my life!"</p><h4>John Doe</h4></div>',
    // Add more testimonials...
  ];
</script>

<div class="container">
  <h2>Testimonial Slider</h2>
  <SvelteFlexSlider
    cards={testimonialCards}
    autoplay={true}
    interval={4000}
    loop={true}
    visibleCards={{ default: 1, 800: 2 }}
  />
</div>

```
Product Showcase
```bash
<script>
  const productCards = [
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?product" alt="Product 1"><h3>Premium Widget</h3><p>$19.99</p></div>',
    // Add more products...
  ];
</script>

<div class="container">
  <h2>Product Showcase</h2>
  <SvelteFlexSlider
    cards={productCards}
    autoplay={false}
    interval={3000}
    loop={true}
    visibleCards={{ default: 1, 520: 2, 800: 3, 1200: 4 }}
  />
</div>
```


News Ticker
```bash
<script>
  const newsCards = [
    '<div class="news-card"><img src="https://source.unsplash.com/random/400x300?news" alt="News 1"><h3>Breaking News</h3><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p></div>',
    // Add more news items...
  ];
</script>

<div class="container">
  <h2>News Ticker</h2>
  <SvelteFlexSlider
    cards={newsCards}
    autoplay={true}
    interval={2000}
    loop={true}
    visibleCards={{ default: 1, 1000: 2 }}
  />
</div>
```
Styling
You can customize the styles for different slider types by modifying the provided CSS. Here are some examples of styles you can add:

```bash
:global(.card-content) {
  background-color: #f0f0f0;
  border: 1px solid #ddd;
  border-radius: 4px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 20px;
}

:global(.testimonial-card) {
  background-color: #f8f8f8;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
}

```
Feel free to customize the styling as per your project's design requirements.

License
This project is licensed under the MIT License - see the LICENSE file for details.

