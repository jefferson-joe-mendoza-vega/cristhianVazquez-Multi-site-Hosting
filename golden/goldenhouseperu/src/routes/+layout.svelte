<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<!-- Primary Meta Tags -->
	<title>Golden House | Inmobiliaria y Construcción en Cajamarca, Perú</title>
	<meta name="title" content="Golden House | Inmobiliaria y Construcción en Cajamarca, Perú" />
	<meta name="description" content="Inmobiliaria líder en Cajamarca con más de 15 años de experiencia. Ofrecemos terrenos, casas, departamentos y servicios de construcción. 250+ proyectos completados." />
	<meta name="keywords" content="inmobiliaria cajamarca, casas cajamarca, departamentos cajamarca, terrenos cajamarca, construcción cajamarca, golden house peru" />
	<meta name="author" content="Golden House" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	
	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://goldenhouse.com.pe/" />
	<meta property="og:title" content="Golden House | Inmobiliaria y Construcción en Cajamarca, Perú" />
	<meta property="og:description" content="Tu hogar ideal te espera. Más de 15 años construyendo sueños en Cajamarca. Terrenos, casas, departamentos y construcción a medida." />
	<meta property="og:image" content="https://goldenhouse.com.pe/fondo.png" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />
	<meta property="og:locale" content="es_PE" />
	<meta property="og:site_name" content="Golden House" />
	
	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://goldenhouse.com.pe/" />
	<meta property="twitter:title" content="Golden House | Inmobiliaria y Construcción en Cajamarca" />
	<meta property="twitter:description" content="Tu hogar ideal te espera. Más de 15 años construyendo sueños en Cajamarca. Terrenos, casas, departamentos y construcción a medida." />
	<meta property="twitter:image" content="https://goldenhouse.com.pe/fondo.png" />
	
	<!-- Additional Meta Tags -->
	<meta name="robots" content="index, follow" />
	<meta name="language" content="Spanish" />
	<meta name="geo.region" content="PE-CAJ" />
	<meta name="geo.placename" content="Cajamarca" />
	<meta name="geo.position" content="-7.1617;-78.5125" />
	<meta name="ICBM" content="-7.1617, -78.5125" />
	
	<!-- Contact & Business Info -->
	<meta name="contact" content="info@goldenhouse.com.pe" />
	<meta name="phone" content="+51 915 173 349" />
	
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
		"name": "Golden House",
		"image": "https://goldenhouse.com.pe/logo.png",
		"description": "Inmobiliaria y construcción en Cajamarca, Perú. Más de 15 años de experiencia ofreciendo terrenos, casas, departamentos y servicios de construcción.",
		"url": "https://goldenhouse.com.pe",
		"telephone": "+51915173349",
		"email": "info@goldenhouse.com.pe",
		"address": {
			"@type": "PostalAddress",
			"addressLocality": "Cajamarca",
			"addressCountry": "PE"
		},
		"geo": {
			"@type": "GeoCoordinates",
			"latitude": "-7.1617",
			"longitude": "-78.5125"
		},
		"sameAs": [
			"https://web.facebook.com/profile.php?id=100076331190287",
			"https://wa.me/51913685917"
		],
		"aggregateRating": {
			"@type": "AggregateRating",
			"ratingValue": "4.9",
			"reviewCount": "250"
		},
		"priceRange": "$$$"
	}
	</script>
</svelte:head>

{@render children()}
