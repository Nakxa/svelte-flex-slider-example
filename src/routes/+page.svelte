<script>
  import SvelteFlexSlider from 'svelte-flex-slider';

  
  // Existing sliders
  const cards = [
    '<div class="card-content"> <img class="slider-img" src="img1.jpg" alt="Slide 1"> </div>',
    '<div class="card-content"> <img class="slider-img" src="img2.jpg" alt="Slide 2"></div>',
    '<div class="card-content"> <img class="slider-img" src="img3.jpg" alt="Slide 3"></div>',
    '<div class="card-content"> <img class="slider-img" src="img4.jpg" alt="Slide 4"></div>',
    '<div class="card-content"> <img class="slider-img" src="img5.jpg" alt="Slide 5"></div>',
    '<div class="card-content"> <img class="slider-img" src="img6.jpg" alt="Slide 6"> </div>',
    '<div class="card-content"> <img class="slider-img" src="img7.jpg" alt="Slide 7"></div>',
    '<div class="card-content"> <img class="slider-img" src="img8.jpg" alt="Slide 8"></div>',
  ];
  const carousel_card = [
    '<div class="carousel-content"> <img class="carousel-img" src="c-1.jpg" alt="Slide 1"> </div>',
    '<div class="carousel-content"> <img class="carousel-img" src="c-2.jpg" alt="Slide 1"> </div>',
    '<div class="carousel-content"> <img class="carousel-img" src="c-3.jpg" alt="Slide 1"> </div>',
    '<div class="carousel-content"> <img class="carousel-img" src="c-4.jpg" alt="Slide 1"> </div>',
    '<div class="carousel-content"> <img class="carousel-img" src="c-5.jpg" alt="Slide 1"> </div>',
  ];

  // New slider types
  const testimonialCards = [
    '<div class="testimonial-card"><p>"This product changed my life!"</p><h4>John Doe</h4></div>',
    '<div class="testimonial-card"><p>"I can\'t imagine working without it."</p><h4>Jane Smith</h4></div>',
    '<div class="testimonial-card"><p>"Absolutely phenomenal service!"</p><h4>Bob Johnson</h4></div>',
    '<div class="testimonial-card"><p>"The best in the business, hands down."</p><h4>Alice Brown</h4></div>',
  ];

  const productCards = [
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?product" alt="Product 1"><h3>Premium Widget</h3><p>$19.99</p></div>',
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?gadget" alt="Product 2"><h3>Super Gadget</h3><p>$29.99</p></div>',
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?tech" alt="Product 3"><h3>Tech Marvel</h3><p>$39.99</p></div>',
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?device" alt="Product 4"><h3>Smart Device</h3><p>$49.99</p></div>',
    '<div class="product-card"><img src="https://source.unsplash.com/random/300x300?electronics" alt="Product 5"><h3>Eco Friendly</h3><p>$59.99</p></div>',
  ];

  const newsCards = [
    '<div class="news-card"><img src="https://source.unsplash.com/random/400x300?news" alt="News 1"><h3>Breaking News</h3><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p></div>',
    '<div class="news-card"><img src="https://source.unsplash.com/random/400x300?article" alt="News 2"><h3>Tech Update</h3><p>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p></div>',
    '<div class="news-card"><img src="https://source.unsplash.com/random/400x300?headline" alt="News 3"><h3>World Affairs</h3><p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris.</p></div>',
    '<div class="news-card"><img src="https://source.unsplash.com/random/400x300?report" alt="News 4"><h3>Science Discovery</h3><p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum.</p></div>',
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

<div class="container">
  <h2>Full-width Carousel</h2>
  <SvelteFlexSlider
    cards={carousel_card}
    autoplay={true}
    interval={5000}
    loop={true}
    visibleCards={{default: 1}}
  />
</div>

<div class="container">
  <h2>Testimonial Slider</h2>
  <SvelteFlexSlider
    cards={testimonialCards}
    autoplay={true}
    interval={4000}
    loop={true}
    visibleCards={{default: 1, 800: 2}}
  />
</div>

<div class="container">
  <h2>Product Showcase</h2>
  <SvelteFlexSlider
    cards={productCards}
    autoplay={false}
    interval={3000}
    loop={true}
    visibleCards={{default: 1, 520: 2, 800: 3, 1200: 4}}
  />
</div>

<div class="container">
  <h2>News Ticker</h2>
  <SvelteFlexSlider
    cards={newsCards}
    autoplay={true}
    interval={2000}
    loop={true}
    visibleCards={{default: 1, 1000: 2}}
  />
</div>

<style>
  /* Existing styles */
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(*) {
    margin: 0;
    padding: 0;box-sizing: border-box;
  }
  :global(.card-content) {
    background-color: #f0f0f0;
    border: 1px solid #ddd;
    border-radius: 4px;
    /* padding: 20px; */
    text-align: center;
    /* height: 300px; */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 20px;
  }
  :global(.carousel-content) {
    background-color: #f0f0f0;
    border: 1px solid #ddd;
    border-radius: 4px;
    /* padding: 20px; */
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    
  }
  :global(.slider-img) {
    width: 100%;
    border-radius: 4px;
    height: 100%;
    object-fit: contain;
  }
  :global(.carousel-img) {
    width: 100%;
    border-radius: 4px;
    height: 100%;
    object-fit: contain;
  }
  
  
  .container {
    width: 80%;
    margin: 40px auto;
  }
  
  h2 {
    margin-bottom: 20px;
    color: #333;
  }

  /* New styles for different slider types */
  :global(.testimonial-card) {
    background-color: #f8f8f8;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    height: 200px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 10px;
  }

  :global(.testimonial-card p) {
    font-style: italic;
    margin-bottom: 10px;
  }

  :global(.product-card) {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    padding: 20px;
    text-align: center;
    margin: 10px;
  }

  :global(.product-card img) {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 4px;
    margin-bottom: 10px;
  }

  :global(.news-card) {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    overflow: hidden;
    margin: 10px;
  }

  :global(.news-card img) {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  :global(.news-card h3, .news-card p) {
    padding: 10px;
  }
</style>