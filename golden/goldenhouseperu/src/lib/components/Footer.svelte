<footer class="footer">
  <div class="container">
    <div class="footer-grid">
      <div class="footer-column">
        <a href="#home" class="footer-logo">
          <img src="/logo.png" alt="Golden House Logo" class="footer-logo-img" />
        </a>
        <p>Tu socio confiable en el sector inmobiliario y construcción. Más de 15 años creando hogares ideales.</p>
      </div>
      
      <div class="footer-column">
        <h4>Enlaces Rápidos</h4>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#nosotros">Nosotros</a></li>
          <li><a href="#proyectos">Proyectos</a></li>
          <li><a href="#contacto">Contacto</a></li>
        </ul>
      </div>
      
      <div class="footer-column">
        <h4>Contacto</h4>
        <ul class="contact-list">
          <li>Cajamarca, Perú</li>
          <li><a href="tel:+51915173349" style="color: inherit; text-decoration: none;">Tel: 915 173 349</a></li>
          <li><a href="https://wa.me/51913685917?text=Hola%2C%20me%20interesa%20conocer%20más%20sobre%20sus%20servicios" target="_blank" rel="noopener noreferrer" style="color: inherit; text-decoration: none;">WhatsApp: 913 685 917</a></li>
          <li><a href="mailto:info@goldenhouse.com.pe" style="color: inherit; text-decoration: none;">info@goldenhouse.com.pe</a></li>
        </ul>
      </div>
      
      <div class="footer-column">
        <h4>Síguenos</h4>
        <div class="social-links">
          <a href="https://web.facebook.com/profile.php?id=100076331190287" target="_blank" rel="noopener noreferrer" aria-label="Facebook">
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
            </svg>
          </a>
        </div>
        
        <div class="newsletter">
          <h4>Boletín</h4>
          <p>Suscríbete para recibir novedades exclusivas.</p>
          <form on:submit|preventDefault={() => alert('¡Gracias por suscribirte!')}>
            <input type="email" placeholder="Tu email" required />
            <button type="submit">Suscribirme</button>
          </form>
        </div>
      </div>
    </div>
    
    <div class="footer-bottom">
      <p>&copy; 2025 Golden House Inmobiliaria y Construcción. Todos los derechos reservados.</p>
    </div>
  </div>
</footer>

<style>
  .footer {
    background: linear-gradient(135deg, #1a3a52 0%, #2d5973 100%);
    color: white;
    padding: 4rem 0 2rem;
    position: relative;
    overflow: hidden;
  }
  
  .footer::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(circle at 20% 80%, rgba(201, 165, 92, 0.1) 0%, transparent 50%);
    pointer-events: none;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }
  
  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1.5fr;
    gap: 3rem;
    margin-bottom: 3rem;
    padding-bottom: 3rem;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  }
  
  .footer-logo {
    display: inline-block;
    margin-bottom: 1.5rem;
    text-decoration: none;
  }
  
  .footer-logo-img {
    height: 45px;
    width: auto;
    object-fit: contain;
  }
  
  .footer-column p {
    color: rgba(255, 255, 255, 0.8);
    line-height: 1.8;
    font-size: 0.95rem;
  }
  
  .footer-column h4 {
    font-size: 1.2rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }
  
  .footer-column ul {
    list-style: none;
    padding: 0;
  }
  
  .footer-column ul li {
    margin-bottom: 0.8rem;
  }
  
  .footer-column ul li a {
    color: rgba(255, 255, 255, 0.8);
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .footer-column ul li a:hover {
    color: #c9a55c;
  }
  
  .contact-list li {
    color: rgba(255, 255, 255, 0.8);
    line-height: 1.8;
  }
  
  .social-links {
    display: flex;
    gap: 1rem;
    margin-bottom: 2.5rem;
  }
  
  .social-links a {
    width: 40px;
    height: 40px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    transition: all 0.3s;
  }
  
  .social-links a:hover {
    background: #c9a55c;
    transform: translateY(-3px);
  }
  
  .social-links svg {
    width: 20px;
    height: 20px;
  }
  
  .newsletter h4 {
    font-size: 1rem;
    margin-bottom: 0.5rem;
  }
  
  .newsletter p {
    font-size: 0.9rem;
    margin-bottom: 1rem;
  }
  
  .newsletter form {
    display: flex;
    gap: 0.5rem;
  }
  
  .newsletter input {
    flex: 1;
    padding: 0.7rem;
    border: 1px solid rgba(255, 255, 255, 0.2);
    background: rgba(255, 255, 255, 0.1);
    border-radius: 5px;
    color: white;
    font-size: 0.9rem;
  }
  
  .newsletter input::placeholder {
    color: rgba(255, 255, 255, 0.5);
  }
  
  .newsletter input:focus {
    outline: none;
    border-color: #c9a55c;
  }
  
  .newsletter button {
    padding: 0.7rem 1.2rem;
    background: #c9a55c;
    border: none;
    border-radius: 5px;
    color: white;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    font-size: 0.9rem;
  }
  
  .newsletter button:hover {
    background: #b8944d;
  }
  
  .footer-bottom {
    text-align: center;
    padding-top: 2rem;
  }
  
  .footer-bottom p {
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
  }
  
  @media (max-width: 968px) {
    .footer {
      padding: 3rem 0 1.5rem;
    }
    
    .container {
      padding: 0 1.5rem;
    }
    
    .footer-grid {
      grid-template-columns: 1fr;
      gap: 2.5rem;
      padding-bottom: 2rem;
      margin-bottom: 2rem;
    }
    
    .footer-column h4 {
      font-size: 1.1rem;
      margin-bottom: 1rem;
    }
    
    .newsletter form {
      flex-direction: column;
    }
    
    .newsletter input,
    .newsletter button {
      width: 100%;
    }
  }
</style>
