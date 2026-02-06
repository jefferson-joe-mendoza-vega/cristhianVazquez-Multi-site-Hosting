<script>
  import ScrollReveal from './ScrollReveal.svelte';
</script>

<section id="proyectos" class="projects">
  <div class="container">
    <ScrollReveal>
      <div class="section-header">
        <h2>Proyecto <span class="highlight">Ladera Real</span></h2>
        <p>Invierte en La Colpa, zona de alto crecimiento y plusvalía garantizada.</p>
      </div>
    </ScrollReveal>
    
    <div class="projects-grid">
      <ScrollReveal delay={100}>
        <div class="project-card">
        <div class="project-image">
          <div class="project-badge sale">Disponible</div>
          <img src="/santa_rosa.png" alt="Proyecto Ladera Real - La Colpa" />
        </div>
        <div class="project-content">
          <h3>Ladera Real</h3>
          <p class="project-location">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
              <circle cx="12" cy="10" r="3"/>
            </svg>
            La Colpa, Cajamarca
          </p>
          <div class="project-price">Desde S/ 30,000</div>
          <div class="project-features">
            <span>
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
              </svg>
              100-200 m²
            </span>
            <span>
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
              </svg>
              18% anual
            </span>
            <span>
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M9 11H7v2h2v-2zm4 0h-2v2h2v-2zm4 0h-2v2h2v-2zm2-7h-1V2h-2v2H8V2H6v2H5c-1.11 0-1.99.9-1.99 2L3 20c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 16H5V9h14v11z"/>
              </svg>
              Trato Directo
            </span>
          </div>
        </div>
        </div>
      </ScrollReveal>
    </div>
  </div>
</section>

<style>
  .projects {
    padding: 5rem 0;
    background: linear-gradient(to bottom, #ffffff 0%, #f8f9fa 100%);
  }
  
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 1.5rem;
  }
  
  @media (max-width: 768px) {
    .projects {
      padding: 3.5rem 0;
    }
    
    .container {
      padding: 0 1.2rem;
    }
    
    .section-header {
      margin-bottom: 2.5rem;
    }
    
    .section-header h2 {
      font-size: 1.8rem;
      margin-bottom: 0.8rem;
    }
    
    .section-header p {
      font-size: 0.95rem;
      padding: 0 0.5rem;
    }
    
    .projects-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
    
    .project-card {
      margin: 0;
    }
    
    .project-image {
      height: 220px;
    }
    
    .project-badge {
      top: 12px;
      right: 12px;
      padding: 0.4rem 0.9rem;
      font-size: 0.75rem;
    }
    
    .project-content {
      padding: 1.5rem 1.2rem;
    }
    
    .project-content h3 {
      font-size: 1.2rem;
      margin-bottom: 0.6rem;
    }
    
    .project-location {
      font-size: 0.85rem;
      margin-bottom: 0.8rem;
    }
    
    .project-price {
      font-size: 1.6rem;
      margin: 0.8rem 0;
    }
    
    .project-features {
      gap: 0.8rem;
      flex-wrap: wrap;
    }
    
    .project-features span {
      font-size: 0.85rem;
    }
  }
  
  .section-header {
    text-align: center;
    margin-bottom: 4rem;
  }
  
  .section-header h2 {
    font-size: clamp(2rem, 5vw, 3rem);
    color: #53564D;
    margin-bottom: 1rem;
    font-weight: 700;
  }
  
  .highlight {
    color: #E1BB6B;
  }
  
  .section-header p {
    color: #6c757d;
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto;
  }
  
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2.5rem;
  }
  
  .project-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
  }
  
  .project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.15);
  }
  
  .project-image {
    position: relative;
    height: 280px;
    overflow: hidden;
    background: #e9ecef;
  }
  
  .project-image svg {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }
  
  .project-card:hover .project-image svg {
    transform: scale(1.1);
  }
  
  .project-badge {
    position: absolute;
    top: 20px;
    left: 20px;
    padding: 0.5rem 1.2rem;
    border-radius: 25px;
    font-size: 0.85rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  .project-badge.sale {
    background: #E1BB6B;
    color: white;
  }
  
  .project-badge.available {
    background: #28a745;
    color: white;
  }
  
  .project-content {
    padding: 2rem;
  }
  
  .project-content h3 {
    font-size: 1.4rem;
    color: #53564D;
    margin-bottom: 0.8rem;
    font-weight: 600;
  }
  
  .project-location {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: #6c757d;
    font-size: 0.95rem;
    margin-bottom: 1rem;
  }
  
  .project-location svg {
    width: 18px;
    height: 18px;
  }
  
  .project-price {
    font-size: 1.8rem;
    color: #E1BB6B;
    font-weight: 700;
    margin-bottom: 1.2rem;
  }
  
  .project-features {
    display: flex;
    gap: 1.5rem;
    padding-top: 1rem;
    border-top: 1px solid #e9ecef;
  }
  
  .project-features span {
    display: flex;
    align-items: center;
    gap: 0.4rem;
    color: #495057;
    font-size: 0.95rem;
    font-weight: 500;
  }
  
  .project-features svg {
    width: 18px;
    height: 18px;
    color: #E1BB6B;
  }
</style>
