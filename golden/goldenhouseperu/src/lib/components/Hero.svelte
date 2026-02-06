<script>
  import { onMount } from 'svelte';
  
  let isVisible = false;
  
  onMount(() => {
    setTimeout(() => {
      isVisible = true;
    }, 100);
  });
</script>

<section id="home" class="hero">
  <div class="hero-overlay"></div>
  <div class="container" class:visible={isVisible}>
    <h1 class="hero-title">CONSTRUIMOS TU FUTURO</h1>
    <p class="hero-subtitle">Inmobiliaria y Construcción de excelencia. Tu hogar ideal te espera.</p>
    <div class="hero-buttons">
      <a href="#proyectos" class="btn-primary">Ver Proyectos</a>
      <a href="https://wa.me/51913685917?text=Hola%2C%20me%20interesa%20conocer%20más%20sobre%20sus%20servicios" target="_blank" rel="noopener noreferrer" class="btn-secondary">Contactar</a>
    </div>
  </div>
  <div class="scroll-indicator">
    <div class="mouse">
      <div class="wheel"></div>
    </div>
  </div>
</section>

<style>
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image: 
      linear-gradient(135deg, rgba(26, 58, 82, 0.5) 0%, rgba(45, 89, 115, 0.4) 100%),
      url('/fondo.png');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    padding-top: 80px;
    overflow: hidden;
  }
  
  .hero-overlay {
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 30% 50%, rgba(201, 165, 92, 0.1) 0%, transparent 50%);
  }
  
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 1.5rem;
    text-align: center;
    position: relative;
    z-index: 1;
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.8s ease-out, transform 0.8s ease-out;
  }
  
  .container.visible {
    opacity: 1;
    transform: translateY(0);
  }
  
  @media (max-width: 768px) {
    .hero {
      min-height: 100vh;
      padding: 80px 0 40px;
      background-attachment: scroll;
      background-position: center center;
    }
    
    .container {
      padding: 0 1.5rem;
    }
    
    .hero-title {
      font-size: 2.2rem !important;
      letter-spacing: 2px;
      line-height: 1.2;
      margin-bottom: 1.2rem;
    }
    
    .hero-subtitle {
      font-size: 1rem !important;
      margin-bottom: 2.5rem;
      line-height: 1.6;
      padding: 0 0.5rem;
    }
    
    .hero-buttons {
      flex-direction: column;
      width: 100%;
      gap: 1rem;
      align-items: center;
    }
    
    .btn-primary, .btn-secondary {
      width: 100%;
      max-width: 280px;
      padding: 1rem 2rem;
      font-size: 1rem;
      font-weight: 600;
    }
    
    .scroll-indicator {
      display: none;
    }
  }
  
  .hero-title {
    font-size: clamp(2.5rem, 8vw, 4.5rem);
    font-weight: 800;
    color: white;
    margin-bottom: 1.5rem;
    letter-spacing: 3px;
    text-shadow: 0 4px 20px rgba(0,0,0,0.3);
    animation: fadeInUp 1s ease-out;
  }
  
  .hero-subtitle {
    font-size: clamp(1.1rem, 2.5vw, 1.4rem);
    color: rgba(255, 255, 255, 0.95);
    margin-bottom: 3rem;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.6;
    animation: fadeInUp 1s ease-out 0.2s both;
  }
  
  .hero-buttons {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
    flex-wrap: wrap;
    animation: fadeInUp 1s ease-out 0.4s both;
  }
  
  .btn-primary, .btn-secondary {
    padding: 1rem 2.5rem;
    font-size: 1.1rem;
    font-weight: 600;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    text-decoration: none;
    display: inline-block;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  }
  
  .btn-primary {
    background: #c9a55c;
    color: white;
  }
  
  .btn-primary:hover {
    background: #b8944d;
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(201, 165, 92, 0.4);
  }
  
  .btn-secondary {
    background: transparent;
    color: white;
    border: 2px solid white;
  }
  
  .btn-secondary:hover {
    background: white;
    color: #1a3a52;
    transform: translateY(-3px);
  }
  
  .scroll-indicator {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    animation: fadeInUp 1s ease-out 0.6s both;
  }
  
  .mouse {
    width: 26px;
    height: 40px;
    border: 2px solid rgba(255, 255, 255, 0.7);
    border-radius: 20px;
    position: relative;
  }
  
  .wheel {
    width: 4px;
    height: 8px;
    background: rgba(255, 255, 255, 0.7);
    border-radius: 2px;
    position: absolute;
    top: 8px;
    left: 50%;
    transform: translateX(-50%);
    animation: scroll 2s infinite;
  }
  
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes scroll {
    0% {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }
    100% {
      opacity: 0;
      transform: translateX(-50%) translateY(15px);
    }
  }
</style>
