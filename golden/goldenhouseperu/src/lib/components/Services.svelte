<script>
  import ScrollReveal from './ScrollReveal.svelte';
</script>

<section class="services">
  <div class="container">
    <ScrollReveal>
      <div class="section-header">
        <span class="section-tag">NUESTROS SERVICIOS</span>
        <h2>Soluciones Inmobiliarias <span class="highlight">Integrales</span></h2>
        <p>Ofrecemos un portafolio completo de servicios para hacer realidad tu proyecto inmobiliario.</p>
      </div>
    </ScrollReveal>
    
    <div class="services-grid">
      <ScrollReveal delay={100}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 2L2 7v10c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V7l-10-5z"/>
            <circle cx="12" cy="11" r="3"/>
          </svg>
        </div>
        <h3>Venta de Terrenos</h3>
        <p>Terrenos urbanizados en las mejores ubicaciones, listos para construir tu proyecto ideal.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={200}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
            <polyline points="9 22 9 12 15 12 15 22"/>
          </svg>
        </div>
        <h3>Casas Residenciales</h3>
        <p>Diseños modernos y funcionales que combinan confort, elegancia y calidad de construcción.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={300}>
        <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="3" y="3" width="18" height="18" rx="2"/>
            <path d="M3 9h18M9 3v18"/>
          </svg>
        </div>
        <h3>Departamentos</h3>
        <p>Espacios contemporáneos con acabados premium y amenidades de primer nivel.</p>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={400}>
        <div class="service-card">
          <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/>
          </svg>
        </div>
        <h3>Construcción</h3>
        <p>Servicio integral de construcción con los más altos estándares de calidad y puntualidad.</p>
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
    color: #c9a55c;
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  
  .section-header h2 {
    font-size: clamp(2rem, 5vw, 3rem);
    color: #1a3a52;
    margin: 1rem 0;
    font-weight: 700;
  }
  
  .highlight {
    color: #c9a55c;
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
    border: 1px solid rgba(201, 165, 92, 0.1);
  }
  
  .service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.15);
    border-color: #c9a55c;
  }
  
  .service-icon {
    width: 70px;
    height: 70px;
    margin: 0 auto 1.5rem;
    background: linear-gradient(135deg, #c9a55c 0%, #b8944d 100%);
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
    color: #1a3a52;
    margin-bottom: 1rem;
    font-weight: 600;
  }
  
  .service-card p {
    color: #6c757d;
    line-height: 1.7;
    font-size: 1rem;
  }
</style>
