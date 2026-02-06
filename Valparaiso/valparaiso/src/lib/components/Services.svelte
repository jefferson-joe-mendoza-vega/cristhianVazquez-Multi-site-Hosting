<script>
  import ScrollReveal from './ScrollReveal.svelte';
</script>

<section class="services">
  <div class="container">
    <ScrollReveal>
      <div class="section-header">
        <span class="section-tag">VENTAJAS DEL PROYECTO</span>
        <h2>Ladera Real <span class="highlight">La Colpa</span></h2>
        <p>Ubicación estratégica con todos los servicios y en zona de alto crecimiento.</p>
      </div>
    </ScrollReveal>
    
    <div class="services-grid">
      <ScrollReveal delay={100}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
            <polyline points="9 22 9 12 15 12 15 22"/>
          </svg>
        </div>
        <h3>Al Filo de Carretera</h3>
        <p>Acceso directo y fácil desde la vía principal, ideal para tu inversión.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={200}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
            <circle cx="12" cy="10" r="3"/>
          </svg>
        </div>
        <h3>Hacienda La Colpa</h3>
        <p>A espaldas de la icónica Hacienda La Colpa, zona turística consolidada.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={300}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/>
          </svg>
        </div>
        <h3>Servicios Básicos</h3>
        <p>Redes de agua y luz ya instaladas, listo para construir tu proyecto.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={400}>
        <div class="service-card">
          <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="2" y="7" width="20" height="14" rx="2" ry="2"/>
            <path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/>
          </svg>
        </div>
        <h3>Transporte Público</h3>
        <p>Línea de combis Ladera Real. Conexión directa con Cajamarca.</p>
        </div>
      </ScrollReveal>
    </div>
  </div>
</section>

<style>
  .services {
    padding: 5rem 0;
    background: linear-gradient(to bottom, #f8f9fa 0%, #ffffff 100%);
  }
  
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 1.5rem;
  }
  
  @media (max-width: 768px) {
    .services {
      padding: 3.5rem 0;
    }
    
    .container {
      padding: 0 1rem;
      max-width: 100%;
    }
    
    .section-header {
      margin-bottom: 2rem;
      padding: 0 0.5rem;
    }
    
    .section-tag {
      font-size: 0.7rem;
      letter-spacing: 1.5px;
    }
    
    .section-header h2 {
      font-size: 1.75rem;
      line-height: 1.3;
      margin: 0.7rem 0;
    }
    
    .section-header p {
      font-size: 0.9rem;
      padding: 0;
      line-height: 1.5;
    }
    
    .services-grid {
      grid-template-columns: 1fr !important;
      gap: 1.5rem;
      padding: 0;
    }
    
    .service-card {
      padding: 2.5rem 1.8rem;
      border-radius: 12px;
      max-width: 100%;
      margin: 0 auto;
      width: 100%;
    }
    
    .service-icon {
      width: 65px;
      height: 65px;
      margin: 0 auto 1.3rem;
      border-radius: 12px;
    }
    
    .service-icon svg {
      width: 32px;
      height: 32px;
    }
    
    .service-card h3 {
      font-size: 1.3rem;
      margin-bottom: 0.9rem;
      line-height: 1.3;
    }
    
    .service-card p {
      font-size: 0.95rem;
      line-height: 1.65;
      color: #6c757d;
    }
  }
  
  .section-header {
    text-align: center;
    margin-bottom: 4rem;
  }
  
  .section-tag {
    color: #E1BB6B;
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  
  .section-header h2 {
    font-size: clamp(2rem, 5vw, 3rem);
    color: #53564D;
    margin: 1rem 0;
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
    line-height: 1.6;
  }
  
  .services-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1.5rem;
  }
  
  @media (max-width: 1100px) {
    .services-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 1.5rem;
    }
  }
  
  @media (max-width: 768px) {
    .services-grid {
      grid-template-columns: 1fr !important;
      gap: 1.5rem;
      padding: 0;
    }
  }
  
  .service-card {
    background: white;
    padding: 2.5rem 2rem;
    border-radius: 12px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
    text-align: center;
    border: 1px solid rgba(225, 187, 107, 0.1);
  }
  
  .service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.15);
    border-color: #E1BB6B;
  }
  
  .service-icon {
    width: 70px;
    height: 70px;
    margin: 0 auto 1.5rem;
    background: linear-gradient(135deg, #E1BB6B 0%, #F0B452 100%);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    transition: all 0.3s;
  }
  
  .service-card:hover .service-icon {
    transform: scale(1.1) rotate(5deg);
  }
  
  .service-icon svg {
    width: 35px;
    height: 35px;
  }
  
  .service-card h3 {
    font-size: 1.4rem;
    color: #53564D;
    margin-bottom: 1rem;
    font-weight: 600;
  }
  
  .service-card p {
    color: #6c757d;
    line-height: 1.7;
    font-size: 1rem;
  }
</style>
