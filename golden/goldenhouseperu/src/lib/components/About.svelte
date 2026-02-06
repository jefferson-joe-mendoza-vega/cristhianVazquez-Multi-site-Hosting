<script>
  import ScrollReveal from './ScrollReveal.svelte';
</script>

<section id="nosotros" class="about">
  <div class="container">
    <div class="about-grid">
      <ScrollReveal>
        <div class="about-image">
        <div class="image-placeholder">
          <img src="/fondo_sobre_nosotros.png" alt="Construcción Golden House" />
        </div>
        <div class="experience-badge">
          <div class="badge-number">15+</div>
          <div class="badge-text">Años de<br/>Experiencia</div>
        </div>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={100}>
        <div class="about-content">
        <span class="section-tag">SOBRE NOSOTROS</span>
        <h2>Construyendo Sueños, <span class="highlight">Creando Hogares</span></h2>
        <p class="about-intro">Golden House nació con la visión de transformar el sector inmobiliario, ofreciendo soluciones integrales que combinan diseño arquitectónico innovador con la más alta calidad de construcción.</p>
        <p>Nuestro equipo de profesionales expertos está comprometido con hacer realidad tu proyecto, desde la selección del terreno ideal hasta la entrega de tu hogar listo para disfrutar.</p>
        
        <div class="values-grid">
          <div class="value-item">
            <div class="value-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M12 2L2 7l10 5 10-5-10-5z"/>
                <path d="M2 17l10 5 10-5M2 12l10 5 10-5"/>
              </svg>
            </div>
            <div>
              <h4>Confianza</h4>
              <p>Transparencia y honestidad en cada transacción.</p>
            </div>
          </div>
          
          <div class="value-item">
            <div class="value-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M12 2v20M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/>
              </svg>
            </div>
            <div>
              <h4>Calidad</h4>
              <p>Materiales premium y acabados de primera.</p>
            </div>
          </div>
          
          <div class="value-item">
            <div class="value-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M16 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
                <circle cx="8.5" cy="7" r="4"/>
                <path d="M20 8v6M23 11h-6"/>
              </svg>
            </div>
            <div>
              <h4>Compromiso</h4>
              <p>Tu satisfacción es nuestra prioridad.</p>
            </div>
          </div>
        </div>
      </ScrollReveal>
    </div>
  </div>
</section>

<style>
  .about {
    padding: 6rem 0;
    background: white;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }
  
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }
  
  .about-image {
    position: relative;
  }
  
  .image-placeholder {
    width: 100%;
    height: 500px;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(0,0,0,0.15);
  }
  
  .image-placeholder img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }
  
  .experience-badge {
    position: absolute;
    bottom: 30px;
    right: 30px;
    background: linear-gradient(135deg, #c9a55c 0%, #b8944d 100%);
    padding: 2rem;
    border-radius: 12px;
    text-align: center;
    color: white;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  }
  
  .badge-number {
    font-size: 2.5rem;
    font-weight: 800;
    line-height: 1;
  }
  
  .badge-text {
    font-size: 0.9rem;
    margin-top: 0.5rem;
    line-height: 1.3;
  }
  
  .about-content {
    padding: 2rem 0;
  }
  
  .section-tag {
    color: #c9a55c;
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  
  .about-content h2 {
    font-size: clamp(2rem, 4vw, 2.8rem);
    color: #1a3a52;
    margin: 1rem 0 1.5rem;
    font-weight: 700;
    line-height: 1.3;
  }
  
  .highlight {
    color: #c9a55c;
  }
  
  .about-intro {
    font-size: 1.15rem;
    color: #495057;
    margin-bottom: 1rem;
    line-height: 1.8;
    font-weight: 500;
  }
  
  .about-content > p {
    color: #6c757d;
    line-height: 1.8;
    margin-bottom: 2rem;
  }
  
  .values-grid {
    display: grid;
    gap: 1.5rem;
    margin-top: 2.5rem;
  }
  
  .value-item {
    display: flex;
    gap: 1.5rem;
    align-items: flex-start;
    padding: 1.5rem;
    border-radius: 10px;
    background: #f8f9fa;
    transition: all 0.3s;
  }
  
  .value-item:hover {
    background: #fff;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    transform: translateX(10px);
  }
  
  .value-icon {
    width: 50px;
    height: 50px;
    background: linear-gradient(135deg, #c9a55c 0%, #b8944d 100%);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    flex-shrink: 0;
  }
  
  .value-icon svg {
    width: 26px;
    height: 26px;
  }
  
  .value-item h4 {
    color: #1a3a52;
    font-size: 1.2rem;
    margin-bottom: 0.3rem;
    font-weight: 600;
  }
  
  .value-item p {
    color: #6c757d;
    font-size: 0.95rem;
    line-height: 1.5;
    margin: 0;
  }
  
  @media (max-width: 968px) {
    .about {
      padding: 3.5rem 0;
    }
    
    .container {
      padding: 0 1.2rem;
    }
    
    .about-grid {
      grid-template-columns: 1fr;
      gap: 2.5rem;
    }
    
    .image-placeholder {
      height: 300px;
      border-radius: 10px;
    }
    
    .experience-badge {
      bottom: 15px;
      right: 15px;
      padding: 1.3rem 1.5rem;
      border-radius: 10px;
    }
    
    .badge-number {
      font-size: 1.8rem;
    }
    
    .badge-text {
      font-size: 0.8rem;
    }
    
    .about-content {
      padding: 0;
    }
    
    .section-tag {
      font-size: 0.75rem;
    }
    
    .about-content h2 {
      font-size: 1.8rem;
      margin: 0.8rem 0 1.2rem;
    }
    
    .about-intro {
      font-size: 0.95rem;
      margin-bottom: 1rem;
    }
    
    .about-content > p {
      font-size: 0.95rem;
    }
    
    .values-grid {
      gap: 1rem;
    }
    
    .value-item {
      padding: 1.5rem 1.2rem;
      flex-direction: row;
      text-align: left;
    }
    
    .value-icon {
      width: 40px;
      height: 40px;
      flex-shrink: 0;
    }
    
    .value-icon svg {
      width: 20px;
      height: 20px;
    }
    
    .value-item h4 {
      font-size: 1.1rem;
    }
    
    .value-item p {
      font-size: 0.9rem;
    }
    
    .value-item:hover {
      transform: translateX(0) translateY(-3px);
    }
  }
</style>
