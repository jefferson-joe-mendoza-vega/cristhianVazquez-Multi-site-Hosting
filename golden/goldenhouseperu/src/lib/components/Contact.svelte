<script>
  import ScrollReveal from './ScrollReveal.svelte';
  
  let formData = {
    nombre: '',
    telefono: '',
    email: '',
    interes: 'Comprar Propiedad',
    mensaje: ''
  };
  
  function handleSubmit(e) {
    e.preventDefault();
    const mensaje = `Hola, soy ${formData.nombre}%0A%0ATeléfono: ${formData.telefono}%0AEmail: ${formData.email}%0AInterés: ${formData.interes}%0A%0AMensaje: ${formData.mensaje}`;
    window.open(`https://wa.me/51913685917?text=${mensaje}`, '_blank');
    formData = { nombre: '', telefono: '', email: '', interes: 'Comprar Propiedad', mensaje: '' };
  }
</script>

<section id="contacto" class="contact">
  <div class="container">
    <ScrollReveal>
      <div class="section-header">
        <span class="section-tag">CONTÁCTANOS</span>
        <h2>¿Listo para <span class="highlight">Comenzar?</span></h2>
        <p>Estamos aquí para ayudarte a encontrar la propiedad perfecta. Contáctanos hoy.</p>
      </div>
    </ScrollReveal>
    
    <div class="contact-grid">
      <ScrollReveal delay={100}>
        <div class="contact-info">
        <div class="info-card">
          <h3>Empecemos a construir tu sueño</h3>
          <p>Agenda una cita con nuestros asesores inmobiliarios para recibir información personalizada sobre nuestros proyectos.</p>
          
          <div class="info-items">
            <div class="info-item">
              <div class="info-icon">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
                  <circle cx="12" cy="10" r="3"/>
                </svg>
              </div>
              <div>
                <h4>Oficina Principal</h4>
                <p>Cajamarca, Perú</p>
              </div>
            </div>
            
            <div class="info-item">
              <div class="info-icon">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
                </svg>
              </div>
              <div>
                <h4>Teléfonos</h4>
                <p><a href="tel:+51915173349" style="color: inherit;">915 173 349</a><br/>
                <a href="https://wa.me/51913685917?text=Hola%2C%20me%20interesa%20conocer%20más%20sobre%20sus%20servicios" target="_blank" rel="noopener noreferrer" style="color: inherit;">WhatsApp: 913 685 917</a></p>
              </div>
            </div>
            
            <div class="info-item">
              <div class="info-icon">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
                  <polyline points="22,6 12,13 2,6"/>
                </svg>
              </div>
              <div>
                <h4>Email</h4>
                <p><a href="mailto:info@goldenhouse.com.pe" style="color: inherit;">info@goldenhouse.com.pe</a></p>
              </div>
            </div>
          </div>
          
          <div class="map-placeholder">
            <svg viewBox="0 0 400 200" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect fill="#e9ecef" width="400" height="200"/>
              <circle cx="200" cy="100" r="30" fill="#c9a55c" opacity="0.5"/>
              <path d="M200 70 L200 100" stroke="#1a3a52" stroke-width="2"/>
              <circle cx="200" cy="70" r="8" fill="#1a3a52"/>
              <text x="200" y="150" text-anchor="middle" fill="#6c757d" font-size="14">Cajamarca, Perú</text>
              <text x="200" y="170" text-anchor="middle" fill="#6c757d" font-size="12" opacity="0.7">Mapa interactivo</text>
            </svg>
          </div>
        </div>
      </ScrollReveal>
      
      <ScrollReveal delay={200}>
        <div class="contact-form-wrapper">
          <div class="form-card">
          <h3>Envíanos un mensaje</h3>
          <form on:submit={handleSubmit}>
            <div class="form-row">
              <div class="form-group">
                <label for="nombre">NOMBRE</label>
                <input type="text" id="nombre" placeholder="Tu nombre" bind:value={formData.nombre} required />
              </div>
              <div class="form-group">
                <label for="telefono">TELÉFONO</label>
                <input type="tel" id="telefono" placeholder="+51 999 999 999" bind:value={formData.telefono} required />
              </div>
            </div>
            
            <div class="form-group">
              <label for="email">EMAIL</label>
              <input type="email" id="email" placeholder="tuemail@ejemplo.com" bind:value={formData.email} required />
            </div>
            
            <div class="form-group">
              <label for="interes">INTERÉS</label>
              <select id="interes" bind:value={formData.interes}>
                <option>Comprar Propiedad</option>
                <option>Vender Propiedad</option>
                <option>Construcción</option>
                <option>Asesoría</option>
                <option>Otro</option>
              </select>
            </div>
            
            <div class="form-group">
              <label for="mensaje">MENSAJE</label>
              <textarea id="mensaje" rows="5" placeholder="¿Cómo podemos ayudarte?" bind:value={formData.mensaje} required></textarea>
            </div>
            
            <button type="submit" class="btn-submit">ENVIAR MENSAJE</button>
          </form>
        </div>
        </div>
      </ScrollReveal>
    </div>
  </div>
