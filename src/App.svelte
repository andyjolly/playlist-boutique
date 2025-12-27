<svelte:head>
  <title>Playlist Boutique</title>
</svelte:head>

<main class="hero">
  <section class="card">
    <p class="eyebrow">Coming soon</p>
    <h1>Playlist Boutique</h1>
    <p class="lede">
      A curated one-pager to showcase your brand. This is the starter view—
      we’ll replace it with the real layout next.
    </p>
    <div class="cta-row">
      <button class="cta primary">View demo</button>
      <button class="cta ghost">Get in touch</button>
    </div>
  </section>
</main>

<style>
  .hero {
    display: grid;
    place-items: center;
    min-height: 100vh;
    padding: 2.5rem 1.5rem;
    background: radial-gradient(circle at 10% 20%, #dbeafe 0, transparent 25%),
      radial-gradient(circle at 80% 0%, #fef9c3 0, transparent 20%),
      radial-gradient(circle at 50% 80%, #f5f3ff 0, transparent 30%),
      #f8fafc;
  }

  .card {
    width: min(720px, 100%);
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 20px;
    padding: 2rem;
    box-shadow:
      0 12px 40px rgba(15, 23, 42, 0.12),
      0 2px 8px rgba(15, 23, 42, 0.08);
  }

  .eyebrow {
    display: inline-block;
    font-size: 0.875rem;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    color: #2563eb;
    background: #e0e7ff;
    border-radius: 999px;
    padding: 0.35rem 0.75rem;
    margin-bottom: 0.75rem;
  }

  h1 {
    font-size: clamp(2rem, 3vw + 1rem, 3rem);
    margin: 0 0 0.75rem;
    color: #0f172a;
    line-height: 1.1;
  }

  .lede {
    margin: 0 0 1.5rem;
    color: #334155;
    font-size: 1.05rem;
    line-height: 1.6;
  }

  .cta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .cta {
    border: 1px solid #2563eb;
    border-radius: 12px;
    padding: 0.75rem 1.1rem;
    font-weight: 600;
    cursor: pointer;
    transition: transform 120ms ease, box-shadow 120ms ease, background 120ms ease;
    font-size: 1rem;
  }

  .cta.primary {
    background: #2563eb;
    color: #fff;
    box-shadow: 0 8px 24px rgba(37, 99, 235, 0.35);
  }

  .cta.primary:hover {
    transform: translateY(-1px);
    box-shadow: 0 10px 28px rgba(37, 99, 235, 0.4);
  }

  .cta.ghost {
    background: #fff;
    color: #2563eb;
  }

  .cta.ghost:hover {
    background: #eff6ff;
  }

  @media (max-width: 600px) {
    .card {
      padding: 1.5rem;
    }

    .cta-row {
      flex-direction: column;
    }

    .cta {
      width: 100%;
      text-align: center;
    }
  }
</style>

