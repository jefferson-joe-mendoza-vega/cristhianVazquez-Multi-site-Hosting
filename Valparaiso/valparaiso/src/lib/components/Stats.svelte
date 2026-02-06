<script>
  import ScrollReveal from './ScrollReveal.svelte';
</script>

<section class="stats">
  <div class="container">
    <div class="stats-grid">
      <ScrollReveal delay={0}>
        <div class="stat-item">
        <div class="stat-number">18%</div>
        <div class="stat-label">Plusvalía Anual Proyectada</div>
        </div>
      </ScrollReveal>
      <ScrollReveal delay={100}>
        <div class="stat-item">
        <div class="stat-number">100m²</div>
        <div class="stat-label">Lotes desde</div>
        </div>
      </ScrollReveal>
      <ScrollReveal delay={200}>
        <div class="stat-item">
        <div class="stat-number">60m</div>
        <div class="stat-label">De la Escuela La Colpa</div>
        </div>
      </ScrollReveal>
      <ScrollReveal delay={300}>
        <div class="stat-item">
        <div class="stat-number">400m</div>
        <div class="stat-label">Del futuro Mercado La Colpa</div>
        </div>
      </ScrollReveal>
    </div>
    <ScrollReveal delay={400}>
        <div class="stats-message">
        <p>Proyecto Ladera Real: Al filo de carretera, a espaldas de Hacienda La Colpa. Con redes de agua y luz. Transporte público Línea de combis Ladera Real. Inversión respaldada con trato directo.</p>
      </div>
    </ScrollReveal>
  </div>
</section>

<style>
  .stats {
    background: linear-gradient(135deg, #53564D 0%, #5F655B 100%);
    padding: 4rem 0;
    position: relative;
    overflow: hidden;
  }
  
  @media (max-width: 768px) {
    .stats {
      padding: 3rem 0;
    }
    
    .container {
      padding: 0 1.2rem;
    }
    
    .stats-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
      margin-bottom: 2rem;
    }
    
    .stat-item {
      padding: 1.8rem 1rem;
      border-radius: 10px;
    }
    
    .stat-number {
      font-size: 2.5rem !important;
      margin-bottom: 0.3rem;
    }
    
    .stat-label {
      font-size: 0.85rem;
      line-height: 1.3;
    }
    
    .stats-message {
      padding: 1.5rem 0.5rem 0;
    }
    
    .stats-message p {
      font-size: 0.95rem;
      line-height: 1.6;
    }
  }
  
  .stats::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120"><path d="M0,0 L1200,0 L1200,120 L0,60 Z" fill="%23f8f9fa"/></svg>');
    background-size: 100% 100%;
    transform: translateY(-100%);
  }
  
  .stats::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(circle at 70% 30%, rgba(225, 187, 107, 0.1) 0%, transparent 50%);
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }
  
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2rem;
    margin-bottom: 3rem;
  }
  
  @media (max-width: 1100px) {
    .stats-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 1.5rem;
    }
  }
  
  .stat-item {
    text-align: center;
    padding: 2rem 1rem;
    border-radius: 12px;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    transition: all 0.3s;
  }
  
  .stat-item:hover {
    transform: translateY(-5px);
    background: rgba(255, 255, 255, 0.08);
    border-color: rgba(225, 187, 107, 0.5);
  }
  
  .stat-number {
    font-size: clamp(2.5rem, 6vw, 4rem);
    font-weight: 800;
    background: linear-gradient(135deg, #E1BB6B 0%, #F0B452 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 0.5rem;
  }
  
  .stat-label {
    color: rgba(255, 255, 255, 0.9);
    font-size: 1.1rem;
    font-weight: 400;
  }
  
  .stats-message {
    text-align: center;
    padding-top: 2rem;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
  }
  
  .stats-message p {
    color: rgba(255, 255, 255, 0.85);
    font-size: 1.1rem;
    line-height: 1.8;
    max-width: 800px;
    margin: 0 auto;
  }
</style>