</section>

<style>
  .contact {
    padding: 5rem 0;
    background: linear-gradient(to bottom, #f8f9fa 0%, #ffffff 100%);
  }
  
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 1.5rem;
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
  }
  
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
  }
  
  .info-card {
    background: linear-gradient(135deg, #1a3a52 0%, #2d5973 100%);
    padding: 3rem 2.5rem;
    border-radius: 12px;
    color: white;
    height: 100%;
  }
  
  .info-card h3 {
    font-size: 1.8rem;
    margin-bottom: 1rem;
    font-weight: 700;
  }
  
  .info-card > p {
    color: rgba(255, 255, 255, 0.85);
    line-height: 1.7;
    margin-bottom: 2.5rem;
  }
  
  .info-items {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    margin-bottom: 2.5rem;
  }
  
  .info-item {
    display: flex;
    gap: 1.5rem;
    align-items: flex-start;
  }
  
  .info-icon {
    width: 50px;
    height: 50px;
    background: rgba(201, 165, 92, 0.2);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #c9a55c;
    flex-shrink: 0;
  }
  
  .info-icon svg {
    width: 24px;
    height: 24px;
  }
  
  .info-item h4 {
    font-size: 1.1rem;
    margin-bottom: 0.5rem;
    font-weight: 600;
  }
  
  .info-item p {
    color: rgba(255, 255, 255, 0.8);
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  .map-placeholder {
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 20px rgba(0,0,0,0.3);
  }
  
  .map-placeholder svg {
    width: 100%;
    height: auto;
  }
  
  .form-card {
    background: white;
    padding: 3rem 2.5rem;
    border-radius: 12px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
  }
  
  .form-card h3 {
    font-size: 1.8rem;
    color: #1a3a52;
    margin-bottom: 2rem;
    font-weight: 700;
  }
  
  .form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
  }
  
  .form-group {
    margin-bottom: 1.5rem;
  }
  
  .form-group label {
    display: block;
    color: #495057;
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
    letter-spacing: 1px;
  }
  
  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    padding: 0.9rem 1rem;
    border: 1px solid #dee2e6;
    border-radius: 5px;
    font-size: 1rem;
    font-family: inherit;
    transition: all 0.3s;
  }
  
  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus {
    outline: none;
    border-color: #c9a55c;
    box-shadow: 0 0 0 3px rgba(201, 165, 92, 0.1);
  }
  
  .form-group textarea {
    resize: vertical;
  }
  
  .btn-submit {
    width: 100%;
    background: linear-gradient(135deg, #c9a55c 0%, #b8944d 100%);
    color: white;
    border: none;
    padding: 1.1rem;
    border-radius: 5px;
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: 1px;
    cursor: pointer;
    transition: all 0.3s;
  }
  
  .btn-submit:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(201, 165, 92, 0.4);
  }
  
  @media (max-width: 968px) {
    .contact {
      padding: 3.5rem 0;
    }
    
    .container {
      padding: 0 1.2rem;
    }
    
    .section-header {
      margin-bottom: 3rem;
    }
    
    .section-tag {
      font-size: 0.75rem;
    }
    
    .section-header h2 {
      font-size: 1.8rem;
      margin: 0.8rem 0;
    }
    
    .section-header p {
      font-size: 0.95rem;
    }
    
    .contact-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
    
    .info-card {
      padding: 2rem 1.5rem;
    }
    
    .info-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.8rem;
    }
    
    .info-card > p {
      font-size: 0.95rem;
      margin-bottom: 2rem;
    }
    
    .info-items {
      gap: 1.5rem;
      margin-bottom: 2rem;
    }
    
    .info-item {
      gap: 1.2rem;
    }
    
    .info-icon {
      width: 45px;
      height: 45px;
    }
    
    .info-icon svg {
      width: 22px;
      height: 22px;
    }
    
    .info-item h4 {
      font-size: 1rem;
      margin-bottom: 0.3rem;
    }
    
    .info-item p {
      font-size: 0.9rem;
    }
    
    .form-card {
      padding: 2rem 1.5rem;
    }
    
    .form-card h3 {
      font-size: 1.5rem;
      margin-bottom: 1.2rem;
    }
    
    .form-row {
      grid-template-columns: 1fr;
      gap: 1rem;
    }
    
    .form-group label {
      font-size: 0.75rem;
    }
    
    .form-group input,
    .form-group select,
    .form-group textarea {
      font-size: 0.95rem;
      padding: 0.9rem 1rem;
    }
    
    .btn-submit {
      padding: 1rem;
      font-size: 0.95rem;
    }
  }
</style>
