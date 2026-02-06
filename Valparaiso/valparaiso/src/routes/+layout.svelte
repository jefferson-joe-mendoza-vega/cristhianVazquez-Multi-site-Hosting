<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<!-- Primary Meta Tags -->
	<title>Inmobiliaria Valparaíso | Proyecto Ladera Real - La Colpa, Cajamarca</title>
	<meta name="title" content="Inmobiliaria Valparaíso | Proyecto Ladera Real - La Colpa, Cajamarca" />
	<meta name="description" content="Desarrolladora de proyectos con Alta Plusvalía. Lotes desde 100m² en La Colpa desde S/30,000. Plusvalía proyectada 18% anual. Trato directo, inversión respaldada." />
	<meta name="keywords" content="terrenos cajamarca, la colpa, ladera real, inmobiliaria cajamarca, lotes cajamarca, inversión inmobiliaria, valparaíso inmobiliaria, alta plusvalía" />
	<meta name="author" content="Inmobiliaria Valparaíso" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	
	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://inmobiliaria-valparaiso.com/" />
	<meta property="og:title" content="Proyecto Ladera Real - La Colpa | Valparaíso Inmobiliaria" />
	<meta property="og:description" content="Invierte donde La Colpa ya está creciendo. Lotes desde 100m² desde S/30,000. Plusvalía proyectada 18% anual. Trato directo." />
	<meta property="og:image" content="https://inmobiliaria-valparaiso.com/fondo.jpg" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />
	<meta property="og:locale" content="es_PE" />
	<meta property="og:site_name" content="Inmobiliaria Valparaíso" />
	
	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://inmobiliaria-valparaiso.com/" />
	<meta property="twitter:title" content="Proyecto Ladera Real - La Colpa | Valparaíso Inmobiliaria" />
	<meta property="twitter:description" content="Invierte donde La Colpa ya está creciendo. Lotes desde 100m² desde S/30,000. Plusvalía proyectada 18% anual." />
	<meta property="twitter:image" content="https://inmobiliaria-valparaiso.com/fondo.jpg" />
	
	<!-- Additional Meta Tags -->
	<meta name="robots" content="index, follow" />
	<meta name="language" content="Spanish" />
	<meta name="geo.region" content="PE-CAJ" />
	<meta name="geo.placename" content="Cajamarca" />
	<meta name="geo.position" content="-7.1617;-78.5125" />
	<meta name="ICBM" content="-7.1617, -78.5125" />
	
	<!-- Contact & Business Info -->
	<meta name="contact" content="contacto@inmobiliaria-valparaiso.com" />
	<meta name="phone" content="+51 978 764 181" />
	
	<!-- Favicon -->
	<link rel="icon" href={favicon} />
	<link rel="apple-touch-icon" href="/logo.png" />
	
	<!-- Fonts -->
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
	
	<!-- Structured Data (JSON-LD) -->
	<script type="application/ld+json">
	{
		"@context": "https://schema.org",
		"@type": "RealEstateAgent",
		"name": "Inmobiliaria Valparaíso",
		"image": "https://inmobiliaria-valparaiso.com/logo.png",
		"description": "Desarrolladora de proyectos con Alta Plusvalía. Proyecto Ladera Real en La Colpa, Cajamarca. Lotes desde 100m² con plusvalía proyectada del 18% anual.",
		"url": "https://inmobiliaria-valparaiso.com",
		"telephone": "+51978764181",
		"email": "contacto@inmobiliaria-valparaiso.com",
		"address": {
			"@type": "PostalAddress",
			"addressLocality": "La Colpa, Cajamarca",
			"addressCountry": "PE"
		},
		"geo": {
			"@type": "GeoCoordinates",
			"latitude": "-7.1617",
			"longitude": "-78.5125"
		},
		"sameAs": [
			"https://web.facebook.com/profile.php?id=61573192016351",
			"https://www.instagram.com/inmobiliariavalparaiso",
			"https://wa.me/51978764181"
		],
		"priceRange": "S/ 30,000 - S/ 60,000"
	}
	</script>
</svelte:head>

{@render children()}
