<svelte:head>
  <title>The Playlist Boutique</title>
  <link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
</svelte:head>

<main class="app">
  <!-- Combined Hero Section with Background Image -->
  <section class="hero-section">
    <div class="hero-background">
      <!-- Background image spans both sections -->
    </div>

    <!-- Centered Content Container -->
    <div class="hero-content">
      <div class="text-container">
        <div class="title-wrapper">
          <h1 class="main-title">The Playlist Boutique</h1>
        </div>
        <div class="tagline-wrapper">
          <h2 class="tagline">Bespoke music curation for every occasion</h2>
        </div>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="testimonials">
    <div class="testimonials-container">
      <h2 class="section-title">What Our Clients Say</h2>
      <div class="testimonials-scroll">
        <div class="testimonial-card">
          <div class="testimonial-header">
            <div class="avatar">
              <div class="avatar-placeholder">JD</div>
            </div>
            <span class="client-name">Jack & Rachel</span>
          </div>
          <p class="testimonial-text">
            "The Playlist Boutique created the perfect wedding soundtrack for our special day.
            Every song choice was thoughtful and captured the essence of our love story."
          </p>
        </div>

        <div class="testimonial-card">
          <div class="testimonial-header">
            <div class="avatar">
              <div class="avatar-placeholder">MS</div>
            </div>
            <span class="client-name">Michael & Sarah</span>
          </div>
          <p class="testimonial-text">
            "Our corporate event was transformed by their curated playlists.
            The energy was perfect and kept our team engaged throughout the evening."
          </p>
        </div>

        <div class="testimonial-card">
          <div class="testimonial-header">
            <div class="avatar">
              <div class="avatar-placeholder">AL</div>
            </div>
            <span class="client-name">Anna & Liam</span>
          </div>
          <p class="testimonial-text">
            "From the first meeting to the final playlist, they understood exactly what we wanted.
            Professional, creative, and truly exceptional service."
          </p>
        </div>

        <div class="testimonial-card">
          <div class="testimonial-header">
            <div class="avatar">
              <div class="avatar-placeholder">RC</div>
            </div>
            <span class="client-name">Robert & Claire</span>
          </div>
          <p class="testimonial-text">
            "The attention to detail in curating our anniversary celebration playlist was remarkable.
            Every song told a chapter of our story together."
          </p>
        </div>
      </div>
    </div>
  </section>
</main>

<style>
  :global(*) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(body) {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    line-height: 1.6;
    color: #1a1a1a;
    background: #ffffff;
  }

  .app {
    min-height: 100vh;
  }

  /* Combined Hero Section */
  .hero-section {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .hero-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('./assets/11083879-3277-438f-a4bb-5d2d772f9578.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    z-index: 0;
  }

  .hero-background::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(0, 0, 0, 0.25) 0%, rgba(0, 0, 0, 0.5) 100%);
    z-index: 1;
  }

  .hero-content {
    position: relative;
    z-index: 2;
    text-align: center;
    max-width: 1200px;
    width: 100%;
    padding: 2rem;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    align-items: center;
  }

  .title-wrapper {
    position: relative;
    margin-bottom: 1.5rem;
  }

  .main-title {
    font-family: 'Libre Baskerville', serif;
    font-size: clamp(4rem, 8vw, 6rem);
    font-weight: 700;
    color: #ffffff;
    margin: 0;
    line-height: 1.1;
    letter-spacing: -0.02em;
    text-shadow:
      0 2px 4px rgba(0, 0, 0, 0.7),
      0 4px 8px rgba(0, 0, 0, 0.5),
      0 8px 16px rgba(0, 0, 0, 0.3),
      0 0 0 2px rgba(0, 0, 0, 0.8),
      0 0 0 4px rgba(0, 0, 0, 0.4),
      0 0 0 6px rgba(0, 0, 0, 0.2);
    -webkit-text-stroke: 1px rgba(0, 0, 0, 0.8);
    position: relative;
    display: inline-block;
  }

  .main-title::before {
    content: '';
    position: absolute;
    top: -10px;
    left: -10px;
    right: -10px;
    bottom: -10px;
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    z-index: -1;
  }

  .tagline-wrapper {
    margin-top: 1rem;
  }

  .tagline {
    font-family: 'Poppins', sans-serif;
    font-size: clamp(1.5rem, 3vw, 2.2rem);
    font-weight: 300;
    color: #ffffff;
    margin: 0;
    line-height: 1.4;
    text-shadow:
      0 2px 4px rgba(0, 0, 0, 0.6),
      0 4px 8px rgba(0, 0, 0, 0.4),
      0 0 0 1px rgba(0, 0, 0, 0.8);
    letter-spacing: 0.01em;
    opacity: 0.95;
  }

  /* Testimonials Section */
  .testimonials {
    padding: 6rem 2rem;
    background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
  }

  .testimonials-container {
    max-width: 1400px;
    margin: 0 auto;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 4vw, 3.5rem);
    font-weight: 700;
    color: #1a1a1a;
    text-align: center;
    margin-bottom: 4rem;
    letter-spacing: -0.02em;
  }

  .testimonials-scroll {
    display: flex;
    gap: 2rem;
    overflow-x: auto;
    padding: 1rem 0;
    scroll-snap-type: x mandatory;
    scrollbar-width: none;
    -ms-overflow-style: none;
  }

  .testimonials-scroll::-webkit-scrollbar {
    display: none;
  }

  .testimonial-card {
    background: #ffffff;
    border-radius: 20px;
    padding: 2.5rem;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08), 0 2px 8px rgba(0, 0, 0, 0.04);
    border: 1px solid #e2e8f0;
    transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    flex: 0 0 340px;
    scroll-snap-align: start;
    position: relative;
  }

  .testimonial-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12), 0 8px 16px rgba(0, 0, 0, 0.08);
  }

  .testimonial-card::before {
    content: '"';
    position: absolute;
    top: 1.5rem;
    left: 2rem;
    font-size: 4rem;
    color: #e2e8f0;
    font-family: 'Playfair Display', serif;
    line-height: 1;
  }

  .testimonial-header {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .avatar {
    width: 64px;
    height: 64px;
    border-radius: 50%;
    overflow: hidden;
    flex-shrink: 0;
    border: 3px solid #e2e8f0;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  }

  .avatar-placeholder {
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    color: #ffffff;
    font-weight: 700;
    font-size: 1.3rem;
    letter-spacing: 0.02em;
  }

  .client-name {
    font-weight: 600;
    color: #374151;
    font-size: 1.2rem;
    font-family: 'Inter', sans-serif;
  }

  .testimonial-text {
    color: #4b5563;
    font-size: 1.1rem;
    line-height: 1.7;
    margin: 0;
    font-style: italic;
    margin-top: 1rem;
    position: relative;
    z-index: 1;
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .hero {
      min-height: 80vh;
      padding: 1rem;
    }

    .main-title {
      font-size: clamp(2.5rem, 12vw, 4rem);
    }

    .tagline {
      font-size: clamp(1.5rem, 8vw, 2.5rem);
    }

    .tagline-section {
      height: 50vh;
      min-height: 300px;
    }

    .testimonials {
      padding: 3rem 1rem;
    }


    .testimonial-card {
      padding: 1.5rem;
    }
  }

  @media (max-width: 480px) {
    .hero-content {
      padding: 1rem;
    }

    .testimonials {
      padding: 2rem 1rem;
    }

    .section-title {
      font-size: 2rem;
    }
  }
</style>

