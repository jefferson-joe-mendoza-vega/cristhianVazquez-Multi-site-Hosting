<footer class="footer">
  <div class="container">
    <div class="footer-grid">
      <div class="footer-column">
        <a href="#home" class="footer-logo">
          <img src="/logo.png" alt="Inmobiliaria Valparaíso Logo" class="footer-logo-img" />
        </a>
        <p>Desarrolladora de proyectos con Alta Plusvalía. Agentes de Cambio Social comprometidos con tu futuro.</p>
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
          <li>Ladera Real - La Colpa, Cajamarca</li>
          <li><a href="tel:+51978764181" style="color: inherit; text-decoration: none;">Tel: +51 978 764 181</a></li>
          <li><a href="https://wa.me/51978764181?text=Hola%2C%20me%20interesa%20conocer%20más%20sobre%20el%20Proyecto%20Ladera%20Real" target="_blank" rel="noopener noreferrer" style="color: inherit; text-decoration: none;">WhatsApp: +51 978 764 181</a></li>
          <li><a href="mailto:contacto@inmobiliaria-valparaiso.com" style="color: inherit; text-decoration: none;">contacto@inmobiliaria-valparaiso.com</a></li>
        </ul>
      </div>
      
      <div class="footer-column">
        <h4>Síguenos</h4>
        <div class="social-links">
          <a href="https://web.facebook.com/profile.php?id=61573192016351" target="_blank" rel="noopener noreferrer" aria-label="Facebook">
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
            </svg>
          </a>
          <a href="https://www.instagram.com/inmobiliariavalparaiso" target="_blank" rel="noopener noreferrer" aria-label="Instagram">
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
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
      <p>&copy; 2025 Inmobiliaria Valparaíso. Todos los derechos reservados.</p>
    </div>
  </div>
</footer>

<style>
  .footer {
    background: linear-gradient(135deg, #53564D 0%, #5F655B 100%);
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
    background: radial-gradient(circle at 20% 80%, rgba(225, 187, 107, 0.1) 0%, transparent 50%);
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
    color: #E1BB6B;
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
    background: #E1BB6B;
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
    border-color: #E1BB6B;
  }
  
  .newsletter button {
    padding: 0.7rem 1.2rem;
    background: #E1BB6B;
    border: none;
    border-radius: 5px;
    color: white;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    font-size: 0.9rem;
  }
  
  .newsletter button:hover {
    background: #F0B452;
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
