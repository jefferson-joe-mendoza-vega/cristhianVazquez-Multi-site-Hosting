<script>
  import { onMount } from 'svelte';
  
  let scrolled = false;
  let mobileMenuOpen = false;
  
  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 50;
    };
    
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
  
  function toggleMobileMenu() {
    mobileMenuOpen = !mobileMenuOpen;
  }
  
  function closeMobileMenu() {
    mobileMenuOpen = false;
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
{#if mobileMenuOpen}
  <div class="mobile-overlay" on:click={closeMobileMenu}></div>
{/if}

<header class:scrolled>
  <div class="container">
    <a href="#home" class="logo" on:click={closeMobileMenu}>
      <img src="/logo.png" alt="Inmobiliaria Valparaíso Logo" class="logo-img" />
    </a>
    
    <nav class:open={mobileMenuOpen}>
      <a href="#home" on:click={closeMobileMenu}>Home</a>
      <a href="#nosotros" on:click={closeMobileMenu}>Nosotros</a>
      <a href="#proyectos" on:click={closeMobileMenu}>Proyectos</a>
      <a href="#contacto" on:click={closeMobileMenu}>Contacto</a>
    </nav>
    
    <a href="https://wa.me/51978764181?text=Hola%2C%20me%20interesa%20el%20Proyecto%20Ladera%20Real" target="_blank" rel="noopener noreferrer" class="btn-cotizar desktop-only">Cotizar</a>
    
    <button class="mobile-menu-btn" on:click={toggleMobileMenu} aria-label="Menu">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        {#if mobileMenuOpen}
          <path d="M6 18L18 6M6 6l12 12"/>
        {:else}
          <path d="M3 12h18M3 6h18M3 18h18"/>
        {/if}
      </svg>
    </button>
  </div>
</header>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    padding: 1.2rem 0;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    background: rgba(83, 86, 77, 0.95);
    backdrop-filter: blur(10px);
  }
  
  header.scrolled {
    padding: 0.8rem 0;
    box-shadow: 0 4px 30px rgba(0,0,0,0.15);
    background: rgba(83, 86, 77, 0.98);
    transform: translateY(0);
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo {
    display: flex;
    align-items: center;
    text-decoration: none;
  }
  
  .logo-img {
    height: 50px;
    width: auto;
    object-fit: contain;
  }
  
  nav {
    display: flex;
    gap: 2.5rem;
  }
  
  nav a {
    color: white;
    text-decoration: none;
    font-weight: 400;
    font-size: 1rem;
    position: relative;
    transition: color 0.3s;
  }
  
  nav a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: #E1BB6B;
    transition: width 0.3s;
  }
  
  nav a:hover {
    color: #E1BB6B;
  }
  
  nav a:hover::after {
    width: 100%;
  }
  
  .btn-cotizar {
    background: #E1BB6B;
    color: white;
    border: none;
    padding: 0.8rem 2rem;
    border-radius: 5px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    font-size: 1rem;
    text-decoration: none;
    display: inline-block;
  }
  
  .btn-cotizar:hover {
    background: #F0B452;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(225, 187, 107, 0.3);
  }
  
  .mobile-menu-btn {
    display: none;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
    padding: 0.5rem;
    z-index: 1001;
  }
  
  .mobile-menu-btn svg {
    width: 28px;
    height: 28px;
  }
  
  .mobile-overlay {
    display: none;
  }
  
  @media (max-width: 968px) {
    header {
      padding: 1rem 0;
    }
    
    header.scrolled {
      padding: 0.8rem 0;
    }
    
    .container {
      padding: 0 1.2rem;
    }
    
    .logo-img {
      height: 40px;
    }
    
    nav {
      position: fixed;
      top: 0;
      right: -100%;
      width: 280px;
      max-width: 85%;
      height: 100vh;
      background: rgba(83, 86, 77, 0.98);
      backdrop-filter: blur(10px);
      flex-direction: column;
      justify-content: flex-start;
      align-items: stretch;
      gap: 0;
      transition: right 0.3s cubic-bezier(0.4, 0, 0.2, 1);
      padding: 5rem 0 2rem;
      box-shadow: -5px 0 20px rgba(0,0,0,0.3);
      z-index: 1002;
    }
    
    nav.open {
      right: 0;
    }
    
    nav a {
      font-size: 1.1rem;
      width: 100%;
      text-align: left;
      padding: 1.2rem 2rem;
      border-bottom: 1px solid rgba(255,255,255,0.1);
      transition: all 0.2s;
    }
    
    nav a:hover {
      background: rgba(225, 187, 107, 0.1);
      padding-left: 2.5rem;
    }
    
    nav a::after {
      display: none;
    }
    
    .mobile-overlay {
      display: block;
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1001;
      animation: fadeIn 0.3s ease;
    }
    
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    
    .desktop-only {
      display: none;
    }
    
    .mobile-menu-btn {
      display: block;
    }
  }
</style>
